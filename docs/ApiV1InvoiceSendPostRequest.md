

# ApiV1InvoiceSendPostRequest


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
|**detalle** | [**List&lt;ApiV1InvoiceSendPostRequestDetalleInner&gt;**](ApiV1InvoiceSendPostRequestDetalleInner.md) |  |  |
|**formaPago** | [**List&lt;ApiV1InvoiceSendPostRequestFormaPagoInner&gt;**](ApiV1InvoiceSendPostRequestFormaPagoInner.md) |  |  |
|**leyendas** | [**List&lt;ApiV1InvoiceSendPostRequestLeyendasInner&gt;**](ApiV1InvoiceSendPostRequestLeyendasInner.md) |  |  |
|**observacion** | **String** |  |  [optional] |
|**vendedor** | **String** |  |  [optional] |
|**pagos** | [**List&lt;ApiV1InvoiceSendPostRequestPagosInner&gt;**](ApiV1InvoiceSendPostRequestPagosInner.md) |  |  [optional] |
|**detraccion** | [**ApiV1InvoiceSendPostRequestDetraccion**](ApiV1InvoiceSendPostRequestDetraccion.md) |  |  [optional] |
|**guiaRemision** | [**List&lt;ApiV1InvoiceSendPostRequestGuiaRemisionInner&gt;**](ApiV1InvoiceSendPostRequestGuiaRemisionInner.md) |  |  [optional] |



## Enum: TipoDocEnum

| Name | Value |
|---- | -----|
| _01 | &quot;01&quot; |
| _03 | &quot;03&quot; |



