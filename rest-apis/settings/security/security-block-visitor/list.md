---
description: List all blocked visitors
---

# List

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/block-visitor" path="" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
List all blocked visitors
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{API\_KEY}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="select" type="array" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="relations" type="object" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="where" type="object" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="order" type="object" required=false %}

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
    "offset": 0,
    "count": 6,
    "data": [
      {
        "id": 1,
        "data": {
          "id": 597304,
          "ip": "2402:8100:21fa:4213:bd98:f32c:7d38:872d",
          "email": "",
          "phone": ""
        },
        "dateCreated": "2021-02-04T20:00:46.000Z",
        "blockTill": "2022-02-04T23:59:59.000Z",
        "blockBy": 1,
        "type": "contact",
        "user": {
            "departments": [],
            "roles": [],
            "id": 1,
            "name": "David Guetta",
            "firstName": "David Guetta",
            "lastName": "",
            "photo": "",
            "email": "user@example.com",
            "clientId": ""
          },
          "parentId": 0,
          "metaDetails": {
            "isBotClient": false,
            "label": ""
          },
          "type": "user",
          "accessLevel": null
        }
      },
      {
        "id": 2,
        "data": {
          "id": 3561,
          "ip": "2402:8100:21f8:519d:747f:7f3f:32c4:cca8",
          "email": "",
          "phone": ""
        },
        "dateCreated": "2021-02-04T20:01:10.000Z",
        "blockTill": "2022-02-04T23:59:59.000Z",
        "blockBy": 1,
        "type": "contact",
        "user": {
            "departments": [],
            "roles": [],
            "id": 1,
            "name": "David Guetta",
            "firstName": "David Guetta",
            "lastName": "",
            "photo": "",
            "email": "user@example.com",
            "clientId": ""
          },
          "parentId": 0,
          "metaDetails": {
            "isBotClient": false,
            "label": ""
          },
          "type": "user",
          "accessLevel": null
        }
      },
      {
        "id": 3,
        "data": {
          "id": 3560,
          "ip": "117.249.237.201",
          "email": "",
          "phone": ""
        },
        "dateCreated": "2021-02-04T20:02:39.000Z",
        "blockTill": "2022-02-04T23:59:59.000Z",
        "blockBy": 1,
        "type": "contact",
        "user": {
            "departments": [],
            "roles": [],
            "id": 1,
            "name": "David Guetta",
            "firstName": "David Guetta",
            "lastName": "",
            "photo": "",
            "email": "user@example.com",
            "clientId": ""
          },
          "parentId": 0,
          "metaDetails": {
            "isBotClient": false,
            "label": ""
          },
          "type": "user",
          "accessLevel": null
        }
      },
      {
        "id": 4,
        "data": {
          "id": 597306,
          "ip": "2402:8100:21ff:bddf:14cb:535:d5c6:d26d",
          "email": "",
          "phone": ""
        },
        "dateCreated": "2021-02-05T08:43:01.000Z",
        "blockTill": "2022-02-05T23:59:59.000Z",
        "blockBy": 1,
        "type": "contact",
        "user": {
            "departments": [],
            "roles": [],
            "id": 1,
            "name": "David Guetta",
            "firstName": "David Guetta",
            "lastName": "",
            "photo": "",
            "email": "user@example.com",
            "clientId": ""
          },
          "parentId": 0,
          "metaDetails": {
            "isBotClient": false,
            "label": ""
          },
          "type": "user",
          "accessLevel": null
        }
      },
      {
        "id": 5,
        "data": {
          "id": 597307,
          "ip": "2402:8100:21fa:14b8:14cb:535:d5c6:d26d",
          "email": "",
          "phone": ""
        },
        "dateCreated": "2021-02-05T08:43:35.000Z",
        "blockTill": "2022-02-05T23:59:59.000Z",
        "blockBy": 1,
        "type": "contact",
        "user": {
            "departments": [],
            "roles": [],
            "id": 1,
            "name": "David Guetta",
            "firstName": "David Guetta",
            "lastName": "",
            "photo": "",
            "email": "user@example.com",
            "clientId": ""
          },
          "parentId": 0,
          "metaDetails": {
            "isBotClient": false,
            "label": ""
          },
          "type": "user",
          "accessLevel": null
        }
      },
      {
        "id": 6,
        "data": [
          "10.10.10.10",
          "11.11.11.11"
        ],
        "dateCreated": "2021-03-22T09:55:44.000Z",
        "blockTill": "2020-03-26T23:59:59.000Z",
        "blockBy": 1,
        "type": "email",
        "user": {
            "departments": [],
            "roles": [],
            "id": 1,
            "name": "David Guetta",
            "firstName": "David Guetta",
            "lastName": "",
            "photo": "",
            "email": "user@example.com",
            "clientId": ""
          },
          "parentId": 0,
          "metaDetails": {
            "isBotClient": false,
            "label": ""
          },
          "type": "user",
          "accessLevel": null
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

