---
description: Update a role
---

# Update

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/account/role/{{roleId}}" path="" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Update a role. The roleId must be passed in to the endpoint as a path parameter.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="roleId" type="integer" required=true %}
ID of the role to be updated
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{API\_KEY}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="permissions" type="object" required=true %}
Permissions object. The features the role will have access to. 
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
  "roleName": "Admin",
  "permissions": {},
  "meta": {},
  "additionalProp1": {}
}
```

