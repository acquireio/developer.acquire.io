---
description: API to update a specific message shortcut
---

# Update

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/crm/message-shortcut/36?shortcut\_name=test&messageJson=test%20json" path="" %}
{% api-method-summary %}
Update Shortcut
{% endapi-method-summary %}

{% api-method-description %}
API to update a specific shortcut
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="number" required=true %}
Specify ID of shortcut to be updated
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
    "shortcut_name":"New shorts Whistle",
    "message":"Hello New Meessages Shortcuts"
}
```

