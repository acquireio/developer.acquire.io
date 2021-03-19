---
description: API to reorder branch sequence
---

# Reorder Branch In Sequence

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/bot/lead/reorder/{id}" path="" %}
{% api-method-summary %}
Reorder Branch In Sequence
{% endapi-method-summary %}

{% api-method-description %}
API to reorder branch sequence
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="number" required=true %}
Specify Id of the branch
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
    "Message": "Branch ordered successfully"
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
  "data": [
    926, 924, 925, 923, 922, 921, 920
  ]
}

```

