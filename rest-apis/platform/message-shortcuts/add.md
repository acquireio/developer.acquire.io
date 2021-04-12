---
description: Add a new message shortcut.
---

# Add

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/message-shortcut" path="" %}
{% api-method-summary %}
Add
{% endapi-method-summary %}

{% api-method-description %}
Add a new message shortcut. During a conversation, the message is displayed when you hit the shortcut key. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="shortcut\_name" type="string" required=false %}
The shortcut's name
{% endapi-method-parameter %}

{% api-method-parameter name="message" type="string" required=true %}
The shortcut's message
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

