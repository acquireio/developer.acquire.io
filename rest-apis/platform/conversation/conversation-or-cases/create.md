---
description: API to create a new case
---

# Create

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/messenger/chat/create?contactId={{contactId}}" path="" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Create a case. The **contactId** must be passed in to the endpoint as a query parameter. The body is optional.   
  
**contactId** - the contact's ID. Send a GET request to List all contacts to retrieve a list of contacts and their IDs or log in to your Acquire platform and hover over the contact's name in `Contact List`. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="contactId" type="integer" required=true %}
Contact's ID. All cases must have a contactId. 
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
        "title": "string",
        "description": "I'm reopening the closed case",
        "channel": "chat",
        "contact": {
            "dateCreated": "2021-03-24T10:06:57.000Z",
            "dateUpdated": "2021-03-30T18:21:41.353Z",
            "id": 597752,
            "clientType": "web",
            "clientName": "Chrome",
            "clientVersion": "87.0",
            "clientOsName": "Linux",
            "clientOsVersion": "x86_64",
            "clientDeviceType": "Desktop",
            "clientDeviceVendor": null,
            "clientDeviceModel": null,
            "clientDetails": {
                "ua": "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/87.0.4280.66 Safari/537.36",
                "engine": {
                    "name": "Blink",
                    "version": "87.0.4280.66"
                },
                "network": {
                    "type": "4g",
                    "speed": "1.71"
                }
            },
            "archive": "no",
            "fields": [
                {
                    "value": null,
                    "owner": "contact",
                    "contactId": 597752,
                    "field": {
                        "id": 1,
                        "object": "contact",
                        "key": "name",
                        "type": "text",
                        "config": {
                            "input": {
                                "type": "text",
                                "label": "Name",
                                "required": false,
                                "placeholder": "",
                                "validationType": "format",
                                "validationFormat": "any",
                                "requiredErrorMessage": "Unfortunately this cannot be blank.",
                                "validationErrorMessage": "Oops! Seems incorrect format that you entered. Can you please recheck your name?"
                            },
                            "label": "Name",
                            "backend": {
                                "list": false
                            },
                            "capture": [
                                "api",
                                "chat-online-pre"
                            ],
                            "online_order": 9,
                            "offline_order": 8494
                        },
                        "system": "yes"
                    }
                },
                {
                    "value": null,
                    "owner": "contact",
                    "contactId": 597752,
                    "field": {
                        "id": 2,
                        "object": "contact",
                        "key": "email",
                        "type": "text",
                        "config": {
                            "input": {
                                "type": "text",
                                "label": "Email!!!!",
                                "required": false,
                                "placeholder": "",
                                "validationType": "format",
                                "validationFormat": "email",
                                "requiredErrorMessage": "Unfortunately this cannot be blank.",
                                "validationErrorMessage": "Oops! Looks like format you entered is wrong. Can you please recheck your email?"
                            },
                            "label": "Email!!!!",
                            "backend": {
                                "list": false
                            },
                            "capture": [
                                "api",
                                "chat-online-pre"
                            ],
                            "online_order": 4,
                            "offline_order": 8492
                        },
                        "system": "yes"
                    }
                },
                {
                    "value": "",
                    "owner": "contact",
                    "contactId": 597752,
                    "field": {
                        "id": 5,
                        "object": "contact",
                        "key": "city",
                        "type": "text",
                        "config": {
                            "input": {
                                "type": "text",
                                "label": "city",
                                "required": false,
                                "placeholder": "",
                                "validationType": "format",
                                "validationFormat": "any",
                                "requiredErrorMessage": "Unfortunately this cannot be blank.",
                                "validationErrorMessage": "Oops! Look like you entered the wrong value."
                            },
                            "label": "city",
                            "backend": {
                                "list": false
                            },
                            "capture": [
                                "api"
                            ],
                            "online_order": 0,
                            "offline_order": 0,
                            "attributeInputDelay": 0
                        },
                        "system": "yes"
                    }
                },
                {
                    "value": "",
                    "owner": "contact",
                    "contactId": 597752,
                    "field": {
                        "id": 6,
                        "object": "contact",
                        "key": "state",
                        "type": "text",
                        "config": {
                            "backend": {
                                "list": false
                            },
                            "capture": [
                                "api"
                            ]
                        },
                        "system": "yes"
                    }
                },
                {
                    "value": "517",
                    "owner": "contact",
                    "contactId": 597752,
                    "field": {
                        "id": 7,
                        "object": "contact",
                        "key": "countryId",
                        "type": "text",
                        "config": {
                            "backend": {
                                "list": false
                            },
                            "capture": [
                                "api"
                            ]
                        },
                        "system": "yes"
                    }
                },
                {
                    "value": "2402:8100:21f5:3d13:d9da:18ea:aa28:f778",
                    "owner": "contact",
                    "contactId": 597752,
                    "field": {
                        "id": 8,
                        "object": "contact",
                        "key": "ip",
                        "type": "text",
                        "config": {
                            "input": {
                                "type": "text",
                                "label": "ip",
                                "required": true,
                                "placeholder": "",
                                "validationType": "format",
                                "validationFormat": "any",
                                "requiredErrorMessage": "Unfortunately this cannot be blank.",
                                "validationErrorMessage": "Oops! I don't understand that."
                            },
                            "label": "ip",
                            "backend": {
                                "list": false
                            },
                            "capture": [],
                            "online_order": 8489,
                            "offline_order": 8490,
                            "attributeInputDelay": 0
                        },
                        "system": "yes"
                    }
                }
            ],
            "company": null,
            "tags": [],
            "visits": [
                {
                    "id": 1367,
                    "contactId": 597752,
                    "title": "Acquire | Test Simulate Page",
                    "url": "https://5mkg3t.uat.env.acquire.io/simulate",
                    "source": "",
                    "dateCreated": "2021-03-24T10:06:57.000Z"
                },
                {
                    "id": 1368,
                    "contactId": 597752,
                    "title": "Acquire | Test Simulate Page",
                    "url": "https://5mkg3t.uat.env.acquire.io/simulate",
                    "source": "",
                    "dateCreated": "2021-03-24T10:31:15.000Z"
                },
                {
                    "id": 1369,
                    "contactId": 597752,
                    "title": "Acquire | Test Simulate Page",
                    "url": "https://5mkg3t.uat.env.acquire.io/simulate",
                    "source": "",
                    "dateCreated": "2021-03-24T10:42:13.000Z"
                },
                {
                    "id": 1370,
                    "contactId": 597752,
                    "title": "Acquire | Test Simulate Page",
                    "url": "https://5mkg3t.uat.env.acquire.io/simulate",
                    "source": "",
                    "dateCreated": "2021-03-24T10:43:01.000Z"
                },
                {
                    "id": 1371,
                    "contactId": 597752,
                    "title": "Acquire | Test Simulate Page",
                    "url": "https://5mkg3t.uat.env.acquire.io/simulate",
                    "source": "",
                    "dateCreated": "2021-03-24T10:43:03.000Z"
                }
            ]
        },
        "status": "active",
        "dateQueue": "2021-03-30T18:21:41.338Z",
        "dateCreated": "2021-03-30T18:21:41.000Z",
        "datePending": null,
        "dateActive": null,
        "visitId": 1371,
        "users": [],
        "parentId": 1683,
        "userId": 25,
        "dateUpdated": null,
        "closedBy": null,
        "closingState": null,
        "dateClosed": null,
        "id": 2071,
        "threadId": 1683,
        "fields": [],
        "isCaseJoined": false,
        "timelineId": 1604,
        "preMessages": []
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
  "title": "string",
  "source": "firstMessage",
  "mentionUsers": [
    "00"
  ],
  "message": {
    "type": "message",
    "message": "I'm reopening the closed case",
    "translateLangKey": ""
  },
  "channel": "chat",
  "routeAgentId": 0,
  "agentId": 0,
  "isFromCobrowse": true,
  "fields": {}
}
```



