# intifact-sdk (Java)

SDK Java para la **API de Facturación Electrónica SUNAT de Intifact** (Perú),
generado con [OpenAPI Generator](https://openapi-generator.tech) desde el spec
que la API expone en `/docs/json`. Facturas, boletas, notas de crédito/débito,
guías de remisión (remitente y transportista), resúmenes diarios y
comunicaciones de baja.

## Requisitos

- Java 8+
- Maven o Gradle (el proyecto trae wrappers `mvnw`/`gradlew`, no necesitas
  tenerlos instalados globalmente)

## Instalación

### Maven

```xml
<dependency>
  <groupId>com.intifact</groupId>
  <artifactId>intifact-sdk</artifactId>
  <version>1.0.0</version>
</dependency>
```

### Gradle

```groovy
implementation 'com.intifact:intifact-sdk:1.0.0'
```

## Autenticación

La API no está modelada con un `securityScheme` de OpenAPI (el chequeo de
API key vive en un plugin de Fastify), así que el header se agrega a mano vía
`addDefaultHeader` — el SDK lo manda en cada request a partir de ahí:

```java
import com.intifact.sdk.client.ApiClient;

ApiClient client = new ApiClient();
client.setBasePath("https://api-facturacion.intifact.com");
client.addDefaultHeader("Authorization", "Bearer " + System.getenv("FACTURACION_API_KEY"));
```

## Uso básico — enviar una factura

```java
import com.intifact.sdk.api.InvoiceApi;
import com.intifact.sdk.client.ApiException;
import com.intifact.sdk.model.*;
import java.math.BigDecimal;
import java.util.List;

InvoiceApi invoiceApi = new InvoiceApi(client);

// Los montos son BigDecimal (precisión exacta, no double) y los campos con
// catálogo SUNAT (tipoDoc, clienteTipoDoc, ...) son enums tipados, no String.
ApiV1InvoiceSendPostRequestDetalleInner item = new ApiV1InvoiceSendPostRequestDetalleInner()
    .unidad("NIU")
    .cantidad(new BigDecimal("2"))
    .codProducto("PROD001")
    .descripcion("Laptop HP 15")
    .montoValorUnitario(new BigDecimal("2500.00"))
    .montoBaseIgv(new BigDecimal("5000.00"))
    .porcentajeIgv(new BigDecimal("18"))
    .igv(new BigDecimal("900.00"))
    .tipAfeIgv("10")
    .totalImpuestos(new BigDecimal("900.00"))
    .montoPrecioUnitario(new BigDecimal("2950.00"))
    .montoValorVenta(new BigDecimal("5000.00"))
    // Código de Producto SUNAT (UNSPSC) — SUNAT lo exige desde 2027-01-01
    // para determinados bienes (error 3496 si falta o es inválido).
    .codProdSunat("43211508");

ApiV1InvoiceSendPostRequest body = new ApiV1InvoiceSendPostRequest()
    .empresaRuc("20553510661")
    .tipoDoc(ApiV1InvoiceSendPostRequest.TipoDocEnum._01)
    .serie("F001")
    .correlativo("100")
    .tipoMoneda("PEN")
    .fechaEmision("2026-01-15")
    .tipoOperacion("0101")
    .clienteTipoDoc("6")
    .clienteNumDoc("20000000001")
    .clienteRazonSocial("EMPRESA CLIENTE SAC")
    .addDetalleItem(item)
    .montoOperGravadas(new BigDecimal("5000.00"))
    .montoOperExoneradas(new BigDecimal("0"))
    .montoIgv(new BigDecimal("900.00"))
    .totalImpuestos(new BigDecimal("900.00"))
    .valorVenta(new BigDecimal("5000.00"))
    .subTotal(new BigDecimal("5900.00"))
    .montoImpVenta(new BigDecimal("5900.00"))
    .addFormaPagoItem(new ApiV1InvoiceSendPostRequestFormaPagoInner()
        .tipo(ApiV1InvoiceSendPostRequestFormaPagoInner.TipoEnum.CONTADO)
        .monto(new BigDecimal("5900.00")).fechaPago("2026-01-15"))
    .addLeyendasItem(new ApiV1InvoiceSendPostRequestLeyendasInner()
        .legendCode("1000").legendValue("CINCO MIL NOVECIENTOS CON 00/100 SOLES"));

try {
    ApiV1InvoiceSendPost202Response resp = invoiceApi.apiV1InvoiceSendPost(body);
    // 202 — el documento queda ENCOLADO, SUNAT lo procesa en background
    System.out.println("Encolado: " + resp.getData().getId());
} catch (ApiException e) {
    // El body real del error (400/401/409/...) viene en getResponseBody()
    System.out.println("Error " + e.getCode() + ": " + e.getResponseBody());
}
```

## Manejo de errores

Toda respuesta fuera de 2xx llega como `ApiException` (no como excepción
genérica de red): `e.getCode()` trae el status HTTP y `e.getResponseBody()`
el JSON crudo `{ success: false, message, errors? }` que devuelve la API.

```java
try {
    invoiceApi.apiV1InvoiceSendPost(body);
} catch (ApiException e) {
    if (e.getCode() == 409) {
        // Comprobante ya en proceso — NO reintentar con otro correlativo,
        // esperar el resultado. Ver /documents/{id} para el estado final.
    }
}
```

## APIs disponibles

| Clase | Para qué |
|---|---|
| `InvoiceApi` | Facturas/boletas: enviar, PDF, XML, CDR |
| `NoteApi` | Notas de crédito/débito |
| `DespatchApi` | Guías de remisión (remitente y transportista) |
| `SummaryApi` | Resumen diario y comunicación de baja; `getSummary(id)` da el estado del envío |
| `DocumentsApi` | Listar/consultar documentos, reintentar fallidos |
| `QueuesApi` | Estado de las colas BullMQ |
| `CompanyApi` / `BranchesApi` | Empresas y establecimientos (solo lectura) |
| `PlansApi` | Planes y consumo (quota) |
| `PublicApi` | Consulta pública de comprobantes (sin auth) |
| `AuthApi` | Autenticación |
| `SystemApi` | `/health`, catálogos SUNAT |

## Compilar desde el código fuente

```bash
./gradlew build      # o: ./mvnw package
```

> **Desde la 3.0** la administración de la cuenta —crear o editar empresas,
> credenciales SOL/GRE, certificado, logo, registrar establecimientos y
> **webhooks**— se hace desde el panel de Intifact, no con la API key (la API
> responde `403`). Por eso `WebhooksApi` y los métodos de escritura de
> `CompanyApi`/`BranchesApi` ya no están en el SDK: una key filtrada solo
> puede emitir y consultar.

## Regenerar desde la API

El proyecto se generó con [OpenAPI Generator](https://openapi-generator.tech)
(`java`, librería `okhttp-gson`) contra `https://api-facturacion.intifact.com/docs/json`.
Para regenerar tras un cambio de la API:

```bash
npx @openapitools/openapi-generator-cli generate \
  -i https://api-facturacion.intifact.com/docs/json \
  -g java --library okhttp-gson \
  --group-id com.intifact --artifact-id intifact-sdk \
  --api-package com.intifact.sdk.api \
  --model-package com.intifact.sdk.model \
  --invoker-package com.intifact.sdk.client \
  -o .
```

## Nota sobre los nombres de métodos

Las rutas de la API no declaran `operationId` explícito en su schema de
Fastify, así que el generador deriva nombres desde el método+path
(`apiV1InvoiceSendPost` en vez de algo como `sendInvoice`). Si la API le
agrega `operationId` a sus rutas, una regeneración futura produciría nombres
más limpios sin romper compatibilidad de comportamiento.
