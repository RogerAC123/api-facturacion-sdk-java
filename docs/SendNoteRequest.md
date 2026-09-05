

# SendNoteRequest


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
|**afectadoTipoDoc** | [**AfectadoTipoDocEnum**](#AfectadoTipoDocEnum) |  |  |
|**afectadoNumDoc** | **String** |  |  |
|**motivoCod** | **String** |  |  |
|**motivoDes** | **String** |  |  |
|**montoOperGravadas** | **BigDecimal** |  |  [optional] |
|**montoOperExoneradas** | **BigDecimal** |  |  [optional] |
|**montoOperInafectas** | **BigDecimal** |  |  [optional] |
|**montoIgv** | **BigDecimal** |  |  |
|**totalImpuestos** | **BigDecimal** |  |  |
|**valorVenta** | **BigDecimal** |  |  |
|**subTotal** | **BigDecimal** |  |  |
|**montoImpVenta** | **BigDecimal** |  |  |
|**descuentoGlobal** | **BigDecimal** |  |  [optional] |
|**descuentoGlobalBase** | **BigDecimal** |  |  [optional] |
|**detalle** | [**List&lt;SendInvoiceRequestDetalleInner&gt;**](SendInvoiceRequestDetalleInner.md) |  |  |
|**leyendas** | [**List&lt;SendInvoiceRequestLeyendasInner&gt;**](SendInvoiceRequestLeyendasInner.md) |  |  |
|**observacion** | **String** |  |  [optional] |



## Enum: TipoDocEnum

| Name | Value |
|---- | -----|
| _07 | &quot;07&quot; |
| _08 | &quot;08&quot; |



## Enum: AfectadoTipoDocEnum

| Name | Value |
|---- | -----|
| _01 | &quot;01&quot; |
| _03 | &quot;03&quot; |



