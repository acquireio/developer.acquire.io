---
description: List all account roles
---

# List

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/account/role" path="" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
Retrieve a list of the account's roles
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter type="string" name="Authorization" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="select" type="array" required=false %}
Specify the array of fields which wants as response
{% endapi-method-parameter %}

{% api-method-parameter name="relations" type="string" required=false %}
Specify the relation with other entities
{% endapi-method-parameter %}

{% api-method-parameter name="where" type="object" required=false %}
Specify the condition to narrow the response.
{% endapi-method-parameter %}

{% api-method-parameter name="order" type="object" required=false %}
Specify the order which is an object with descending or ascending order.
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
    "count": 2,
    "data": [
      {
        "id": 1,
        "roleName": "Administrator",
        "permissionType": null,
        "meta": null
      },
      {
        "id": 2,
        "roleName": "Operator",
        "permissionType": {
          "bot": [],
          "chat": [],
          "voIP": [],
          "email": [],
          "media": [],
          "settings": [
            "profile"
          ],
          "triggers": [],
          "analytics": [],
          "app-store": [],
          "dashboard": [
            "case",
            "company",
            "contact",
            "field",
            "filter",
            "follow-up",
            "messenger",
            "note",
            "objects",
            "timeline",
            "ui-component",
            "view"
          ],
          "access-level": [],
          "knowledge-base": []
        },
        "meta": {
          "accessLevel": "account"
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

