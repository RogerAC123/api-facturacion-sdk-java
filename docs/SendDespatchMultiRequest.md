

# SendDespatchMultiRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**tipoDoc** | [**TipoDocEnum**](#TipoDocEnum) |  |  |
|**serie** | **String** |  |  |
|**observacion** | **String** |  |  [optional] |
|**fechaEmision** | **String** |  |  |
|**empresaRuc** | **String** |  |  |
|**establecimientoCodigo** | **String** |  |  [optional] |
|**guiaCodTraslado** | **String** |  |  |
|**guiaModTraslado** | [**GuiaModTrasladoEnum**](#GuiaModTrasladoEnum) |  |  |
|**guiaFecTraslado** | **String** |  |  |
|**guiaVehiculoPlaca** | **String** |  |  [optional] |
|**transportistaTipoDoc** | **String** |  |  [optional] |
|**transportistaNumDoc** | **String** |  |  [optional] |
|**transportistaRazonSocial** | **String** |  |  [optional] |
|**transportistaNroMtc** | **String** |  |  [optional] |
|**guiaPartidaUbigeo** | **String** |  |  |
|**guiaPartidaDireccion** | **String** |  |  |
|**chofer** | [**List&lt;SendDespatchRequestChoferInner&gt;**](SendDespatchRequestChoferInner.md) |  |  [optional] |
|**guiaFecEntrega** | **String** |  |  [optional] |
|**guiaDesTraslado** | **String** |  |  [optional] |
|**guiaPesoNeto** | **BigDecimal** |  |  [optional] |
|**guiaSustentoPeso** | **String** |  |  [optional] |
|**guiaNumBultos** | **Integer** |  |  [optional] |
|**indicadores** | [**SendDespatchRequestIndicadores**](SendDespatchRequestIndicadores.md) |  |  [optional] |
|**contenedores** | [**List&lt;SendDespatchRequestContenedoresInner&gt;**](SendDespatchRequestContenedoresInner.md) |  |  [optional] |
|**guiaVehiculoTuc** | **String** |  |  [optional] |
|**guiaVehiculoAutorizacion** | **String** |  |  [optional] |
|**guiaVehiculoAutorizacionEntidad** | **String** |  |  [optional] |
|**vehiculosSecundarios** | [**List&lt;SendDespatchRequestVehiculosSecundariosInner&gt;**](SendDespatchRequestVehiculosSecundariosInner.md) |  |  [optional] |
|**transportistaAutorizacion** | **String** |  |  [optional] |
|**transportistaAutorizacionEntidad** | **String** |  |  [optional] |
|**guiaPartidaRuc** | **String** |  |  [optional] |
|**guiaPartidaCodLocal** | **String** |  |  [optional] |
|**guiaPartidaGeo** | [**SendDespatchRequestGuiaLlegadaGeo**](SendDespatchRequestGuiaLlegadaGeo.md) |  |  [optional] |
|**guiaLlegadaRuc** | **String** |  |  [optional] |
|**guiaLlegadaCodLocal** | **String** |  |  [optional] |
|**guiaLlegadaGeo** | [**SendDespatchRequestGuiaLlegadaGeo**](SendDespatchRequestGuiaLlegadaGeo.md) |  |  [optional] |
|**documentosRelacionados** | [**List&lt;SendDespatchRequestDocumentosRelacionadosInner&gt;**](SendDespatchRequestDocumentosRelacionadosInner.md) |  |  [optional] |
|**remitenteAutorizacion** | **String** |  |  [optional] |
|**remitenteAutorizacionEntidad** | **String** |  |  [optional] |
|**proveedorTipoDoc** | **String** |  |  [optional] |
|**proveedorNumDoc** | **String** |  |  [optional] |
|**proveedorRazonSocial** | **String** |  |  [optional] |
|**compradorTipoDoc** | **String** |  |  [optional] |
|**compradorNumDoc** | **String** |  |  [optional] |
|**compradorRazonSocial** | **String** |  |  [optional] |
|**puertoCodigo** | **String** |  |  [optional] |
|**puertoNombre** | **String** |  |  [optional] |
|**puertoTipo** | **String** |  |  [optional] |
|**destinos** | [**List&lt;SendDespatchMultiRequestDestinosInner&gt;**](SendDespatchMultiRequestDestinosInner.md) |  |  |



## Enum: TipoDocEnum

| Name | Value |
|---- | -----|
| _09 | &quot;09&quot; |



## Enum: GuiaModTrasladoEnum

| Name | Value |
|---- | -----|
| _01 | &quot;01&quot; |
| _02 | &quot;02&quot; |



