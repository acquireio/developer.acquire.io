---
description: Retrieve a list of messages.
---

# Retrieve a list of messages

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/messenger/chat/messages" path="" %}
{% api-method-summary %}
Get message List
{% endapi-method-summary %}

{% api-method-description %}
Retrieve a list of messages. The following query parameters must be present: **threadId** and **contactId**.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="-x-user-type" type="string" required=false %}
Send this parameter with a value of "contact" to send messages to Acquire.
{% endapi-method-parameter %}

{% api-method-parameter name="threadId" type="integer" required=true %}
ID of the thread.
{% endapi-method-parameter %}

{% api-method-parameter name="contactId" type="integer" required=true %}
ID of the customer/contact.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "data": [
        {
            "dateCreated": "2021-04-13T05:22:19.000Z",
            "dateUpdated": "2021-04-13T12:17:02.000Z",
            "id": 854,
            "contactId": 750940,
            "closedBy": null,
            "visitId": 222,
            "title": "#750940  : hi",
            "description": "lk",
            "channel": "chat",
            "status": "active",
            "closingState": "handled",
            "dateQueue": "2021-04-13T05:22:19.000Z",
            "datePending": "2021-04-13T05:22:19.000Z",
            "dateActive": "2021-04-13T05:22:23.000Z",
            "dateClosed": null,
            "queueId": null,
            "queueOrder": 0,
            "parentId": null,
            "userId": null,
            "waitTime": 4,
            "cases": [],
            "users": [
                {
                    "id": 2126,
                    "caseId": 854,
                    "type": "user",
                    "userId": 12,
                    "role": "owner",
                    "status": "active",
                    "dateCreated": "2021-04-13T05:22:18.000Z",
                    "dateLastAssigned": "2021-04-13T05:22:19.000Z",
                    "closed": "no",
                    "meta": null,
                    "user": {
                        "roles": [],
                        "id": 12,
                        "name": "vivek",
                        "firstName": "vivek",
                        "lastName": "",
                        "photo": "",
                        "email": "vivek@acquire.io",
                        "clientId": "",
                        "parentId": 0,
                        "type": "user",
                        "accessLevel": null
                    }
                },
                {
                    "id": 2125,
                    "caseId": 854,
                    "type": "contact",
                    "userId": 750940,
                    "role": "owner",
                    "status": "active",
                    "dateCreated": "2021-04-13T05:22:18.000Z",
                    "dateLastAssigned": "2021-04-13T05:22:18.000Z",
                    "closed": "no",
                    "meta": null,
                    "user": {
                        "type": "contact",
                        "id": 750940,
                        "name": "#750940",
                        "photo": null
                    }
                }
            ],
            "threadId": 854,
            "lastMessage": {
                "id": 3391,
                "caseId": 854,
                "channel": "chat",
                "senderId": 12,
                "senderType": "user",
                "type": "message",
                "message": "lk",
                "dateCreated": "2021-04-13T12:17:02.000Z",
                "dateUpdated": null,
                "seen": "no",
                "meta": {}
            }
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

