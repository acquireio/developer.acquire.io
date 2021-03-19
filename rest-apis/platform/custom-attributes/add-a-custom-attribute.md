---
description: API to add a new custom attribute to the list of available custom attributes
---

# Add a custom attribute

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/objects/object-field" path="" %}
{% api-method-summary %}
Add Custom Attribute
{% endapi-method-summary %}

{% api-method-description %}
API to add new custom attributes to the list of custom attributes
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
    "object": "string",
    "key": "string",
    "type": "text",
    "config": {},
    "system": "string",
    "id": 35
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
  "object": "string",
  "key": "string",
  "type": "text",
  "config": {},
  "system": "string"
}
```

