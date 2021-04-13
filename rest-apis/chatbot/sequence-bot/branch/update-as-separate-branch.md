---
description: API to update a parent branch
---

# Update as Parent branch

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/bot/lead/parent-branch/{id}" path="" %}
{% api-method-summary %}
Update as Parent branch
{% endapi-method-summary %}

{% api-method-description %}
API to update a parent branch. The child branch `id` must be passed in to the endpoint as a path parameter.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
Specify branch ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
Parent branch ID
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "data": true
}

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Body\(raw\)

```text
{
  "id": 926,
  "currentPos": {
    "x": 22,
    "y": 30
  }
}

```

