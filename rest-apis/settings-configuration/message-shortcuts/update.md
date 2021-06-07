---
description: Update a specific message shortcut.
---

# Update

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/crm/message-shortcut/{{shortcutId}}" path="" %}
{% api-method-summary %}
Update Shortcut
{% endapi-method-summary %}

{% api-method-description %}
Update a specific shortcut. The **shortcutId** must passed in to the endpoint as a path parameter.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="shortcutId" type="integer" required=true %}
Shortcut's ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

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
    "id": 36,
    "shortcut_name": "New shorts Whistle",
    "type": null,
    "message": "",
    "messageJson": null,
    "messageHtml": "",
    "department": null,
    "groupName": null
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

```text
{
    "shortcut_name":"New Whistle",
    "message":"Hello New Messages Shortcuts"
}
```

