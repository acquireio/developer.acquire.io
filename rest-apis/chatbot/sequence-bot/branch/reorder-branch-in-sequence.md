---
description: Reorder branch sequence
---

# Reorder Branch In Sequence

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/bot/lead/reorder/{{id}}" path="" %}
{% api-method-summary %}
Reorder Branch In Sequence
{% endapi-method-summary %}

{% api-method-description %}
Reorder branch sequence. The Sequence Bot `id` must be passed in to the endpoint as a path parameter. The body must contain a `data` object. To reorder the branches, set the opening  branch ID at position 0 of the data array. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
Sequence bot ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="data" type="array" required=true %}
Array of branch IDs.
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

