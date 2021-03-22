---
description: Update specific role by it's ID
---

# Update

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/account/role/{id}" path="" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Update specific role by it's ID
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
ID of the role to be updated
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {api\_key}
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
    "id": 3,
    "roleName": "Higher Master",
    "permissions": [],
    "permissionType": {},
    "meta": {},
    "users": []
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
  "roleName": "Higher Master",
  "permissions": {},
  "meta": {},
  "additionalProp1": {}
}
```

