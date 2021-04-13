---
description: Update a sequence branch.
---

# Update

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/bot/lead/branch/{{id}}" path="" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Update a sequence branch. The branch ID must be passed in to the endpoint as a path parameter and into the body as "id". 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the branch you'd like to update
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="title" type="string" required=false %}
The title of the branch
{% endapi-method-parameter %}

{% api-method-parameter name="data" type="object" required=false %}
Data object
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="integer" required=true %}
The ID of the branch you'd like to update
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

