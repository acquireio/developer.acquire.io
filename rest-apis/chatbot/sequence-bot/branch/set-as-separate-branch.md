---
description: Set the parent branch
---

# Set as Parent Branch

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/bot/lead/parent-branch/{{branchId}}" path="" %}
{% api-method-summary %}
Set as Parent Branch
{% endapi-method-summary %}

{% api-method-description %}
Set the parent branch. The child branch \(`branchId`\) must be passed through the endpoint as a path parameter. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="branchId" type="integer" required=true %}
Specify branch id for child branch
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="leadId" type="integer" required=true %}
Specify branch id for parent branch
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
  "leadId": 138
}

```

