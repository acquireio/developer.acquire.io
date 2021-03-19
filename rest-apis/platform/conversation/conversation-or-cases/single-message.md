# Single Message

{% api-method method="get" host="https://suthar.uat.env.acquire.io/api/v1/crm/objects/case-message/{caseMessageId}?relations=case&select=id&select=caseId&select=channel&select=senderId&select=senderType&select=type&select=message&select=dateCreated&select=dateUpdated&select=seen&select=meta" path="" %}
{% api-method-summary %}
Get a message
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="caseMessageId" type="string" required=true %}
ID of the case
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="select" type="string" required=false %}
id\|caseId\|channel\|senderId\|senderType\|type\|  
message\|dateCreated\|dateUpdated\|seen\|meta
{% endapi-method-parameter %}

{% api-method-parameter name="relations" type="string" required=false %}
'case' \(To get messages with case details\)
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "data": {
    "id": 5,
    "channel": null,
    "senderId": 1,
    "senderType": "user",
    "type": "event",
    "message": "Surendra Suthar just joined this chat.",
    "dateCreated": "2020-05-27T05:55:04.000Z",
    "dateUpdated": null,
    "seen": "yes",
    "meta": {},
    "case": {
      "dateCreated": "2020-05-27T05:52:12.000Z",
      "dateUpdated": "2020-05-27T05:55:06.000Z",
      "id": 2,
      "contactId": 77,
      "closedBy": 1,
      "visitId": 4,
      "title": "#77 : Hello",
      "description": "Hello",
      "channel": "chat",
      "status": "closed",
      "closingState": "handled",
      "dateQueue": "2020-05-27T05:52:12.000Z",
      "datePending": "2020-05-27T05:52:12.000Z",
      "dateActive": "2020-05-27T05:55:04.000Z",
      "dateClosed": "2020-05-27T05:55:06.000Z",
      "queueId": null,
      "queueOrder": null,
      "meta": {
        "_routes": {}
      },
      "parentId": null,
      "userId": null,
      "waitTime": 0,
      "threadId": 2
    }
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

