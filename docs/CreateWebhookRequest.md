

# CreateWebhookRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**empresaRuc** | **String** |  |  [optional] |
|**tenantId** | **UUID** |  |  [optional] |
|**url** | **URI** |  |  |
|**events** | [**List&lt;EventsEnum&gt;**](#List&lt;EventsEnum&gt;) |  |  |
|**description** | **String** |  |  [optional] |
|**secret** | **String** |  |  [optional] |



## Enum: List&lt;EventsEnum&gt;

| Name | Value |
|---- | -----|
| DOCUMENT_ACCEPTED | &quot;document.accepted&quot; |
| DOCUMENT_REJECTED | &quot;document.rejected&quot; |
| DOCUMENT_QUEUE_FAILED | &quot;document.queue_failed&quot; |
| DOCUMENT_RETRIED | &quot;document.retried&quot; |
| TICKET_RESOLVED | &quot;ticket.resolved&quot; |



