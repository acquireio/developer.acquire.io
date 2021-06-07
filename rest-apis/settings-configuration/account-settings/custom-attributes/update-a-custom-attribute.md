---
description: Update a custom attribute
---

# Update a custom attribute

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/crm/objects/object-field/{{custom\_attributeId}}" path="" %}
{% api-method-summary %}
Update Custom Attribute
{% endapi-method-summary %}

{% api-method-description %}
Update a custom attribute. The **custom\_attributeId** must be passed in to the endpoint as a path parameter. An object must be passed in to the body of the request.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="custom\_attributeId" type="integer" required=true %}
The ID of custom attribute
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="object" type="string" required=true %}
Body object
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
    "key": "loyalty_number",
    "type": "text",
    "config": {},
    "system": "string"
  }
}
```

