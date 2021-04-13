---
description: Delete sequence branch
---

# Delete

{% api-method method="delete" host="https://{{account\_id}}.acquire.io/api/v1/bot/lead/branch/{{id}}" path="" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
API to delete sequence branch. The branch ID must be passed in to the endpoint as a path parameter. **Warning**: This action cannot be undone. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the branch you would like to delete
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
    "success": true,
    "message": "Branch deleted successfully."
  }
}

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

