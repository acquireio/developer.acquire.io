# Send Message

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/messenger/chat/add-message?-x-user-type=user" path="" %}
{% api-method-summary %}
Send a message
{% endapi-method-summary %}

{% api-method-description %}
 This API can be used to send a message in a conversation. To send a message to a customer, you must pass an object of the message.  
**Type, message, and caseID** are mandatory in the message object to send the message, you can also add transAngec to the message object for message translation.  
  
`caseId` - You can get **CaseId** from Webhook or from the conversation or chat API.  
  
`Type` - This indicates the type of message. There can be 1 type of message **\(message, note, event\)**.  
  
The **'-x-user-type'** in the query string parameter value **'user'** indicates the message sender, which means that the message is being sent from the agent side.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="-x-user-type" type="string" required=false %}
user
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
        "channel": "chat",
        "senderType": "user",
        "senderId": 23,
        "type": "message",
        "seen": "no",
        "message": "this is test message",
        "meta": {},
        "dateCreated": "2021-03-10T11:32:00.000Z",
        "case": {
            "dateCreated": "2020-12-24T12:15:21.000Z",
            "dateUpdated": "2020-12-24T12:15:46.000Z",
            "id": 28,
            "closedBy": null,
            "visitId": 35,
            "title": "#5 has just started a chat",
            "description": "dassd",
            "channel": "chat",
            "status": "active",
            "closingState": "handled",
            "dateQueue": "2020-12-24T12:15:21.000Z",
            "datePending": "2020-12-24T12:15:21.000Z",
            "dateActive": "2020-12-24T12:15:46.000Z",
            "dateClosed": null,
            "queueId": null,
            "queueOrder": 0,
            "meta": {
                "queues": [
                    1
                ],
                "sessionId": "1727541200",
                "queueRecheck": "no"
            },
            "parentId": null,
            "userId": null,
            "waitTime": 26,
            "contact": {
                "dateCreated": "2020-12-10T11:54:24.000Z",
                "dateUpdated": "2021-03-03T10:19:49.000Z",
                "id": 5,
                "clientType": "web",
                "clientName": "Chrome",
                "clientVersion": "88.0",
                "clientOsName": "Windows",
                "clientOsVersion": "10",
                "clientDeviceType": "Desktop",
                "clientDeviceVendor": null,
                "clientDeviceModel": null,
                "clientDetails": {
                    "ua": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/88.0.4324.190 Safari/537.36",
                    "engine": {
                        "name": "Blink",
                        "version": "88.0.4324.190"
                    },
                    "network": {
                        "type": "4g",
                        "speed": "18"
                    }
                },
                "meta": {},
                "archive": "no",
                "companyId": null
            },
            "users": [
                {
                    "id": 74,
                    "caseId": 28,
                    "type": "user",
                    "userId": 1,
                    "role": "owner",
                    "status": "active",
                    "dateCreated": "2020-12-24T12:15:20.000Z",
                    "dateLastAssigned": "2020-12-24T12:15:21.000Z",
                    "closed": "no",
                    "meta": null
                },
                {
                    "id": 73,
                    "caseId": 28,
                    "type": "contact",
                    "userId": 5,
                    "role": "owner",
                    "status": "active",
                    "dateCreated": "2020-12-24T12:15:20.000Z",
                    "dateLastAssigned": "2020-12-24T12:15:20.000Z",
                    "closed": "no",
                    "meta": null
                }
            ],
            "threadId": 28
        },
        "sender": {
            "departments": [],
            "roles": [],
            "id": 23,
            "name": "TokenNew",
            "firstName": "TokenNew",
            "lastName": "",
            "photo": "",
            "email": "",
            "clientId": "",
            "parentId": 0,
            "metaDetails": {
                "isBotClient": false,
                "label": ""
            },
            "type": "user",
            "accessLevel": null
        },
        "dateUpdated": null,
        "id": 328,
        "caseId": 28,
        "threadId": 28
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

**Body\(row\)**

```text
{
  "message": {
    "type": "message",
    "message": "this is test message"
  },
  "caseId":28
}
```

**Response JSON**

