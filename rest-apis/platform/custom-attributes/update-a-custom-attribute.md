---
description: API to update a custom attribute fields based on it's ID
---

# Update a custom attribute

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/crm/objects/object-field/33" path="" %}
{% api-method-summary %}
Update Custom Attribute
{% endapi-method-summary %}

{% api-method-description %}
API to update custom attribute fields
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Specify ID of custom attribute to update
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

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
    "id": 33,
    "object": "string",
    "key": "hello",
    "type": "text",
    "config": {},
    "system": "string"
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
  "data": {
    "id": 33,
    "object": "string",
    "key": "hello",
    "type": "text",
    "config": {},
    "system": "string"
  }
}
```

