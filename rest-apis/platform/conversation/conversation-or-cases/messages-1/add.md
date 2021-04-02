---
description: API to add a new message
---

# Send a message

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/messenger/chat/add-message" path="" %}
{% api-method-summary %}
Send Chat Message
{% endapi-method-summary %}

{% api-method-description %}
Send a chat message to a conversation. To send a message to a contact, you must pass a `"message"` object. Only active cases may receive messages via the API.  
  
`"type"`, `"message"`, ****and ****`"caseId"` are required keys in the message object. See example body below. You can also add `translateLangKey` to the message object for message translation.  
  
**caseId** - You can retrieve caseId from a Webhook or from the conversation or chat API or from the Acquire Dashboard.  
  
**Type** - This indicates the type of message. There are three options: message, note, and event. Set `"type"` to `"message"` to send a chat message.  
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="translateLangKey" type="string" required=false %}
HTML ISO language code
{% endapi-method-parameter %}

{% api-method-parameter name="caseId" type="integer" required=true %}
The case ID
{% endapi-method-parameter %}

{% api-method-parameter name="message" type="string" required=false %}
The chat message you would like to send.
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
"message" 
{% endapi-method-parameter %}

{% api-method-parameter name="message" type="object" required=true %}
message object
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
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

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/mail/add-message" path="" %}
{% api-method-summary %}
Send Mail Message
{% endapi-method-summary %}

{% api-method-description %}
Send an email message. You must have an inbox connected to your Acquire account. The case \(`"caseId"`\) must have its channel set to email.  A `"data"` object with  `"caseId"`, `"contactId"`, `"to"`, `"from"`,  and  a key of `"type"` set to `"message"` are required body attributes. See body example below.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="htmlBody" type="string" required=false %}
the email message
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
"message"
{% endapi-method-parameter %}

{% api-method-parameter name="subject" type="string" required=false %}
the subject of the email
{% endapi-method-parameter %}

{% api-method-parameter name="bcc" type="array" required=false %}
blind carbon copy email addresses
{% endapi-method-parameter %}

{% api-method-parameter name="cc" type="array" required=false %}
carbon copy email addresses
{% endapi-method-parameter %}

{% api-method-parameter name="from" type="string" required=true %}
your Acquire-connected email address
{% endapi-method-parameter %}

{% api-method-parameter name="to" type="array" required=true %}
an array of recipients' email addresses
{% endapi-method-parameter %}

{% api-method-parameter name="contactId" type="integer" required=true %}
the contact's ID
{% endapi-method-parameter %}

{% api-method-parameter name="caseId" type="integer" required=true %}
the cases' ID
{% endapi-method-parameter %}

