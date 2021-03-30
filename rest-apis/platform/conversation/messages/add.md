---
description: API to add a new message
---

# Add

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/messenger/chat/add-message?-x-user-type=contact" path="" %}
{% api-method-summary %}
Add Message
{% endapi-method-summary %}

{% api-method-description %}
API to add a new message
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
        "channel": "chat",
        "senderType": "user",
        "senderId": 25,
        "type": "message",
        "seen": "no",
        "message": "Hey added from the api",
        "meta": {
            "additionalProp1": {}
        },
        "dateCreated": "2021-03-30T16:05:46.000Z",
        "case": {
            "dateCreated": "2021-03-30T16:04:10.000Z",
            "dateUpdated": "2021-03-30T16:04:11.000Z",
            "id": 2069,
            "closedBy": null,
            "visitId": 1379,
            "title": "#597759 has just started a chat",
            "description": "fdgdfgd",
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
            "contact": {
                "dateCreated": "2021-03-26T08:34:29.000Z",
                "dateUpdated": "2021-03-30T16:04:10.000Z",
                "id": 597759,
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
                        "type": "3g",
                        "speed": "2.3400000000000003"
                    }
                },
                "meta": {},
                "archive": "no",
                "companyId": null
            },
            "users": [
                {
                    "id": 4607,
                    "caseId": 2069,
                    "type": "user",
                    "userId": 1,
                    "role": "owner",
                    "status": "active",
                    "dateCreated": "2021-03-30T16:04:10.000Z",
                    "dateLastAssigned": "2021-03-30T16:04:10.000Z",
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
                },
                {
                    "id": 4606,
                    "caseId": 2069,
                    "type": "contact",
                    "userId": 597759,
                    "role": "owner",
                    "status": "active",
                    "dateCreated": "2021-03-30T16:04:10.000Z",
                    "dateLastAssigned": "2021-03-30T16:04:10.000Z",
                    "closed": "no",
                    "meta": null,
                    "user": {
                        "type": "contact",
                        "id": 597759,
                        "name": "#597759",
                        "photo": null
                    }
                }
            ],
            "threadId": 1875
        },
        "sender": {
            "roles": [],
            "id": 25,
            "name": "a",
            "firstName": "a",
            "lastName": "",
            "photo": "",
            "email": "",
            "clientId": "",
            "meta": {
                "fields": {
                    "type": {
                        "stringValue": "fullAccess",
                        "kind": "stringValue"
                    },
                    "value": {
                        "structValue": {
                            "fields": {
                                "bot": {
                                    "listValue": {
                                        "values": [
                                            {
                                                "stringValue": "home",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "conversational-bot",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "sequence-bot",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "configurations",
                                                "kind": "stringValue"
                                            }
                                        ]
                                    },
                                    "kind": "listValue"
                                },
                                "chat": {
                                    "listValue": {
                                        "values": [
                                            {
                                                "stringValue": "cobrowse",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "screen-share",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "video-calls",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "audio-calls",
                                                "kind": "stringValue"
                                            }
                                        ]
                                    },
                                    "kind": "listValue"
                                },
                                "voIP": {
                                    "listValue": {
                                        "values": [
                                            {
                                                "stringValue": "default",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "event",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "setup",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "setting",
                                                "kind": "stringValue"
                                            }
                                        ]
                                    },
                                    "kind": "listValue"
                                },
                                "email": {
                                    "listValue": {
                                        "values": [
                                            {
                                                "stringValue": "inbox",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "template",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "smtp",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "signature",
                                                "kind": "stringValue"
                                            }
                                        ]
                                    },
                                    "kind": "listValue"
                                },
                                "media": {
                                    "listValue": {
                                        "values": [
                                            {
                                                "stringValue": "media",
                                                "kind": "stringValue"
                                            }
                                        ]
                                    },
                                    "kind": "listValue"
                                },
                                "settings": {
                                    "listValue": {
                                        "values": [
                                            {
                                                "stringValue": "web-widget",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "account-settings",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "profile",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "users",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "roles",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "departments",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "apps",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "custom-attributes",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "shortcuts",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "tags",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "feedbacks",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "audit-logs",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "spam",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "translations",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "api-keys",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "webhooks",
                                                "kind": "stringValue"
                                            }
                                        ]
                                    },
                                    "kind": "listValue"
                                },
                                "triggers": {
                                    "listValue": {
                                        "values": [
                                            {
                                                "stringValue": "business-rules",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "triggers",
                                                "kind": "stringValue"
                                            }
                                        ]
                                    },
                                    "kind": "listValue"
                                },
                                "analytics": {
                                    "listValue": {
                                        "values": [
                                            {
                                                "stringValue": "agent",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "app",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "bot",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "chat",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "custom-reporting",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "feedback",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "general",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "kb",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "liveDashboard",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "mail",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "voip",
                                                "kind": "stringValue"
                                            }
                                        ]
                                    },
                                    "kind": "listValue"
                                },
                                "app-store": {
                                    "listValue": {
                                        "values": [
                                            {
                                                "stringValue": "home",
                                                "kind": "stringValue"
                                            }
                                        ]
                                    },
                                    "kind": "listValue"
                                },
                                "dashboard": {
                                    "listValue": {
                                        "values": [
                                            {
                                                "stringValue": "contact-list",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "messenger",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "company",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "delete-conversation",
                                                "kind": "stringValue"
                                            }
                                        ]
                                    },
                                    "kind": "listValue"
                                },
                                "access-level": {
                                    "listValue": {
                                        "values": [
                                            {
                                                "stringValue": "account",
                                                "kind": "stringValue"
                                            }
                                        ]
                                    },
                                    "kind": "listValue"
                                },
                                "knowledge-base": {
                                    "listValue": {
                                        "values": [
                                            {
                                                "stringValue": "kb-setup",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "add",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "edit",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "delete",
                                                "kind": "stringValue"
                                            },
                                            {
                                                "stringValue": "edit-theme",
                                                "kind": "stringValue"
                                            }
                                        ]
                                    },
                                    "kind": "listValue"
                                },
                                "cobrowse-access-url": {
                                    "listValue": {
                                        "values": []
                                    },
                                    "kind": "listValue"
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
        "dateUpdated": null,
        "id": 8289,
        "caseId": 2069,
        "threadId": 1875,
        "contactId": 597759
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
  "channel": "chat",
  "mentionUsers": [
    "00"
  ],
  "meta": {
    "additionalProp1": {}
  },
  "message": {
    "type": "message",
    "message": "Hey added from the api",
    "translateLangKey": "en"
  },
  "delay": 1000,
  "caseId": 2069
}
```

