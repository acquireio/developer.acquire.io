---
description: Update the branch position
---

# Update Branch Position

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/bot/lead/parent-branch/{{id}}" path="" %}
{% api-method-summary %}
Update Branch Position
{% endapi-method-summary %}

{% api-method-description %}
Update the branch position. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
Specify the branch ID you'd like to update
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="leadId" type="integer" required=true %}
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
  "leadId": 926,
  "currentPos": {
    "x": 22,
    "y": 30
  }
}

```

