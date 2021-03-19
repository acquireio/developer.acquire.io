---
description: API to set the parent branch
---

# Set as Parent Branch

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/bot/lead/parent-branch/{id}" path="" %}
{% api-method-summary %}
Set as Parent Branch
{% endapi-method-summary %}

{% api-method-description %}
API to set the parent branch
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Specify branch id
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
    "message": "Branch marked as parent successfully."
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
  "leadId": 138
}

```