{% api-method-parameter name="data" type="object" required=true %}
data object
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "data": {
        "id": 407,
        "caseMessageId": 407,
        "channelId": null,
        "caseId": 90,
        "inboxId": 1,
        "mailId": 1,
        "type": "message",
        "senderType": "user",
        "senderId": 93,
        "to": [
            {
                "Name": "",
                "Email": "developer@acquire.io"
            }
        ],
        "from": {
            "Name": "test",
            "Email": "surendra@acquire.io",
            "MailboxHash": ""
        },
        "cc": [],
        "bcc": [],
        "reply_to": null,
        "subject": "test",
        "textBody": "test api email\n\nOn Mon, Sep 14 2020, at 05:00 PM<\"surendra@acquire.io\"> wrote:test\n\nOn Mon, Sep 14 2020, at 04:36 PM<\"surendra@acquire.io\"> wrote:yrety",
        "htmlBody": "<div class=\"content-writer\" data-reactroot=\"\">test api email</div><div class=\"acq-content hide\" data-reactroot=\"\"><br><br><div>On Mon, Sep 14 2020, at 05:00 PM&lt;\"surendra@acquire.io\"&gt; wrote:</div><blockquote><div class=\"content-writer\" data-reactroot=\"\">test</div><div class=\"acq-content hide\" data-reactroot=\"\"><br><br><div>On Mon, Sep 14 2020, at 04:36 PM&lt;\"surendra@acquire.io\"&gt; wrote:</div><blockquote>yrety</blockquote></div></blockquote></div>",
        "mailboxMessageId": "0.5345358743514836",
        "messageId": null,
        "mailboxInReplyTo": "<c89eb634-612c-45af-8edf-7e06d425833f@mtasv.net>",
        "originalRecipient": "developer@acquire.io",
        "parentId": 14,
        "attachments": [],
        "dateCreated": "2021-03-12T09:21:20.000Z",
        "dateSeen": null,
        "dateBounce": null,
        "dateFailed": null,
        "dateDelivery": null,
        "seen": "no",
        "isDraft": "no",
        "scheduleAt": "2021-03-12T09:21:20.000Z",
        "meta": null,
        "clickedDate": null,
        "unsubscribeDate": null,
        "appMessageId": null,
        "appThreadId": null,
        "user": {
            "departments": [],
            "roles": [],
            "id": 93,
            "name": "test",
            "firstName": "test",
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
        "sender": {
            "type": "user",
            "id": 93,
            "name": "test",
            "email": "",
            "photo": ""
        },
        "mailMsgId": 13
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
    "data": {
        "caseId": 575,
        "to": [
            "test@gmail.com"
        ],
        "from": "user@acquire.io",
        "cc": [],
        "bcc": [],
        "subject": "test",
        "contactId": 597632,
        "type": "message", 
        "htmlBody": "This is the message body"
    }
}
```

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/voip/send-sms" path="" %}
{% api-method-summary %}
Send SMS
{% endapi-method-summary %}

{% api-method-description %}
API to send a message through sms channel
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
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
    "cas": {
      "dateCreated": "2021-04-01T16:31:44.000Z",
      "dateUpdated": "2021-04-01T16:31:48.000Z",
      "id": 2219,
      "contactId": 751069,
      "closedBy": null,
      "visitId": 1424,
      "title": "#751069 has just started a chat",
      "description": "This thread has been reactivated.|translate",
      "channel": "chat",
      "status": "active",
      "closingState": "handled",
      "dateQueue": "2021-04-01T16:31:44.000Z",
      "datePending": "2021-04-01T16:31:44.000Z",
      "dateActive": "2021-04-01T16:31:44.000Z",
      "dateClosed": null,
      "queueId": null,
      "queueOrder": null,
      "meta": {
        "contact": {
          "id": 751069,
          "meta": {},
          "fields": {
            "ip": "2402:8100:21f3:1066:2ced:44dd:d071:88a3",
            "city": "",
            "phone": "919666929552",
            "state": "",
            "country": {
              "lat": "38",
              "lng": "-97",
              "cca2": "US",
              "cca3": "USA",
              "ccn3": "84",
              "name": "United States",
              "region_id": 496,
              "voip_enable": true,
              "calling_code1": 1,
              "name_official": "United States of America"
            },
            "countryId": "517"
          },
          "archive": "no",
          "companyId": null,
          "clientName": "Chrome",
          "clientType": "web",
          "dateCreated": "2021-04-01T13:10:25.000Z",
          "dateUpdated": "2021-04-01T16:31:44.000Z",
          "clientOsName": "Linux",
          "clientDetails": {
            "ua": "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/87.0.4280.66 Safari/537.36",
            "engine": {
              "name": "Blink",
              "version": "87.0.4280.66"
            },
            "network": {
              "type": "3g",
              "speed": "2.43"
            }
          },
          "clientVersion": "87.0",
          "clientOsVersion": "x86_64",
          "clientDeviceType": "Desktop",
          "clientDeviceModel": null,
          "clientDeviceVendor": null
        },
        "timeline": {
          "id": 2108,
          "meta": {},
          "caseId": 2219,
          "noteId": null,
          "viewId": null,
          "archive": "no",
          "threadId": 2207,
          "contactId": 751069,
          "objectType": "case",
          "dateCreated": "2021-04-01T13:11:02.000Z",
          "dateUpdated": "2021-04-01T16:31:44.000Z"
        },
        "is_new_contact": false
      },
      "parentId": 2207,
      "userId": null,
      "waitTime": 0,
      "users": [
        {
          "id": 6240,
          "caseId": 2219,
          "type": "user",
          "userId": 28,
          "role": "owner",
          "status": "active",
          "dateCreated": "2021-04-01T16:31:44.000Z",
          "dateLastAssigned": "2021-04-01T16:31:44.000Z",
          "closed": "no",
          "meta": null,
          "user": {
            "roles": [],
            "id": 28,
            "name": "myuser",
            "firstName": "myuser",
            "lastName": "",
            "photo": "",
            "email": "myuser@acquire.io",
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
                }
              }
            },
            "parentId": 0,
            "type": "user",
            "accessLevel": null
          }
        },
        {
          "id": 6239,
          "caseId": 2219,
          "type": "contact",
          "userId": 751069,
          "role": "owner",
          "status": "active",
          "dateCreated": "2021-04-01T16:31:44.000Z",
          "dateLastAssigned": "2021-04-01T16:31:44.000Z",
          "closed": "no",
          "meta": null,
          "user": {
            "type": "contact",
            "id": 751069,
            "name": "#751069",
            "photo": null
          }
        }
      ],
      "timeline": {
        "id": 2108,
        "objectType": "case",
        "caseId": 2219,
        "viewId": null,
        "noteId": null,
        "threadId": 2207,
        "dateCreated": "2021-04-01T13:11:02.000Z",
        "dateUpdated": "2021-04-01T16:31:48.000Z",
        "contactId": 751069,
        "archive": "no",
        "meta": {}
      },
      "threadId": 2207
    },
    "threadId": 2219,
    "timeline": {
      "id": 2108,
      "objectType": "case",
      "threadId": 2207,
      "dateCreated": "2021-04-01T13:11:02.000Z",
      "dateUpdated": "2021-04-01T16:35:05.000Z",
      "contactId": 751069,
      "archive": "no",
      "meta": {},
      "case": {
        "dateCreated": "2021-04-01T16:31:44.000Z",
        "dateUpdated": "2021-04-01T16:35:05.000Z",
        "id": 2219,
        "contactId": 751069,
        "closedBy": null,
        "visitId": 1424,
        "title": "#751069 has just started a chat",
        "description": "This thread has been reactivated.|translate",
        "channel": "chat",
        "status": "active",
        "closingState": "handled",
        "dateQueue": "2021-04-01T16:31:44.000Z",
        "datePending": "2021-04-01T16:31:44.000Z",
        "dateActive": "2021-04-01T16:31:44.000Z",
        "dateClosed": null,
        "queueId": null,
        "queueOrder": null,
        "meta": {
          "contact": {
            "id": 751069,
            "meta": {},
            "fields": {
              "ip": "2402:8100:21f3:1066:2ced:44dd:d071:88a3",
              "city": "",
              "phone": "919666929552",
              "state": "",
              "country": {
                "lat": "38",
                "lng": "-97",
                "cca2": "US",
                "cca3": "USA",
                "ccn3": "84",
                "name": "United States",
                "region_id": 496,
                "voip_enable": true,
                "calling_code1": 1,
                "name_official": "United States of America"
              },
              "countryId": "517"
            },
            "archive": "no",
            "companyId": null,
            "clientName": "Chrome",
            "clientType": "web",
            "dateCreated": "2021-04-01T13:10:25.000Z",
            "dateUpdated": "2021-04-01T16:31:44.000Z",
            "clientOsName": "Linux",
            "clientDetails": {
              "ua": "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/87.0.4280.66 Safari/537.36",
              "engine": {
                "name": "Blink",
                "version": "87.0.4280.66"
              },
              "network": {
                "type": "3g",
                "speed": "2.43"
              }
            },
            "clientVersion": "87.0",
            "clientOsVersion": "x86_64",
            "clientDeviceType": "Desktop",
            "clientDeviceModel": null,
            "clientDeviceVendor": null
          },
          "timeline": {
            "id": 2108,
            "meta": {},
            "caseId": 2219,
            "noteId": null,
            "viewId": null,
            "archive": "no",
            "threadId": 2207,
            "contactId": 751069,
            "objectType": "case",
            "dateCreated": "2021-04-01T13:11:02.000Z",
            "dateUpdated": "2021-04-01T16:31:44.000Z"
          },
          "is_new_contact": false
        },
        "parentId": 2207,
        "userId": null,
        "waitTime": 0,
        "users": [
          {
            "id": 6240,
            "caseId": 2219,
            "type": "user",
            "userId": 28,
            "role": "owner",
            "status": "active",
            "dateCreated": "2021-04-01T16:31:44.000Z",
            "dateLastAssigned": "2021-04-01T16:31:44.000Z",
            "closed": "no",
            "meta": null,
            "user": {
              "roles": [],
              "id": 28,
              "name": "myuser",
              "firstName": "myuser",
              "lastName": "",
              "photo": "",
              "email": "myuser@acquire.io",
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
                  }
                }
              },
              "parentId": 0,
              "type": "user",
              "accessLevel": null
            }
          },
          {
            "id": 6239,
            "caseId": 2219,
            "type": "contact",
            "userId": 751069,
            "role": "owner",
            "status": "active",
            "dateCreated": "2021-04-01T16:31:44.000Z",
            "dateLastAssigned": "2021-04-01T16:31:44.000Z",
            "closed": "no",
            "meta": null,
            "user": {
              "type": "contact",
              "id": 751069,
              "name": "#751069",
              "photo": null
            }
          },
          {
            "id": 6214,
            "caseId": 2207,
            "type": "user",
            "userId": 1,
            "role": "owner",
            "status": "rejected",
            "dateCreated": "2021-04-01T13:15:06.000Z",
            "dateLastAssigned": "2021-04-01T13:15:06.000Z",
            "closed": "yes",
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
            "id": 6213,
            "caseId": 2207,
            "type": "user",
            "userId": 28,
            "role": "owner",
            "status": "assigned",
            "dateCreated": "2021-04-01T13:11:02.000Z",
            "dateLastAssigned": "2021-04-01T13:11:02.000Z",
            "closed": "no",
            "meta": null,
            "user": {
              "roles": [],
              "id": 28,
              "name": "myuser",
              "firstName": "myuser",
              "lastName": "",
              "photo": "",
              "email": "myuser@acquire.io",
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
                  }
                }
              },
              "parentId": 0,
              "type": "user",
              "accessLevel": null
            }
          },
          {
            "id": 6212,
            "caseId": 2207,
            "type": "contact",
            "userId": 751069,
            "role": "owner",
            "status": "active",
            "dateCreated": "2021-04-01T13:11:02.000Z",
            "dateLastAssigned": "2021-04-01T13:11:02.000Z",
            "closed": "no",
            "meta": null,
            "user": {
              "type": "contact",
              "id": 751069,
              "name": "#751069",
              "photo": null
            }
          },
          {
            "id": 6217,
            "caseId": 2208,
            "type": "user",
            "userId": 1,
            "role": "owner",
            "status": "rejected",
            "dateCreated": "2021-04-01T13:20:05.000Z",
            "dateLastAssigned": "2021-04-01T13:20:05.000Z",
            "closed": "yes",
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
            "id": 6216,
            "caseId": 2208,
            "type": "user",
            "userId": 28,
            "role": "owner",
            "status": "assigned",
            "dateCreated": "2021-04-01T13:15:56.000Z",
            "dateLastAssigned": "2021-04-01T13:15:57.000Z",
            "closed": "no",
            "meta": null,
            "user": {
              "roles": [],
              "id": 28,
              "name": "myuser",
              "firstName": "myuser",
              "lastName": "",
              "photo": "",
              "email": "myuser@acquire.io",
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
                  }
                }
              },
              "parentId": 0,
              "type": "user",
              "accessLevel": null
            }
          },
          {
            "id": 6215,
            "caseId": 2208,
            "type": "contact",
            "userId": 751069,
            "role": "owner",
            "status": "active",
            "dateCreated": "2021-04-01T13:15:56.000Z",
            "dateLastAssigned": "2021-04-01T13:15:56.000Z",
            "closed": "no",
            "meta": null,
            "user": {
              "type": "contact",
              "id": 751069,
              "name": "#751069",
              "photo": null
            }
          },
          {
            "id": 6220,
            "caseId": 2209,
            "type": "user",
            "userId": 1,
            "role": "owner",
            "status": "rejected",
            "dateCreated": "2021-04-01T13:35:05.000Z",
            "dateLastAssigned": "2021-04-01T13:35:05.000Z",
            "closed": "yes",
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
            "id": 6219,
            "caseId": 2209,
            "type": "user",
            "userId": 28,
            "role": "owner",
            "status": "assigned",
            "dateCreated": "2021-04-01T13:31:22.000Z",
            "dateLastAssigned": "2021-04-01T13:31:23.000Z",
            "closed": "no",
            "meta": null,
            "user": {
              "roles": [],
              "id": 28,
              "name": "myuser",
              "firstName": "myuser",
              "lastName": "",
              "photo": "",
              "email": "myuser@acquire.io",
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
                  }
                }
              },
              "parentId": 0,
              "type": "user",
              "accessLevel": null
            }
          },
          {
            "id": 6218,
            "caseId": 2209,
            "type": "contact",
            "userId": 751069,
            "role": "owner",
            "status": "active",
            "dateCreated": "2021-04-01T13:31:22.000Z",
            "dateLastAssigned": "2021-04-01T13:31:22.000Z",
            "closed": "no",
            "meta": null,
            "user": {
              "type": "contact",
              "id": 751069,
              "name": "#751069",
              "photo": null
            }
          }
        ],
        "fields": {},
        "threadId": 2207,
        "lastMessage": {
          "id": 8651,
          "caseId": 2219,
          "channel": "chat",
          "senderId": 28,
          "senderType": "user",
          "type": "event",
          "message": "This thread has been reactivated.|translate",
          "dateCreated": "2021-04-01T16:31:44.000Z",
          "dateUpdated": null,
          "seen": "yes",
          "meta": {}
        },
        "tags": [],
        "channels": [
          "voip"
        ],
        "msgUnread": 0
      },
      "note": null,
      "view": null,
      "snooze": []
    },
    "data": {
      "members": [],
      "message": "SMS by myuser",
      "msgType": "sms",
      "channelType": "voip",
      "attachments": [],
      "id": 339,
      "caseId": 2219,
      "from": "+12513188609",
      "to": "+919666929552",
      "voip_account_id": 3,
      "senderType": "user",
      "senderId": 28,
      "type": "sms",
      "recording_status": null,
      "meta": {
        "To": "+919666929552",
        "to": "+919666929552",
        "SMS": "hi",
        "sid": "SMf7dc149c12e54cbd9864d543ac8bd041",
        "uri": "/2010-04-01/Accounts/ACf83886e81f434fe02812d132ab8790ce/Messages/SMf7dc149c12e54cbd9864d543ac8bd041.json",
        "Body": "hi",
        "From": "+12513188609",
        "body": "hi",
        "from": "+12513188609",
        "price": null,
        "status": "queued",
        "dateSent": null,
        "numMedia": "0",
        "MediaMeta": [],
        "direction": "outbound-api",
        "errorCode": null,
        "priceUnit": "USD",
        "accountSid": "ACf83886e81f434fe02812d132ab8790ce",
        "apiVersion": "2010-04-01",
        "dateCreated": "2021-04-01T16:35:05.000Z",
        "dateUpdated": "2021-04-01T16:35:05.000Z",
        "numSegments": "1",
        "errorMessage": null,
        "subresourceUris": {
          "media": "/2010-04-01/Accounts/ACf83886e81f434fe02812d132ab8790ce/Messages/SMf7dc149c12e54cbd9864d543ac8bd041/Media.json"
        },
        "messagingServiceSid": null
      },
      "call_transcript": 0,
      "caseMessageId": 8653,
      "timelineId": 2108,
      "contactId": 751069,
      "seen": "yes",
      "dateCreated": "2021-04-01T16:35:05.000Z",
      "call_answered": null,
      "call_end": null,
      "call_sid": "SMf7dc149c12e54cbd9864d543ac8bd041",
      "status": "sent",
      "call_status": null,
      "conferenceId": null,
      "price": "0",
      "sender": {
        "departments": [],
        "roles": [],
        "id": 28,
        "name": "myuser",
        "firstName": "myuser",
        "lastName": "",
        "photo": "",
        "email": "myuser@acquire.io",
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
            }
          }
        },
        "parentId": 0,
        "metaDetails": {
          "isBotClient": false,
          "label": ""
        },
        "type": "user",
        "accessLevel": null
      },
      "is_new_case": false,
      "is_new_contact": false,
      "cas": {
        "dateCreated": "2021-04-01T16:31:44.000Z",
        "dateUpdated": "2021-04-01T16:35:05.000Z",
        "id": 2219,
        "contactId": 751069,
        "closedBy": null,
        "visitId": 1424,
        "title": "#751069 has just started a chat",
        "description": "This thread has been reactivated.|translate",
        "channel": "chat",
        "status": "active",
        "closingState": "handled",
        "dateQueue": "2021-04-01T16:31:44.000Z",
        "datePending": "2021-04-01T16:31:44.000Z",
        "dateActive": "2021-04-01T16:31:44.000Z",
        "dateClosed": null,
        "queueId": null,
        "queueOrder": null,
        "meta": {
          "contact": {
            "id": 751069,
            "meta": {},
            "fields": {
              "ip": "2402:8100:21f3:1066:2ced:44dd:d071:88a3",
              "city": "",
              "phone": "919666929552",
              "state": "",
              "country": {
                "lat": "38",
                "lng": "-97",
                "cca2": "US",
                "cca3": "USA",
                "ccn3": "84",
                "name": "United States",
                "region_id": 496,
                "voip_enable": true,
                "calling_code1": 1,
                "name_official": "United States of America"
              },
              "countryId": "517"
            },
            "archive": "no",
            "companyId": null,
            "clientName": "Chrome",
            "clientType": "web",
            "dateCreated": "2021-04-01T13:10:25.000Z",
            "dateUpdated": "2021-04-01T16:31:44.000Z",
            "clientOsName": "Linux",
            "clientDetails": {
              "ua": "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/87.0.4280.66 Safari/537.36",
              "engine": {
                "name": "Blink",
                "version": "87.0.4280.66"
              },
              "network": {
                "type": "3g",
                "speed": "2.43"
              }
            },
            "clientVersion": "87.0",
            "clientOsVersion": "x86_64",
            "clientDeviceType": "Desktop",
            "clientDeviceModel": null,
            "clientDeviceVendor": null
          },
          "timeline": {
            "id": 2108,
            "meta": {},
            "caseId": 2219,
            "noteId": null,
            "viewId": null,
            "archive": "no",
            "threadId": 2207,
            "contactId": 751069,
            "objectType": "case",
            "dateCreated": "2021-04-01T13:11:02.000Z",
            "dateUpdated": "2021-04-01T16:31:44.000Z"
          },
          "is_new_contact": false
        },
        "parentId": 2207,
        "userId": null,
        "waitTime": 0,
        "users": [
          {
            "id": 6240,
            "caseId": 2219,
            "type": "user",
            "userId": 28,
            "role": "owner",
            "status": "active",
            "dateCreated": "2021-04-01T16:31:44.000Z",
            "dateLastAssigned": "2021-04-01T16:31:44.000Z",
            "closed": "no",
            "meta": null,
            "user": {
              "roles": [],
              "id": 28,
              "name": "myuser",
              "firstName": "myuser",
              "lastName": "",
              "photo": "",
              "email": "myuser@acquire.io",
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
                  }
                }
              },
              "parentId": 0,
              "type": "user",
              "accessLevel": null
            }
          },
          {
            "id": 6239,
            "caseId": 2219,
            "type": "contact",
            "userId": 751069,
            "role": "owner",
            "status": "active",
            "dateCreated": "2021-04-01T16:31:44.000Z",
            "dateLastAssigned": "2021-04-01T16:31:44.000Z",
            "closed": "no",
            "meta": null,
            "user": {
              "type": "contact",
              "id": 751069,
              "name": "#751069",
              "photo": null
            }
          }
        ],
        "timeline": {
          "id": 2108,
          "objectType": "case",
          "caseId": 2219,
          "viewId": null,
          "noteId": null,
          "threadId": 2207,
          "dateCreated": "2021-04-01T13:11:02.000Z",
          "dateUpdated": "2021-04-01T16:35:05.000Z",
          "contactId": 751069,
          "archive": "no",
          "meta": {}
        },
        "threadId": 2207
      },
      "case_id": 2219,
      "timeline": {
        "id": 2108,
        "objectType": "case",
        "caseId": 2219,
        "viewId": null,
        "noteId": null,
        "threadId": 2207,
        "dateCreated": "2021-04-01T13:11:02.000Z",
        "dateUpdated": "2021-04-01T16:35:05.000Z",
        "contactId": 751069,
        "archive": "no",
        "meta": {}
      },
      "is_case_join": false
    }
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
    "Body": "hi",
    "From": "+12513188609",
    "To": "919666929552",
    "contactId": 751069,
    "id": 2219,
    "isClosed": false,
    "isMultiChannel": false,
    "markValue": "<p>hi</p>",
    "message": "hi",
    "msgType": "message",
    "sms": "hi",
    "threadId": 2219,
    "timelineId": 2108,
    "title": "#751069 has just started a chat"
}
```

