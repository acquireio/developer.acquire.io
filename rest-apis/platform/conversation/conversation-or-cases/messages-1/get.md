---
description: Get a single message based on its ID
---

# Retrieve a message

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/objects/case-message/{MessageId}" path="" %}
{% api-method-summary %}
Get
{% endapi-method-summary %}

{% api-method-description %}
Retrieve a single message by passing its MessageId into the endpoint as a path parameter. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
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
      "meta": {
        "fields": {
          "onboard_setup": {
            "structValue": {
              "fields": {
                "install": {
                  "boolValue": false,
                  "kind": "boolValue"
                },
                "welcome": {
                  "boolValue": false,
                  "kind": "boolValue"
                },
                "setupMail": {
                  "boolValue": false,
                  "kind": "boolValue"
                },
                "setupVoip": {
                  "boolValue": false,
                  "kind": "boolValue"
                },
                "setupAppStore": {
                  "boolValue": false,
                  "kind": "boolValue"
                },
                "setupSocialApp": {
                  "boolValue": false,
                  "kind": "boolValue"
                }
              }
            },
            "kind": "structValue"
          },
          "productUpdate": {
            "structValue": {
              "fields": {
                "data": {
                  "listValue": {
                    "values": []
                  },
                  "kind": "listValue"
                },
                "lastSeenArticleLength": {
                  "numberValue": 0,
                  "kind": "numberValue"
                }
              }
            },
            "kind": "structValue"
          }
        }
      },
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

