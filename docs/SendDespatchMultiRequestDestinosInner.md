

# SendDespatchMultiRequestDestinosInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
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
|**guiaLlegadaUbigeo** | **String** |  |  |
|**guiaLlegadaDireccion** | **String** |  |  |
|**guiaPesoTotal** | **BigDecimal** |  |  |
|**guiaUndPesoTotal** | **String** |  |  [optional] |
|**detalle** | [**List&lt;SendDespatchRequestDetalleInner&gt;**](SendDespatchRequestDetalleInner.md) |  |  |



## Enum: ModalidadEntregaEnum

| Name | Value |
|---- | -----|
| DOMICILIO | &quot;DOMICILIO&quot; |
| AGENCIA | &quot;AGENCIA&quot; |



