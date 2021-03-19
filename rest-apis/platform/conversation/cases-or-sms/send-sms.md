---
description: API to send case message with sms channel
---

# Send-SMS

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/voip/send-sms" path="" %}
{% api-method-summary %}
Send SMS
{% endapi-method-summary %}

{% api-method-description %}
API to send case message with sms channel
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
    "cas": {
      "dateCreated": "2021-03-18T04:51:39.000Z",
      "dateUpdated": "2021-03-18T05:28:02.000Z",
      "id": 1266,
      "contactId": 597718,
      "closedBy": null,
      "visitId": 1345,
      "title": "viswa  : hi",
      "description": "Checkers",
      "channel": "chat",
      "status": "active",
      "closingState": "handled",
      "dateQueue": "2021-03-18T04:51:39.000Z",
      "datePending": "2021-03-18T04:51:39.000Z",
      "dateActive": "2021-03-18T04:51:43.000Z",
      "dateClosed": null,
      "queueId": null,
      "queueOrder": 0,
      "meta": {
        "queues": [
          15
        ],
        "sessionId": "3967179740",
        "queueRecheck": "no",
        "is_new_contact": false,
        "timeline": {
          "id": 1188,
          "objectType": "case",
          "caseId": 1266,
          "viewId": null,
          "noteId": null,
          "threadId": 1266,
          "dateCreated": "2021-03-18T04:51:39.000Z",
          "dateUpdated": "2021-03-18T05:28:02.000Z",
          "contactId": 597718,
          "archive": "no",
          "meta": {}
        },
        "contact": {
          "dateCreated": "2021-03-18T04:44:59.000Z",
          "dateUpdated": "2021-03-19T11:10:59.000Z",
          "id": 597718,
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
              "speed": "7.470000000000001"
            }
          },
          "meta": {},
          "archive": "no",
          "companyId": null,
          "fields": {
            "name": "viswa",
            "email": "viswa@gmail.com",
            "phone": "+19666929552",
            "city": "",
            "state": "",
            "country": {
              "name": "United States",
              "name_official": "United States of America",
              "cca2": "US",
              "ccn3": "84",
              "cca3": "USA",
              "calling_code1": 1,
              "region_id": 496,
              "lat": "38",
              "lng": "-97",
              "voip_enable": true
            },
            "countryId": "517",
            "ip": "2402:8100:21ff:6128:9069:afe4:edd4:1429",
            "dept": "Youpps",
            "checks": "a",
            "title": "Hellos",
            "completed": "No Not Yet",
            "product": "Checkers"
          }
        }
      },
      "parentId": null,
      "userId": null,
      "waitTime": 4,
      "users": [
        {
          "id": 2934,
          "caseId": 1266,
          "type": "user",
          "userId": 1,
          "role": "owner",
          "status": "active",
          "dateCreated": "2021-03-18T04:51:38.000Z",
          "dateLastAssigned": "2021-03-18T04:51:39.000Z",
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
          "id": 2933,
          "caseId": 1266,
          "type": "contact",
          "userId": 597718,
          "role": "owner",
          "status": "active",
          "dateCreated": "2021-03-18T04:51:38.000Z",
          "dateLastAssigned": "2021-03-18T04:51:38.000Z",
          "closed": "no",
          "meta": null,
          "user": {
            "type": "contact",
            "id": 597718,
            "name": "viswa",
            "photo": null
          }
        }
      ],
      "timeline": {
        "id": 1188,
        "objectType": "case",
        "caseId": 1266,
        "viewId": null,
        "noteId": null,
        "threadId": 1266,
        "dateCreated": "2021-03-18T04:51:39.000Z",
        "dateUpdated": "2021-03-18T05:28:02.000Z",
        "contactId": 597718,
        "archive": "no",
        "meta": {}
      },
      "threadId": 1266
    },
    "threadId": 1266,
    "timeline": {
      "id": 1188,
      "objectType": "case",
      "threadId": 1266,
      "dateCreated": "2021-03-18T04:51:39.000Z",
      "dateUpdated": "2021-03-19T11:11:56.000Z",
      "contactId": 597718,
      "archive": "no",
      "meta": {},
      "case": {
        "dateCreated": "2021-03-18T04:51:39.000Z",
        "dateUpdated": "2021-03-19T11:11:56.000Z",
        "id": 1266,
        "contactId": 597718,
        "closedBy": null,
        "visitId": 1345,
        "title": "viswa  : hi",
        "description": "Checkers",
        "channel": "chat",
        "status": "active",
        "closingState": "handled",
        "dateQueue": "2021-03-18T04:51:39.000Z",
        "datePending": "2021-03-18T04:51:39.000Z",
        "dateActive": "2021-03-18T04:51:43.000Z",
        "dateClosed": null,
        "queueId": null,
        "queueOrder": 0,
        "meta": {
          "queues": [
            15
          ],
          "contact": {
            "id": 597718,
            "meta": {},
            "fields": {
              "ip": "2402:8100:21ff:6128:9069:afe4:edd4:1429",
              "city": "",
              "dept": "Youpps",
              "name": "viswa",
              "email": "viswa@gmail.com",
              "phone": "+19666929552",
              "state": "",
              "title": "Hellos",
              "checks": "a",
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
              "product": "Checkers",
              "completed": "No Not Yet",
              "countryId": "517"
            },
            "archive": "no",
            "companyId": null,
            "clientName": "Chrome",
            "clientType": "web",
            "dateCreated": "2021-03-18T04:44:59.000Z",
            "dateUpdated": "2021-03-19T11:10:59.000Z",
            "clientOsName": "Linux",
            "clientDetails": {
              "ua": "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/87.0.4280.66 Safari/537.36",
              "engine": {
                "name": "Blink",
                "version": "87.0.4280.66"
              },
              "network": {
                "type": "4g",
                "speed": "7.470000000000001"
              }
            },
            "clientVersion": "87.0",
            "clientOsVersion": "x86_64",
            "clientDeviceType": "Desktop",
            "clientDeviceModel": null,
            "clientDeviceVendor": null
          },
          "timeline": {
            "id": 1188,
            "meta": {},
            "caseId": 1266,
            "noteId": null,
            "viewId": null,
            "archive": "no",
            "threadId": 1266,
            "contactId": 597718,
            "objectType": "case",
            "dateCreated": "2021-03-18T04:51:39.000Z",
            "dateUpdated": "2021-03-18T05:28:02.000Z"
          },
          "sessionId": "3967179740",
          "queueRecheck": "no",
          "is_new_contact": false
        },
        "parentId": null,
        "userId": null,
        "waitTime": 4,
        "users": [
          {
            "id": 2934,
            "caseId": 1266,
            "type": "user",
            "userId": 1,
            "role": "owner",
            "status": "active",
            "dateCreated": "2021-03-18T04:51:38.000Z",
            "dateLastAssigned": "2021-03-18T04:51:39.000Z",
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
            "id": 2933,
            "caseId": 1266,
            "type": "contact",
            "userId": 597718,
            "role": "owner",
            "status": "active",
            "dateCreated": "2021-03-18T04:51:38.000Z",
            "dateLastAssigned": "2021-03-18T04:51:38.000Z",
            "closed": "no",
            "meta": null,
            "user": {
              "type": "contact",
              "id": 597718,
              "name": "viswa",
              "photo": null
            }
          }
        ],
        "fields": {
          "completed": "Yes Done"
        },
        "threadId": 1266,
        "lastMessage": {
          "id": 6736,
          "caseId": 1266,
          "channel": "chat",
          "senderId": 1,
          "senderType": "user",
          "type": "message",
          "message": "Checkers",
          "dateCreated": "2021-03-18T05:28:02.000Z",
          "dateUpdated": null,
          "seen": "no",
          "meta": {}
        },
        "tags": [],
        "channels": [
          "chat",
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
      "message": "SMS by David Guetta",
      "msgType": "sms",
      "channelType": "voip",
      "attachments": [],
      "id": 331,
      "caseId": 1266,
      "from": "+12513188609",
      "to": "+919666929552",
      "voip_account_id": 3,
      "senderType": "user",
      "senderId": 1,
      "type": "sms",
      "meta": {
        "To": "+919666929552",
        "to": "+919666929552",
        "SMS": "hi",
        "sid": "SM78eeffd82fb84a7aa06e7baaf9a3d6e1",
        "uri": "/2010-04-01/Accounts/ACf83886e81f434fe02812d132ab8790ce/Messages/SM78eeffd82fb84a7aa06e7baaf9a3d6e1.json",
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
        "dateCreated": "2021-03-19T11:11:55.000Z",
        "dateUpdated": "2021-03-19T11:11:55.000Z",
        "numSegments": "1",
        "errorMessage": null,
        "subresourceUris": {
          "media": "/2010-04-01/Accounts/ACf83886e81f434fe02812d132ab8790ce/Messages/SM78eeffd82fb84a7aa06e7baaf9a3d6e1/Media.json"
        },
        "messagingServiceSid": null
      },
      "call_transcript": 0,
      "caseMessageId": 6819,
      "timelineId": 1188,
      "contactId": 597718,
      "seen": "yes",
      "dateCreated": "2021-03-19T11:11:56.000Z",
      "call_answered": null,
      "call_end": null,
      "call_sid": "SM78eeffd82fb84a7aa06e7baaf9a3d6e1",
      "status": "sent",
      "call_status": null,
      "conferenceId": null,
      "sender": {
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
      "is_new_case": false,
      "is_new_contact": false,
      "cas": {
        "dateCreated": "2021-03-18T04:51:39.000Z",
        "dateUpdated": "2021-03-19T11:11:56.000Z",
        "id": 1266,
        "contactId": 597718,
        "closedBy": null,
        "visitId": 1345,
        "title": "viswa  : hi",
        "description": "Checkers",
        "channel": "chat",
        "status": "active",
        "closingState": "handled",
        "dateQueue": "2021-03-18T04:51:39.000Z",
        "datePending": "2021-03-18T04:51:39.000Z",
        "dateActive": "2021-03-18T04:51:43.000Z",
        "dateClosed": null,
        "queueId": null,
        "queueOrder": 0,
        "meta": {
          "queues": [
            15
          ],
          "contact": {
            "id": 597718,
            "meta": {},
            "fields": {
              "ip": "2402:8100:21ff:6128:9069:afe4:edd4:1429",
              "city": "",
              "dept": "Youpps",
              "name": "viswa",
              "email": "viswa@gmail.com",
              "phone": "+19666929552",
              "state": "",
              "title": "Hellos",
              "checks": "a",
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
              "product": "Checkers",
              "completed": "No Not Yet",
              "countryId": "517"
            },
            "archive": "no",
            "companyId": null,
            "clientName": "Chrome",
            "clientType": "web",
            "dateCreated": "2021-03-18T04:44:59.000Z",
            "dateUpdated": "2021-03-19T11:10:59.000Z",
            "clientOsName": "Linux",
            "clientDetails": {
              "ua": "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/87.0.4280.66 Safari/537.36",
              "engine": {
                "name": "Blink",
                "version": "87.0.4280.66"
              },
              "network": {
                "type": "4g",
                "speed": "7.470000000000001"
              }
            },
            "clientVersion": "87.0",
            "clientOsVersion": "x86_64",
            "clientDeviceType": "Desktop",
            "clientDeviceModel": null,
            "clientDeviceVendor": null
          },
          "timeline": {
            "id": 1188,
            "meta": {},
            "caseId": 1266,
            "noteId": null,
            "viewId": null,
            "archive": "no",
            "threadId": 1266,
            "contactId": 597718,
            "objectType": "case",
            "dateCreated": "2021-03-18T04:51:39.000Z",
            "dateUpdated": "2021-03-18T05:28:02.000Z"
          },
          "sessionId": "3967179740",
          "queueRecheck": "no",
          "is_new_contact": false
        },
        "parentId": null,
        "userId": null,
        "waitTime": 4,
        "users": [
          {
            "id": 2934,
            "caseId": 1266,
            "type": "user",
            "userId": 1,
            "role": "owner",
            "status": "active",
            "dateCreated": "2021-03-18T04:51:38.000Z",
            "dateLastAssigned": "2021-03-18T04:51:39.000Z",
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
            "id": 2933,
            "caseId": 1266,
            "type": "contact",
            "userId": 597718,
            "role": "owner",
            "status": "active",
            "dateCreated": "2021-03-18T04:51:38.000Z",
            "dateLastAssigned": "2021-03-18T04:51:38.000Z",
            "closed": "no",
            "meta": null,
            "user": {
              "type": "contact",
              "id": 597718,
              "name": "viswa",
              "photo": null
            }
          }
        ],
        "timeline": {
          "id": 1188,
          "objectType": "case",
          "caseId": 1266,
          "viewId": null,
          "noteId": null,
          "threadId": 1266,
          "dateCreated": "2021-03-18T04:51:39.000Z",
          "dateUpdated": "2021-03-19T11:11:56.000Z",
          "contactId": 597718,
          "archive": "no",
          "meta": {}
        },
        "threadId": 1266
      },
      "case_id": 1266,
      "timeline": {
        "id": 1188,
        "objectType": "case",
        "caseId": 1266,
        "viewId": null,
        "noteId": null,
        "threadId": 1266,
        "dateCreated": "2021-03-18T04:51:39.000Z",
        "dateUpdated": "2021-03-19T11:11:56.000Z",
        "contactId": 597718,
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
    "threadId":1266,
    "contactId":597718,
    "timelineId":1188,
    "Body":"hi",
    "message":"hi",
    "msgType":"message",
    "title":"viswa  : hi",
    "isMultiChannel":false,
    "sms":"hi",
    "id":1266,
    "To":"+919666929552",
    "From":"+12513188609",
    "isClosed":false,
    "markValue":"<p>hi</p>"
}
```

