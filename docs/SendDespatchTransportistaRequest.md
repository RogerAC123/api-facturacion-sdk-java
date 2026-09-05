

# SendDespatchTransportistaRequest


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
|**transportistaNroMtc** | **String** |  |  [optional] |
|**destinatarioTipoDoc** | **String** |  |  |
|**destinatarioNumDoc** | **String** |  |  |
|**destinatarioRazonSocial** | **String** |  |  |
|**destinatarioDireccion** | **String** |  |  [optional] |
|**destinatarioDistrito** | **String** |  |  [optional] |
|**destinatarioProvincia** | **String** |  |  [optional] |
|**destinatarioDepartamento** | **String** |  |  [optional] |
|**destinatarioContacto** | **String** |  |  [optional] |
|**destinatarioTelefono** | **String** |  |  [optional] |
|**destinatarioEmail** | **String** |  |  [optional] |
|**entregaReferencia** | **String** |  |  [optional] |
|**modalidadEntrega** | [**ModalidadEntregaEnum**](#ModalidadEntregaEnum) |  |  [optional] |
|**agenciaNombre** | **String** |  |  [optional] |
|**agenciaSede** | **String** |  |  [optional] |
|**remitenteTipoDoc** | **String** |  |  |
|**remitenteNumDoc** | **String** |  |  |
|**remitenteRazonSocial** | **String** |  |  |
|**guiaCodTraslado** | **String** |  |  |
|**guiaDesTraslado** | **String** |  |  [optional] |
|**guiaPesoTotal** | **BigDecimal** |  |  |
|**guiaUndPesoTotal** | **String** |  |  [optional] |
|**guiaNumBultos** | **Integer** |  |  [optional] |
|**guiaFecTraslado** | **String** |  |  |
|**chofer** | [**List&lt;SendDespatchRequestChoferInner&gt;**](SendDespatchRequestChoferInner.md) |  |  |
|**guiaVehiculoPlaca** | **String** |  |  |
|**guiaVehiculoTuc** | **String** |  |  [optional] |
|**vehiculosSecundarios** | [**List&lt;SendDespatchTransportistaRequestVehiculosSecundariosInner&gt;**](SendDespatchTransportistaRequestVehiculosSecundariosInner.md) |  |  [optional] |
|**guiaPartidaUbigeo** | **String** |  |  |
|**guiaPartidaDireccion** | **String** |  |  |
|**guiaLlegadaUbigeo** | **String** |  |  |
|**guiaLlegadaDireccion** | **String** |  |  |
|**documentosRelacionados** | [**List&lt;SendDespatchRequestDocumentosRelacionadosInner&gt;**](SendDespatchRequestDocumentosRelacionadosInner.md) |  |  [optional] |
|**detalle** | [**List&lt;SendDespatchRequestDetalleInner&gt;**](SendDespatchRequestDetalleInner.md) |  |  |



## Enum: TipoDocEnum

| Name | Value |
|---- | -----|
| _31 | &quot;31&quot; |



## Enum: ModalidadEntregaEnum

| Name | Value |
|---- | -----|
| DOMICILIO | &quot;DOMICILIO&quot; |
| AGENCIA | &quot;AGENCIA&quot; |



