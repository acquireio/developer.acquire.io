---
description: API to update a message based on its ID
---

# Update message

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/messenger/chat/message/{{messageId}}" path="" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Use this endpoint to modify a message in a Conversation. The **messageId** needs to be passed as a path parameter in the endpoint URL.  
  
**messageId** - the message ID. Use a webhook or GET request to find the message ID.   
 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The message's ID
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
    "id": 8288,
    "channel": "chat",
    "senderId": 1,
    "senderType": "user",
    "type": "message",
    "message": "updating the sent message",
    "dateCreated": "2021-03-30T16:04:11.000Z",
    "dateUpdated": "2021-03-30T16:10:54.000Z",
    "seen": "no",
    "meta": {},
    "case": {
      "dateCreated": "2021-03-30T16:04:10.000Z",
      "dateUpdated": "2021-03-30T16:05:46.000Z",
      "id": 2069,
      "contactId": 597759,
      "closedBy": null,
      "visitId": 1379,
      "title": "#597759 has just started a chat",
      "description": "Hey added from the api",
      "channel": "chat",
      "status": "active",
      "closingState": "handled",
      "dateQueue": "2021-03-30T16:04:10.000Z",
      "datePending": "2021-03-30T16:04:10.000Z",
      "dateActive": "2021-03-30T16:04:10.000Z",
      "dateClosed": null,
      "queueId": null,
      "queueOrder": null,
      "meta": {},
      "parentId": 1875,
      "userId": null,
      "waitTime": 0,
      "threadId": 1875
    },
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
    },
    "caseId": 2069,
    "threadId": 1875
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Body\(raw\)

```text
{
  "message": {
    "type": "message",
    "message": "updating the sent message",
    "translateLangKey": "en"
  }
}
```

