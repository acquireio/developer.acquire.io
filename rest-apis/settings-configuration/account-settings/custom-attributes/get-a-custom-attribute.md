---
description: Retrieve a single custom attributeGe
---

# Get a custom Attribute

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/objects/object-field/{{custom\_attributeId}}" path="" %}
{% api-method-summary %}
Get Custom Attribute
{% endapi-method-summary %}

{% api-method-description %}
Get details about a specific custom attribute.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="custom\_attributeId" type="integer" required=true %}
The ID of the custom attribute
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="select" type="array" required=false %}
the array of columns to get
{% endapi-method-parameter %}

{% api-method-parameter name="relations" type="string" required=false %}
specify the relations 
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "data": {
    "id": 1,
    "object": "contact",
    "key": "name",
    "type": "text",
    "config": {
      "input": {
        "type": "text",
        "label": "Name",
        "required": false,
        "placeholder": "",
        "validationType": "format",
        "validationFormat": "any",
        "requiredErrorMessage": "Please add an attribute name.",
        "validationErrorMessage": "Oops! Seems incorrect format that you entered. Can you please recheck your name?"
      },
      "label": "Name",
      "backend": {
        "list": false
      },
      "capture": [
        "api"
      ],
      "online_order": 2,
      "offline_order": 2
    },
    "system": "yes"
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

