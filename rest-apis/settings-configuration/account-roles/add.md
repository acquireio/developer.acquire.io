---
description: Add a new role
---

# Add

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/account/role" path="" %}
{% api-method-summary %}
Add
{% endapi-method-summary %}

{% api-method-description %}
Add a new role. The body must contain the keys `roleName` and `permissions`. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{API\_KEY}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="permissions" type="object" required=true %}
Permissions object. Give permission to access features in the platform. 
{% endapi-method-parameter %}

{% api-method-parameter name="roleName" type="string" required=true %}
Name of the role
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
  "roleName": "Agent",
  "permissions": {},
  "meta": {}
}
```

