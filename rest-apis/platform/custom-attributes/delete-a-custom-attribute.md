---
description: API to delete custom attributes
---

# Delete a custom attribute

{% api-method method="delete" host="https://{{account\_id}}.acquire.io/api/v1/crm/objects/object-field/{{custom\_attributeId}}" path="" %}
{% api-method-summary %}
Delete a custom attribute
{% endapi-method-summary %}

{% api-method-description %}
Delete a specific custom attribute. The custom\_attributeId must be passed in to the endpoint as a path parameter. **Warning:** This action can't be undone. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="custom\_attributeId" type="integer" required=true %}
The custom attribute's ID
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
    "deleted": 1
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

