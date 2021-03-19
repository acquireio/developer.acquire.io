---
description: API to copy a group
---

# Copy

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/bot/group/copy" path="" %}
{% api-method-summary %}
Copy
{% endapi-method-summary %}

{% api-method-description %}
API to copy a group
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
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
    "success": true,
    "message": "Group is being copied .."
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
  "id": 1
}
```

