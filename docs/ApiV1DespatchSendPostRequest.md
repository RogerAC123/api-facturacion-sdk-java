

# ApiV1DespatchSendPostRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**tipoDoc** | [**TipoDocEnum**](#TipoDocEnum) |  |  |
|**serie** | **String** |  |  |
|**correlativo** | **String** |  |  |
|**observacion** | **String** |  |  [optional] |
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
|**destinatarioContacto** | **String** |  |  [optional] |
|**destinatarioTelefono** | **String** |  |  [optional] |
|**destinatarioEmail** | **String** |  |  [optional] |
|**entregaReferencia** | **String** |  |  [optional] |
|**modalidadEntrega** | [**ModalidadEntregaEnum**](#ModalidadEntregaEnum) |  |  [optional] |
|**agenciaNombre** | **String** |  |  [optional] |
|**agenciaSede** | **String** |  |  [optional] |
|**guiaCodTraslado** | **String** |  |  |
|**guiaModTraslado** | [**GuiaModTrasladoEnum**](#GuiaModTrasladoEnum) |  |  |
|**guiaPesoTotal** | **BigDecimal** |  |  |
|**guiaUndPesoTotal** | **String** |  |  [optional] |
|**guiaFecTraslado** | **String** |  |  |
|**guiaVehiculoPlaca** | **String** |  |  [optional] |
|**transportistaTipoDoc** | **String** |  |  [optional] |
|**transportistaNumDoc** | **String** |  |  [optional] |
|**transportistaRazonSocial** | **String** |  |  [optional] |
|**transportistaNroMtc** | **String** |  |  [optional] |
|**guiaPartidaUbigeo** | **String** |  |  |
|**guiaPartidaDireccion** | **String** |  |  |
|**guiaPartidaCiudad** | **String** |  |  [optional] |
|**guiaLlegadaUbigeo** | **String** |  |  |
|**guiaLlegadaDireccion** | **String** |  |  |
|**guiaLlegadaCiudad** | **String** |  |  [optional] |
|**chofer** | [**List&lt;ApiV1DespatchSendPostRequestChoferInner&gt;**](ApiV1DespatchSendPostRequestChoferInner.md) |  |  [optional] |
|**guiaFecEntrega** | **String** |  |  [optional] |
|**guiaDesTraslado** | **String** |  |  [optional] |
|**guiaPesoNeto** | **BigDecimal** |  |  [optional] |
|**guiaSustentoPeso** | **String** |  |  [optional] |
|**guiaNumBultos** | **Integer** |  |  [optional] |
|**indicadores** | [**ApiV1DespatchSendPostRequestIndicadores**](ApiV1DespatchSendPostRequestIndicadores.md) |  |  [optional] |
|**contenedores** | [**List&lt;ApiV1DespatchSendPostRequestContenedoresInner&gt;**](ApiV1DespatchSendPostRequestContenedoresInner.md) |  |  [optional] |
|**guiaVehiculoTuc** | **String** |  |  [optional] |
|**guiaVehiculoAutorizacion** | **String** |  |  [optional] |
|**guiaVehiculoAutorizacionEntidad** | **String** |  |  [optional] |
|**vehiculosSecundarios** | [**List&lt;ApiV1DespatchSendPostRequestVehiculosSecundariosInner&gt;**](ApiV1DespatchSendPostRequestVehiculosSecundariosInner.md) |  |  [optional] |
|**transportistaAutorizacion** | **String** |  |  [optional] |
|**transportistaAutorizacionEntidad** | **String** |  |  [optional] |
|**guiaPartidaRuc** | **String** |  |  [optional] |
|**guiaPartidaCodLocal** | **String** |  |  [optional] |
|**guiaPartidaGeo** | [**ApiV1DespatchSendPostRequestGuiaPartidaGeo**](ApiV1DespatchSendPostRequestGuiaPartidaGeo.md) |  |  [optional] |
|**guiaLlegadaRuc** | **String** |  |  [optional] |
|**guiaLlegadaCodLocal** | **String** |  |  [optional] |
|**guiaLlegadaGeo** | [**ApiV1DespatchSendPostRequestGuiaLlegadaGeo**](ApiV1DespatchSendPostRequestGuiaLlegadaGeo.md) |  |  [optional] |
|**documentosRelacionados** | [**List&lt;ApiV1DespatchSendPostRequestDocumentosRelacionadosInner&gt;**](ApiV1DespatchSendPostRequestDocumentosRelacionadosInner.md) |  |  [optional] |
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
|**detalle** | [**List&lt;ApiV1DespatchSendPostRequestDetalleInner&gt;**](ApiV1DespatchSendPostRequestDetalleInner.md) |  |  |



## Enum: TipoDocEnum

| Name | Value |
|---- | -----|
| _09 | &quot;09&quot; |



## Enum: ModalidadEntregaEnum

| Name | Value |
|---- | -----|
| DOMICILIO | &quot;DOMICILIO&quot; |
| AGENCIA | &quot;AGENCIA&quot; |



## Enum: GuiaModTrasladoEnum

| Name | Value |
|---- | -----|
| _01 | &quot;01&quot; |
| _02 | &quot;02&quot; |



