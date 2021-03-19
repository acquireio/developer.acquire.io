---
description: API to get mail messages
---

# Mail Messages

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/mail/messages" path="" %}
{% api-method-summary %}
Mail Messages
{% endapi-method-summary %}

{% api-method-description %}
API to get mail messages
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
    "previous": "LTUy",
    "next": "KzUz",
    "messages": [
      {
        "id": 52,
        "caseMessageId": null,
        "channelId": null,
        "caseId": 489,
        "inboxId": 2,
        "mailId": 2,
        "type": "message",
        "senderType": "user",
        "senderId": 1,
        "to": [
          {
            "Name": ""
          }
        ],
        "from": {
          "Name": "",
          "Email": "viswanath.sarma@acquire.io"
        },
        "cc": [],
        "bcc": [],
        "reply_to": null,
        "subject": "( No Subject )",
        "textBody": "",
        "htmlBody": "",
        "mailboxMessageId": "0.0507382348570502",
        "messageId": null,
        "mailboxInReplyTo": null,
        "originalRecipient": null,
        "parentId": null,
        "attachments": [],
        "dateCreated": "2020-11-17T13:42:25.000Z",
        "dateSeen": null,
        "dateBounce": null,
        "dateFailed": null,
        "dateDelivery": null,
        "seen": "no",
        "isDraft": "yes",
        "scheduleAt": null,
        "meta": null,
        "clickedDate": null,
        "unsubscribeDate": null,
        "appMessageId": null,
        "appThreadId": null,
        "user": {
          "departments": [],
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
          "metaDetails": {
            "isBotClient": false,
            "label": ""
          },
          "type": "user",
          "accessLevel": null
        },
        "sender": {
          "type": "user",
          "id": 1,
          "name": "David Guetta",
          "email": "user@example.com",
          "photo": ""
        }
      },
      {
        "id": 53,
        "caseMessageId": 4394,
        "channelId": null,
        "caseId": 489,
        "inboxId": 2,
        "mailId": 2,
        "type": "message",
        "senderType": "user",
        "senderId": 1,
        "to": [
          {
            "Name": "",
            "Email": "allamrajuviswanath@gmail.com"
          }
        ],
        "from": {
          "Name": "David Guetta",
          "Email": "viswanath.sarma@acquire.io",
          "MailboxHash": ""
        },
        "cc": [],
        "bcc": [],
        "reply_to": null,
        "subject": "Test Attachments",
        "textBody": "HI____Via acquire.io",
        "htmlBody": "HI<p class=\"acq-signature\"><p>____</p><p>Via <a href=\"https://acquire.io\" target=\"_self\">acquire.io</a></p></p>",
        "mailboxMessageId": "<0d526848-0422-4d08-95c9-33c1ab388046@mtasv.net>",
        "messageId": "0d526848-0422-4d08-95c9-33c1ab388046",
        "mailboxInReplyTo": null,
        "originalRecipient": null,
        "parentId": null,
        "attachments": [
          {
            "n": "Employee Form.docx",
            "s": 452516,
            "t": "application/vnd.openxmlformats-officedocument.wordprocessingml.document",
            "u": "https://uat-drive.acquire.io/5mkg3t/chat/246/2020/11/Employee-Form-4faf9845d158cacbd759d27a.docx",
            "cid": "",
            "key": "WzE5ODEsImNoYXQvMjQ2LzIwMjAvMTEvRW1wbG95ZWUtRm9ybS00ZmFmOTg0NWQxNThjYWNiZDc1OWQyN2EuZG9jeCIsIjVta2czdCIsIkVtcGxveWVlIEZvcm0uZG9jeCIsNDUyNTE2XQ=="
          }
        ],
        "dateCreated": "2020-11-17T13:43:08.000Z",
        "dateSeen": null,
        "dateBounce": null,
        "dateFailed": null,
        "dateDelivery": "2020-11-17T13:43:12.000Z",
        "seen": "no",
        "isDraft": "no",
        "scheduleAt": "2020-11-17T13:43:08.000Z",
        "meta": null,
        "clickedDate": null,
        "unsubscribeDate": null,
        "appMessageId": null,
        "appThreadId": null,
        "user": {
          "departments": [],
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
          "metaDetails": {
            "isBotClient": false,
            "label": ""
          },
          "type": "user",
          "accessLevel": null
        },
        "sender": {
          "type": "user",
          "id": 1,
          "name": "David Guetta",
          "email": "user@example.com",
          "photo": ""
        }
      }
    ]
  }
}mail 
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Body\(raw\)

```text
{
  "ids": [
    53,
    52
  ]
}
```

