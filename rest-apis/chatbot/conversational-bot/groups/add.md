---
description: API to add a new bot group
---

# Add

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/bot/group" path="" %}
{% api-method-summary %}
Add Group
{% endapi-method-summary %}

{% api-method-description %}
API to add a new bot group
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
YOUR API KEY
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

