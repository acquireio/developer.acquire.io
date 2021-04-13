---
description: Update bot group
---

# Update

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/bot/group/{id}" path="" %}
{% api-method-summary %}
Update Group
{% endapi-method-summary %}

{% api-method-description %}
Update a Conversational Bot group's details.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
GroupID to be updated
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="askFeedback" type="string" required=false %}
Have the bot ask for feedback \("active" \| "disabled"\)
{% endapi-method-parameter %}

{% api-method-parameter name="isDefault" type="string" required=false %}
Make group the default \("yes" \| "no"\)
{% endapi-method-parameter %}

{% api-method-parameter name="description" type="string" required=false %}
Description for group
{% endapi-method-parameter %}

{% api-method-parameter name="title" type="string" required=false %}
Title for group
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
    "message": "Group Updated Successfully."
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
  "description": "Group Description",
  "title": "Group Title",
  "isDefault": "no",
  "askFeedback": "active"
}
```

