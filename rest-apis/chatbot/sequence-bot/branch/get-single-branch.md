---
description: API to get the details of the branch sequence by id
---

# Get Single Branch

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/bot/lead/branch/{id}" path="" %}
{% api-method-summary %}
Get Single Branch
{% endapi-method-summary %}

{% api-method-description %}
API to get the details of the branch sequence by id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
API KEY
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
    "success": true,
    "message": "Branch updated successfully"
  }
}

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

