# Message List

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/objects/case-message?limit=20&relations=case&select=id&select=caseId&select=senderId&select=senderType&select=type&select=message&select=dateCreated&select=dateUpdated&select=seen&select=meta" path="" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
 Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="select" type="string" required=false %}
id\|caseId\|senderId\|senderType\|type\|  
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
        "page": 0,
        "offset": 0,
        "limit": 2,
        "count": 327,
        "data": [
            {
                "id": 1,
                "senderId": 1,
                "senderType": "contact",
                "type": "event",
                "message": "The visitor started chat.",
                "dateCreated": "2020-08-11T07:26:23.000Z",
                "seen": "yes",
                "meta": {},
                "case": {
                    "dateCreated": "2020-08-11T07:26:23.000Z",
                    "dateUpdated": "2020-08-11T07:26:28.000Z",
                    "id": 1,
                    "contactId": 1,
                    "closedBy": null,
                    "visitId": 1,
                    "title": "test : ",
                    "description": "",
                    "channel": "chat",
                    "status": "active",
                    "closingState": "handled",
                    "dateQueue": "2020-08-11T07:26:23.000Z",
                    "datePending": "2020-08-11T07:26:23.000Z",
                    "dateActive": "2020-08-11T07:26:28.000Z",
                    "dateClosed": null,
                    "queueId": null,
                    "queueOrder": null,
                    "meta": {
                        "_routes": {}
                    },
                    "parentId": null,
                    "userId": null,
                    "waitTime": 0,
                    "threadId": 1
                }
            },
            {
                "id": 2,
                "senderId": 1,
                "senderType": "contact",
                "type": "event",
                "message": "You're being transferred to one of our agents, they'll be with you shortly.",
                "dateCreated": "2020-08-11T07:26:23.000Z",
                "seen": "yes",
                "meta": {},
                "case": {
                    "dateCreated": "2020-08-11T07:26:23.000Z",
                    "dateUpdated": "2020-08-11T07:26:28.000Z",
                    "id": 1,
                    "contactId": 1,
                    "closedBy": null,
                    "visitId": 1,
                    "title": "test : ",
                    "description": "",
                    "channel": "chat",
                    "status": "active",
                    "closingState": "handled",
                    "dateQueue": "2020-08-11T07:26:23.000Z",
                    "datePending": "2020-08-11T07:26:23.000Z",
                    "dateActive": "2020-08-11T07:26:28.000Z",
                    "dateClosed": null,
                    "queueId": null,
                    "queueOrder": null,
                    "meta": {
                        "_routes": {}
                    },
                    "parentId": null,
                    "userId": null,
                    "waitTime": 0,
                    "threadId": 1
                }
            }
        ]
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

