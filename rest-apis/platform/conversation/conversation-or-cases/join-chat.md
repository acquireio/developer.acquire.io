# Join Chat

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/messenger/chat/join" path="" %}
{% api-method-summary %}
Join a case/chat
{% endapi-method-summary %}

{% api-method-description %}
This API will help you to join the chat. `caseId` must be included in the body.  
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
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
        "dateCreated": "2021-03-24T10:44:35.000Z",
        "dateUpdated": "2021-03-24T10:44:48.538Z",
        "id": 1684,
        "contactId": 597752,
        "closedBy": null,
        "visitId": 1371,
        "title": "#597752 has just started a chat",
        "description": "You're being transferred to one of our agents, they'll be with you shortly.|translate",
        "channel": "chat",
        "status": "active",
        "closingState": "handled",
        "dateQueue": "2021-03-24T10:44:35.000Z",
        "datePending": "2021-03-24T10:44:35.000Z",
        "dateActive": "2021-03-24T10:44:48.538Z",
        "dateClosed": null,
        "queueId": null,
        "queueOrder": 0,
        "meta": {
            "sessionId": "1976277490",
            "queueRecheck": "no",
            "queues": [
                15
            ]
        },
        "parentId": null,
        "userId": null,
        "waitTime": 14,
        "threadId": 1684,
        "users": [
            {
                "id": 3838,
                "caseId": 1684,
                "type": "user",
                "userId": 1,
                "role": "owner",
                "status": "ignored",
                "dateCreated": "2021-03-24T10:44:35.000Z",
                "dateLastAssigned": "2021-03-24T10:44:35.000Z",
                "closed": "no",
                "meta": null,
                "user": {
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
            },
            {
                "id": 3837,
                "caseId": 1684,
                "type": "contact",
                "userId": 597752,
                "role": "owner",
                "status": "active",
                "dateCreated": "2021-03-24T10:44:35.000Z",
                "dateLastAssigned": "2021-03-24T10:44:35.000Z",
                "closed": "no",
                "meta": null,
                "user": {
                    "type": "contact",
                    "id": 597752,
                    "name": "#597752",
                    "photo": null
                }
            },
            {
                "userId": 25,
                "status": "joined",
                "type": "user",
                "closed": "no",
                "role": "owner",
                "dateCreated": "2021-03-24T10:44:48.000Z",
                "dateLastAssigned": null,
                "meta": null,
                "id": 3839,
                "user": {
                    "roles": [],
                    "id": 25,
                    "name": "a",
                    "firstName": "a",
                    "lastName": "",
                    "photo": "",
                    "email": "",
                    "clientId": "",
                    "parentId": 0,
                    "type": "user",
                    "accessLevel": null
                },
                "case": {
                    "dateCreated": "2021-03-24T10:44:35.000Z",
                    "dateUpdated": "2021-03-24T10:44:48.538Z",
                    "id": 1684,
                    "contactId": 597752,
                    "closedBy": null,
                    "visitId": 1371,
                    "title": "#597752 has just started a chat",
                    "description": "You're being transferred to one of our agents, they'll be with you shortly.|translate",
                    "channel": "chat",
                    "status": "active",
                    "closingState": "handled",
                    "dateQueue": "2021-03-24T10:44:35.000Z",
                    "datePending": "2021-03-24T10:44:35.000Z",
                    "dateActive": "2021-03-24T10:44:48.538Z",
                    "dateClosed": null,
                    "queueId": null,
                    "queueOrder": 0,
                    "meta": {
                        "sessionId": "1976277490",
                        "queueRecheck": "no",
                        "queues": [
                            15
                        ]
                    },
                    "parentId": null,
                    "userId": null,
                    "waitTime": 14,
                    "threadId": 1684,
                    "lastMessage": {
                        "id": 7783,
                        "caseId": 1684,
                        "channel": "chat",
                        "senderId": 597752,
                        "senderType": "contact",
                        "type": "event",
                        "message": "You're being transferred to one of our agents, they'll be with you shortly.|translate",
                        "dateCreated": "2021-03-24T10:44:35.000Z",
                        "dateUpdated": null,
                        "seen": "yes",
                        "meta": {}
                    }
                }
            }
        ],
        "lastMessage": {
            "id": 7783,
            "caseId": 1684,
            "channel": "chat",
            "senderId": 597752,
            "senderType": "contact",
            "type": "event",
            "message": "You're being transferred to one of our agents, they'll be with you shortly.|translate",
            "dateCreated": "2021-03-24T10:44:35.000Z",
            "dateUpdated": null,
            "seen": "yes",
            "meta": {}
        }
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

**Body \(raw\)**

```text
{
    "caseId": 1684,
    "askJoin": true
}
```

