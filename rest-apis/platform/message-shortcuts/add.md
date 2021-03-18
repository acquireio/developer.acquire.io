---
description: API to add a new message shortcut
---

# Add

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/message-shortcut?shortcut\_name=test&message=test&messageJson=test%20json" path="" %}
{% api-method-summary %}
Add
{% endapi-method-summary %}

{% api-method-description %}
API to add a new message shortcut
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
API KEY
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
    "shortcut_name": "New shorts",
    "message": "Hello New Shortcuts",
    "id": 36
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
    "shortcut_name":"New shorts",
    "message":"Hello New Shortcuts"
}
```

