---
description: API to update a sequence branch
---

# Update

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/bot/lead/branch/{id}" path="" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
API to update a sequence branch
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="number" required=true %}

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
    "message": "Branch updated successfully"
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
  "id": 926,
  "leadId": 138,
  "data": {
    "title": "Welcome Branch"
  }
}

```

