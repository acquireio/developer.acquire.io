---
description: API to add a new custom attribute to the list of available custom attributes
---

# Add a custom attribute

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/objects/object-field" path="" %}
{% api-method-summary %}
Add Custom Attribute
{% endapi-method-summary %}

{% api-method-description %}
API to add new custom attribute to the list of custom attributes. An object must be passed in to the body of the request.  
 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="object" type="string" required=false %}
The object that the custom attribute will map to
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=false %}
The type of custom attribute
{% endapi-method-parameter %}

{% api-method-parameter name="key" type="string" required=false %}
Name and key of custom attribute
{% endapi-method-parameter %}

{% api-method-parameter name="object" type="object" required=true %}
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

