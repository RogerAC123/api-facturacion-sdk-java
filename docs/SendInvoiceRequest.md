

# SendInvoiceRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**tipoOperacion** | **String** |  |  [optional] |
|**tipoDoc** | [**TipoDocEnum**](#TipoDocEnum) |  |  |
|**serie** | **String** |  |  |
|**correlativo** | **String** |  |  |
|**tipoMoneda** | **String** |  |  [optional] |
|**fechaEmision** | **String** |  |  |
|**empresaRuc** | **String** |  |  |
|**establecimientoCodigo** | **String** |  |  [optional] |
|**clienteTipoDoc** | **String** |  |  |
|**clienteNumDoc** | **String** |  |  |
|**clienteRazonSocial** | **String** |  |  |
|**clienteDireccion** | **String** |  |  [optional] |
|**clienteDistrito** | **String** |  |  [optional] |
|**clienteProvincia** | **String** |  |  [optional] |
|**clienteDepartamento** | **String** |  |  [optional] |
|**montoOperGravadas** | **BigDecimal** |  |  [optional] |
|**montoOperExoneradas** | **BigDecimal** |  |  [optional] |
|**montoOperInafectas** | **BigDecimal** |  |  [optional] |
|**montoOperGratuitas** | **BigDecimal** |  |  [optional] |
|**montoIgv** | **BigDecimal** |  |  |
|**totalImpuestos** | **BigDecimal** |  |  |
|**valorVenta** | **BigDecimal** |  |  |
|**subTotal** | **BigDecimal** |  |  |
|**montoImpVenta** | **BigDecimal** |  |  |
|**descuentoGlobal** | **BigDecimal** |  |  [optional] |
|**descuentoGlobalBase** | **BigDecimal** |  |  [optional] |
|**detalle** | [**List&lt;SendInvoiceRequestDetalleInner&gt;**](SendInvoiceRequestDetalleInner.md) |  |  |
|**formaPago** | [**List&lt;SendInvoiceRequestFormaPagoInner&gt;**](SendInvoiceRequestFormaPagoInner.md) |  |  |
|**leyendas** | [**List&lt;SendInvoiceRequestLeyendasInner&gt;**](SendInvoiceRequestLeyendasInner.md) |  |  |
|**observacion** | **String** |  |  [optional] |
|**vendedor** | **String** |  |  [optional] |
|**pagos** | [**List&lt;SendInvoiceRequestPagosInner&gt;**](SendInvoiceRequestPagosInner.md) |  |  [optional] |
|**detraccion** | [**SendInvoiceRequestDetraccion**](SendInvoiceRequestDetraccion.md) |  |  [optional] |
|**guiaRemision** | [**List&lt;SendInvoiceRequestGuiaRemisionInner&gt;**](SendInvoiceRequestGuiaRemisionInner.md) |  |  [optional] |



## Enum: TipoDocEnum

| Name | Value |
|---- | -----|
| _01 | &quot;01&quot; |
| _03 | &quot;03&quot; |



