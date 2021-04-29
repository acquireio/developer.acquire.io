---
description: Add a new role
---

# Add

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/account/role" path="" %}
{% api-method-summary %}
Add
{% endapi-method-summary %}

{% api-method-description %}
Add a new role
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {api\_Key}
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
    "roleName": "MyMaster",
    "meta": {},
    "permissionType": {},
    "id": 3
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
  "roleName": "MyMaster",
  "permissions": {},
  "meta": {}
}
```

