---
description: API to update a specific department by it's ID
---

# Update

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/account/department/14" path="" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
API to update a specific department by it's ID
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
ID specifies the department id to update
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "data": {
    "id": 14,
    "name": "My Depts",
    "status": "active",
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
  "name": "My Depts",
  "status": "active",
  "id": "14"
}
```

