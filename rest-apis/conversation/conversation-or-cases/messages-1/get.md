---
description: Get a single message based on its ID
---

# Retrieve a message

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/objects/case-message/{{messageId}}" path="" %}
{% api-method-summary %}
Get
{% endapi-method-summary %}

{% api-method-description %}
Retrieve a single message by passing its **messageId** in to the endpoint as a path parameter. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="messageId" type="integer" required=true %}
ID of the message 
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "data": {
    "id": 8285,
    "caseId": 2068,
    "channel": "chat",
    "senderId": 1,
    "senderType": "user",
    "type": "message",
    "message": "hijk",
    "dateCreated": "2021-03-30T15:15:52.000Z",
    "dateUpdated": "2021-03-30T15:16:02.000Z",
    "seen": "no",
    "meta": {},
    "sender": {
      "roles": [],
      "id": 1,
      "name": "David Guetta",
      "firstName": "David Guetta",
      "lastName": "",
      "photo": "",
      "email": "user@example.com",
      "clientId": "",
      "parentId": 0,
      "type": "user",
      "accessLevel": null
    }
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

