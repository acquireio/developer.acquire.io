---
description: API to add a new bot group
---

# Add

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/bot/group" path="" %}
{% api-method-summary %}
Add Group
{% endapi-method-summary %}

{% api-method-description %}
Add a new bot group
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
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
Make this group the default \("yes" \| "no"\)
{% endapi-method-parameter %}

{% api-method-parameter name="description" type="string" required=false %}
Description of your bot group
{% endapi-method-parameter %}

{% api-method-parameter name="title" type="string" required=true %}
Title for your bot group
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
    "message": "Group Added successfully.",
    "addedGroup": 2
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
  "title": "Group Title Demo",
  "description": "Group Title Demo",
  "isDefault": "no",
  "askFeedback": "active"
}
```

