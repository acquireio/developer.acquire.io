---
description: Retrieve a log user activities
---

# Audit Log Users

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/account/audit-log/get-audit-log-users" path="" %}
{% api-method-summary %}
Get Audit Log Users
{% endapi-method-summary %}

{% api-method-description %}
Retrieve a log of user activities
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{API\_KEY}}
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
    "data": [
      {
        "auditUser": {
          "id": 1,
          "objectTable": "feedback",
          "objectId": 1,
          "objectProperty": null,
          "actionType": "created",
          "actionDate": "2020-06-24T14:28:14.000Z",
          "actionOwnerType": "user",
          "dataBefore": {},
          "dataAfter": {
            "type": "multiple_checkbox",
            "config": {
              "values": [
                {
                  "label": "a",
                  "value": "a"
                },
                {
                  "label": "b",
                  "value": "b"
                },
                {
                  "label": "c",
                  "value": "c"
                }
              ],
              "required": false,
              "rating_type": "multiple_checkbox",
              "error_message": "Please select at least one."
            },
            "status": "active",
            "channels": [
              "chat"
            ],
            "question": "Give the feedback for the chat experience",
            "dateCreated": "2020-06-24T14:28:13.543Z",
            "departments": []
          },
          "ip": "117.209.192.185",
          "user": {
            "firstName": "David Guetta",
            "lastName": "",
            "id": 1,
            "type": "user",
            "status": "active",
            "lastLoginId": null,
            "parentId": null,
            "ownerId": null,
            "name": "David Guetta",
            "email": "user@example.com",
            "phone": "+91-1234567890",
            "photo": "",
            "inviteToken": null,
            "language": null,
            "clientId": null,
            "clientAppId": null,
            "clientAuthorizer": null,
            "clientPermissions": null,
            "stateId": null,
            "countryId": null,
            "dateCreated": null
          }
        },
        "firstName": "David Guetta",
        "lastName": "",
        "id": 1,
        "type": "user",
        "status": "active",
        "lastLoginId": null,
        "parentId": null,
        "ownerId": null,
        "name": "David Guetta",
        "email": "user@example.com",
        "phone": "+91-1234567890",
        "photo": "",
        "inviteToken": null,
        "language": null,
        "clientId": null,
        "clientAppId": null,
        "clientAuthorizer": null,
        "clientPermissions": null,
        "stateId": null,
        "countryId": null,
        "dateCreated": null
      },
      {
        "auditUser": {
          "id": 1754,
          "objectTable": "user",
          "objectId": 1,
          "objectProperty": null,
          "actionType": "modified",
          "actionDate": "2021-02-03T17:02:21.000Z",
          "actionOwnerType": "user",
          "dataBefore": {},
          "dataAfter": {
            "id": 19
            "name": "hello user1",
            "type": "user",
            "email": "hello@acquire.io",
            "phone": null,
            "status": "active",
            "stateId": null,
            "clientId": null,
            "language": null,
            "lastName": "",
            "parentId": null,
            "tenantId": "5mkg3t",
            "countryId": null,
            "firstName": "hello user1",
            "clientAppId": null,
            "dateCreated": "2021-02-03T16:59:45.000Z",
            "inviteToken": null,
            "lastLoginId": null,
            "clientAuthorizer": null,
            "clientPermissions": null
          },
          "ip": "2409:4070:2c83:144f:bd5d:f306:e429:9876",
          "user": {
            "firstName": "hello user1",
            "lastName": "",
            "id": 19,
            "type": "user",
            "status": "active",
            "lastLoginId": null,
            "parentId": null,
            "ownerId": null,
            "name": "hello user1",
            "email": "hello@acquire.io",
            "phone": null,
            "photo": null,
            "inviteToken": null,
            "language": null,
            "clientId": null,
            "clientAppId": null,
            "clientAuthorizer": null,
            "clientPermissions": null,
            "stateId": null,
            "countryId": null,
            "dateCreated": "2021-02-03T16:59:45.000Z"
          }
        },
        "firstName": "hello user1",
        "lastName": "",
        "id": 19,
        "type": "user",
        "status": "active",
        "lastLoginId": null,
        "parentId": null,
        "ownerId": null,
        "name": "hello user1",
        "email": "hello@acquire.io",
        "phone": null,
        "photo": null,
        "inviteToken": null,
        "language": null,
        "clientId": null,
        "clientAppId": null,
        "clientAuthorizer": null,
        "clientPermissions": null,
        "stateId": null,
        "countryId": null,
        "dateCreated": "2021-02-03T16:59:45.000Z"
        "tenantId": "5mkg3t"
      },
      {
        "auditUser": {
          "id": 1873,
          "objectTable": "user",
          "objectId": 1,
          "objectProperty": null,
          "actionType": "modified",
          "actionDate": "2021-03-10T08:03:56.000Z",
          "actionOwnerType": "user",
          "dataBefore": {},
          "dataAfter": {
            "id": 20,
            "name": "set2",
            "type": "user",
            "email": "set2@acquire.io",
            "phone": null,
            "status": "active",
            "ownerId": null,
            "stateId": null,
            "clientId": null,
            "language": null,
            "lastName": "",
            "parentId": null,
            "tenantId": "5mkg3t",
            "countryId": null,
            "firstName": "set2",
            "clientAppId": null,
            "dateCreated": "2021-02-03T17:00:26.000Z",
            "inviteToken": null,
            "lastLoginId": null,
            "clientAuthorizer": null,
            "clientPermissions": null
          },
          "ip": "2409:4070:2e96:7812:fd05:dce7:4652:27b1",
          "user": {
            "firstName": "set2",
            "lastName": "",
            "id": 20,
            "type": "user",
            "status": "active",
            "lastLoginId": null,
            "parentId": null,
            "ownerId": null,
            "name": "set2",
            "email": "set2@acquire.io",
            "phone": null,
            "photo": null,
            "inviteToken": null,
            "language": null,
            "clientId": null,
            "clientAppId": null,
            "clientAuthorizer": null,
            "clientPermissions": null,
            "stateId": null,
            "countryId": null,
            "dateCreated": "2021-02-03T17:00:26.000Z"
          }
        },
        "firstName": "set2",
        "lastName": "",
        "id": 20,
        "type": "user",
        "status": "active",
        "lastLoginId": null,
        "parentId": null,
        "ownerId": null,
        "name": "set2",
        "email": "set2@acquire.io",
        "phone": null,
        "photo": null,
        "inviteToken": null,
        "language": null,
        "clientId": null,
        "clientAppId": null,
        "clientAuthorizer": null,
        "clientPermissions": null,
        "stateId": null,
        "countryId": null,
        "dateCreated": "2021-02-03T17:00:26.000Z",
        "tenantId": "5mkg3t"
      },
      {
        "auditUser": {
          "id": 2096,
          "objectTable": "webhook",
          "objectId": 1,
          "objectProperty": null,
          "actionType": "created",
          "actionDate": "2021-03-18T12:26:08.000Z",
          "actionOwnerType": "client",
          "dataBefore": {},
          "dataAfter": {
            "url": "https://5mkg3t.uat.env.acquire.io/api/v1/bot/hook?slug=conversational_bot&misc_id=2",
            "flow": "outbound",
            "name": "bot:conversational_bot:2",
            "type": "client",
            "events": [
              {
                "event": "user:case-invite",
                "params": {
                  "user": 22
                }
              },
              {
                "event": "user:case-joined",
                "params": {}
              },
              {
                "event": "case:message:new",
                "params": {
                  "user": 22
                }
              }
            ],
            "format": "application/json",
            "status": "active",
            "userId": 22,
            "hmacKey": "Secret:conversational_bot:2",
            "tenantId": "5mkg3t",
            "urlSkipSsl": "yes",
            "historyExpires": "2021-03-25T12:26:08.150Z",
            "notificationEmail": "sanjay@acquire.io"
          },
          "ip": "127.0.0.1",
          "user": null
        },
        "id": 22,
        "name": "User Deleted (22)"
      },
      {
        "auditUser": {
          "id": 2100,
          "objectTable": "webhook",
          "objectId": 1,
          "objectProperty": null,
          "actionType": "created",
          "actionDate": "2021-03-18T12:31:46.000Z",
          "actionOwnerType": "client",
          "dataBefore": {},
          "dataAfter": {
            "url": "https://5mkg3t.uat.env.acquire.io/api/v1/bot/hook?slug=conversational_bot&misc_id=3",
            "flow": "outbound",
            "name": "bot:conversational_bot:3",
            "type": "client",
            "events": [
              {
                "event": "user:case-invite",
                "params": {
                  "user": 23
                }
              },
              {
                "event": "user:case-joined",
                "params": {}
              },
              {
                "event": "case:message:new",
                "params": {
                  "user": 23
                }
              }
            ],
            "format": "application/json",
            "status": "active",
            "userId": 23,
            "hmacKey": "Secret:conversational_bot:3",
            "tenantId": "5mkg3t",
            "urlSkipSsl": "yes",
            "historyExpires": "2021-03-25T12:31:46.189Z",
            "notificationEmail": "sanjay@acquire.io"
          },
          "ip": "127.0.0.1",
          "user": {
            "firstName": "Virtual Assistant",
            "lastName": "",
            "id": 23,
            "type": "client",
            "status": "active",
            "lastLoginId": null,
            "parentId": 3,
            "ownerId": null,
            "name": "Virtual Assistant",
            "email": null,
            "phone": null,
            "photo": "",
            "inviteToken": null,
            "language": null,
            "clientId": "bot:conversational_bot:3",
            "clientAppId": null,
            "clientAuthorizer": {
              "id": 3,
              "clientIp": "127.0.0.1",
              "clientName": "api",
              "clientType": "api"
            },
            "clientPermissions": [],
            "stateId": null,
            "countryId": null,
            "dateCreated": "2021-03-18T12:31:46.000Z",
          }
        },
        "firstName": "Virtual Assistant",
        "lastName": "",
        "id": 23,
        "type": "client",
        "status": "active",
        "lastLoginId": null,
        "parentId": 3,
        "ownerId": null,
        "name": "Virtual Assistant",
        "email": null,
        "phone": null,
        "photo": "",
        "inviteToken": null,
        "language": null,
        "clientId": "bot:conversational_bot:3",
        "clientAppId": null,
        "clientAuthorizer": {
          "id": 3,
          "clientIp": "127.0.0.1",
          "clientName": "api",
          "clientType": "api"
        },
        "clientPermissions": [],
        "stateId": null,
        "countryId": null,
        "dateCreated": "2021-03-18T12:31:46.000Z",
        "tenantId": "5mkg3t"
      },
      {
        "auditUser": {
          "id": 2220,
          "objectTable": "API token",
          "objectId": 1,
          "objectProperty": null,
          "actionType": "modified",
          "actionDate": "2021-04-01T06:10:47.000Z",
          "actionOwnerType": "user",
          "dataBefore": {},
          "dataAfter": {
            "id": 26,
            "name": "asd",
            "type": "client",
            "email": null,
            "phone": null,
            "photo": null,
            "status": "active",
            "ownerId": 1,
            "stateId": null,
            "clientId": null,
            "language": "en",
            "lastName": "",
            "parentId": null,
            "tenantId": "5mkg3t",
            "countryId": null,
            "firstName": "asd",
            "clientAppId": null,
            "dateCreated": "2021-03-31T05:01:08.000Z",
            "inviteToken": null,
            "lastLoginId": null,
            "clientAuthorizer": null,
            "clientPermissions": [
              "settings.web-widget",
              "settings.account-settings",
              "settings.profile",
              "settings.roles",
              "settings.departments",
              "settings.apps",
              "settings.custom-attributes",
              "settings.shortcuts",
              "settings.tags",
              "settings.feedbacks",
              "settings.audit-logs",
              "settings.spam",
              "settings.translations",
              "settings.api-keys",
              "settings.webhooks",
              "analytics.agent",
              "analytics.app",
              "analytics.bot",
              "analytics.chat",
              "analytics.cobrowse",
              "analytics.custom-reporting",
              "analytics.feedback",
              "analytics.general",
              "analytics.kb",
              "analytics.liveDashboard",
              "analytics.mail",
              "analytics.voip",
              "app-store.home",
              "bot.home",
              "bot.conversational-bot",
              "bot.sequence-bot",
              "bot.configurations",
              "dashboard.contact-list",
              "dashboard.company",
              "dashboard.campaign",
              "dashboard.delete-conversation",
              "knowledge-base.kb-setup",
              "knowledge-base.add",
              "knowledge-base.edit",
              "knowledge-base.delete",
              "knowledge-base.edit-theme",
              "email.inbox",
              "email.template",
              "email.smtp",
              "email.signature",
              "media.media",
              "voIP.default",
              "voIP.event",
              "voIP.setup",
              "voIP.setting",
              "triggers.business-rules",
              "triggers.triggers",
              "chat.cobrowse",
              "chat.screen-share",
              "chat.video-calls",
              "chat.audio-calls",
              "access-level.account"
            ],
            "userAuthProviders": [
              {
                "id": 26,
                "type": "api",
                "token": "YgaB7h87Aj0UvV7MLUdLUWhxLo1bfLWcxVyQWfq09Vb4T3lp",
                "status": "active",
                "expires": null,
                "identity": null,
                "metaData": null,
                "tenantId": "5mkg3t",
                "dateCreated": "2021-03-31T05:01:08.000Z"
              }
            ]
          },
          "ip": "2402:8100:21fc:ed57:3513:3d04:bbde:4cec",
          "user": {
            "firstName": "myuser",
            "lastName": "",
            "id": 28,
            "type": "user",
            "status": "active",
            "lastLoginId": null,
            "parentId": null,
            "ownerId": null,
            "name": "myuser",
            "email": "myuser@acquire.io",
            "phone": null,
            "photo": null,
            "inviteToken": null,
            "language": null,
            "clientId": null,
            "clientAppId": null,
            "clientAuthorizer": null,
            "clientPermissions": null,
            "stateId": null,
            "countryId": null,
            "dateCreated": "2021-04-01T05:55:37.000Z"
          }
        },
        "firstName": "myuser",
        "lastName": "",
        "id": 28,
        "type": "user",
        "status": "active",
        "lastLoginId": null,
        "parentId": null,
        "ownerId": null,
        "name": "myuser",
        "email": "myuser@acquire.io",
        "phone": null,
        "photo": null,
        "inviteToken": null,
        "language": null,
        "clientId": null,
        "clientAppId": null,
        "clientAuthorizer": null,
        "clientPermissions": null,
        "stateId": null,
        "countryId": null,
        "dateCreated": "2021-04-01T05:55:37.000Z",
        "tenantId": "5mkg3t"
      },
      {
        "auditUser": {
          "id": 2251,
          "objectTable": "setting",
          "objectId": 1,
          "objectProperty": null,
          "actionType": "created",
          "actionDate": "2021-04-02T09:02:19.000Z",
          "actionOwnerType": "user",
          "dataBefore": {},
          "dataAfter": {
            "key": "crm.show_agent_avatars_widget",
            "value": "yes",
            "tenantId": "5mkg3t"
          },
          "ip": "103.238.107.147",
          "user": {
            "firstName": "Jagrut",
            "lastName": "",
            "id": 31,
            "type": "user",
            "status": "active",
            "lastLoginId": null,
            "parentId": null,
            "ownerId": null,
            "name": "Jagrut",
            "email": "jagrut@example.com",
            "phone": null,
            "photo": null,
            "inviteToken": null,
            "language": null,
            "clientId": null,
            "clientAppId": null,
            "clientAuthorizer": null,
            "clientPermissions": null,
            "stateId": null,
            "countryId": null,
            "dateCreated": "2021-04-02T08:57:02.000Z"
          }
        },
        "firstName": "Jagrut",
        "lastName": "",
        "id": 31,
        "type": "user",
        "status": "active",
        "lastLoginId": null,
        "parentId": null,
        "ownerId": null,
        "name": "Jagrut",
        "email": "jagrut@example.com",
        "phone": null,
        "photo": null,
        "inviteToken": null,
        "language": null,
        "clientId": null,
        "clientAppId": null,
        "clientAuthorizer": null,
        "clientPermissions": null,
        "stateId": null,
        "countryId": null,
        "dateCreated": "2021-04-02T08:57:02.000Z",
        "tenantId": "5mkg3t"
      },
      {
        "auditUser": {
          "id": 2308,
          "objectTable": "shortcut",
          "objectId": 1,
          "objectProperty": null,
          "actionType": "created",
          "actionDate": "2021-04-02T17:59:32.000Z",
          "actionOwnerType": "client",
          "dataBefore": {},
          "dataAfter": {
            "message": "Hello New Shortcuts",
            "tenantId": "5mkg3t",
            "department": [
              "6"
            ],
            "shortcut_name": "New shorts"
          },
          "ip": "117.209.253.86",
          "user": null
        },
        "id": 32,
        "name": "User Deleted (32)"
      }
    ]
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

