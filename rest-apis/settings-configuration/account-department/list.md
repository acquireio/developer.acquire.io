---
description: List the available departments
---

# List

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/account/department" path="" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
List all departments and users who belong to those departments.
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
    "count": 8,
    "data": [
      {
        "id": 6,
        "name": "eswweew ",
        "status": "active",
        "users": []
      },
      {
        "id": 7,
        "name": "fdhfthnfgg",
        "status": "active",
        "users": []
      },
      {
        "id": 8,
        "name": "Youpps",
        "status": "active",
        "users": [
          {
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
        ]
      },
      {
        "id": 9,
        "name": "robust",
        "status": "active",
        "users": [
          {
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
        ]
      },
      {
        "id": 10,
        "name": "qwe",
        "status": "active",
        "users": []
      },
      {
        "id": 11,
        "name": "moi",
        "status": "active",
        "users": []
      },
      {
        "id": 12,
        "name": "roi",
        "status": "active",
        "users": []
      },
      {
        "id": 13,
        "name": "eoi",
        "status": "active",
        "users": []
      }
    ]
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

