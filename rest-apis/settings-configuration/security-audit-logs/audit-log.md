# Audit Log

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/account/audit-log" path="" %}
{% api-method-summary %}
Get Audit log
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="select" type="array" required=false %}
Specify the columns to be selected from the response.
{% endapi-method-parameter %}

{% api-method-parameter name="relations" type="object" required=false %}
Specifies the relation ship with other entities
{% endapi-method-parameter %}

{% api-method-parameter name="where" type="object" required=false %}
Specify the object which is a column name followed by the condition
{% endapi-method-parameter %}

{% api-method-parameter name="userId" type="string" required=false %}
Specify the user Id
{% endapi-method-parameter %}

{% api-method-parameter name="order" type="object" required=false %}
Specify an object which have a key value pairs where key with be name and value will be ordering expression
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
    "page": 1,
    "limit": 10,
    "count": 1403,
    "data": [
      {
        "id": 2351,
        "objectTable": "setting",
        "objectId": 1,
        "objectProperty": null,
        "actionType": "created",
        "actionDate": "2021-04-07T05:44:23.000Z",
        "actionOwnerType": "user",
        "dataBefore": {},
        "dataAfter": {
          "key": "crm.permissions",
          "value": {
            "value": [
              "jpg",
              "png",
              "gif",
              "bmp",
              "jpeg",
              "txt",
              "doc",
              "docx",
              "xls",
              "xlsx",
              "avi",
              "mp3",
              "mp4",
              "7z",
              "rar",
              "ai",
              "csv",
              "ppt",
              "pdf",
              "ico",
              "psd",
              "zip"
            ],
            "selected": "default"
          },
          "tenantId": "5mkg3t"
        },
        "ip": "117.245.108.71",
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
      {
        "id": 2352,
        "objectTable": "setting",
        "objectId": 1,
        "objectProperty": null,
        "actionType": "created",
        "actionDate": "2021-04-07T05:44:23.000Z",
        "actionOwnerType": "user",
        "dataBefore": {},
        "dataAfter": {
          "key": "crm.enable_file_upload_backend",
          "value": "yes",
          "tenantId": "5mkg3t"
        },
        "ip": "117.245.108.71",
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
      {
        "id": 2353,
        "objectTable": "setting",
        "objectId": 1,
        "objectProperty": null,
        "actionType": "created",
        "actionDate": "2021-04-07T05:44:23.000Z",
        "actionOwnerType": "user",
        "dataBefore": {},
        "dataAfter": {
          "key": "crm.enable_file_upload_frontend",
          "value": "yes",
          "tenantId": "5mkg3t"
        },
        "ip": "117.245.108.71",
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
      {
        "id": 2342,
        "objectTable": "business_rules_actions",
        "objectId": 1,
        "objectProperty": null,
        "actionType": "created",
        "actionDate": "2021-04-07T05:21:17.000Z",
        "actionOwnerType": "user",
        "dataBefore": {},
        "dataAfter": {
          "name": "Entry Point",
          "isRoot": "yes",
          "linkType": "goto",
          "nodeType": "output-only",
          "position": {
            "x": 300,
            "y": 100
          },
          "actionType": "channel",
          "businessRule": 85
        },
        "ip": "117.245.108.71",
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
      {
        "id": 2343,
        "objectTable": "business_rules_actions_data",
        "objectId": 1,
        "objectProperty": null,
        "actionType": "created",
        "actionDate": "2021-04-07T05:21:17.000Z",
        "actionOwnerType": "user",
        "dataBefore": {},
        "dataAfter": {
          "actionData": {
            "data": {
              "entryPoints": []
            },
            "type": "channel"
          },
          "businessRuleAction": 122
        },
        "ip": "117.245.108.71",
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
      {
        "id": 2344,
        "objectTable": "business_rules_ports",
        "objectId": 1,
        "objectProperty": null,
        "actionType": "created",
        "actionDate": "2021-04-07T05:21:17.000Z",
        "actionOwnerType": "user",
        "dataBefore": {},
        "dataAfter": {
          "name": "Entry Point",
          "type": "output",
          "value": "continue",
          "businessRuleAction": 122
        },
        "ip": "117.245.108.71",
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
      {
        "id": 2345,
        "objectTable": "business_rules_actions",
        "objectId": 1,
        "objectProperty": null,
        "actionType": "created",
        "actionDate": "2021-04-07T05:21:17.000Z",
        "actionOwnerType": "user",
        "dataBefore": {},
        "dataAfter": {
          "name": "SLA Policy",
          "isRoot": "no",
          "linkType": "bubble",
          "nodeType": "input-output",
          "position": {
            "x": 300,
            "y": 250
          },
          "actionType": "sla-policy",
          "businessRule": 85
        },
        "ip": "117.245.108.71",
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
      {
        "id": 2346,
        "objectTable": "business_rules_actions_data",
        "objectId": 1,
        "objectProperty": null,
        "actionType": "created",
        "actionDate": "2021-04-07T05:21:17.000Z",
        "actionOwnerType": "user",
        "dataBefore": {},
        "dataAfter": {
          "actionData": {
            "data": {
              "sla": [
                "1"
              ]
            },
            "type": "sla-policy"
          },
          "businessRuleAction": 123
        },
        "ip": "117.245.108.71",
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
      {
        "id": 2347,
        "objectTable": "business_rules_ports",
        "objectId": 1,
        "objectProperty": null,
        "actionType": "created",
        "actionDate": "2021-04-07T05:21:17.000Z",
        "actionOwnerType": "user",
        "dataBefore": {},
        "dataAfter": {
          "name": "First Response",
          "type": "bottom",
          "value": "first_response",
          "businessRuleAction": 123
        },
        "ip": "117.245.108.71",
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
      {
        "id": 2348,
        "objectTable": "business_rules_ports",
        "objectId": 1,
        "objectProperty": null,
        "actionType": "created",
        "actionDate": "2021-04-07T05:21:17.000Z",
        "actionOwnerType": "user",
        "dataBefore": {},
        "dataAfter": {
          "name": "Resolution",
          "type": "bottom",
          "value": "resolution",
          "businessRuleAction": 123
        },
        "ip": "117.245.108.71",
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
      }
    ]
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

