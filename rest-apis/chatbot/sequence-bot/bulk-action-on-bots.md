---
description: API to take bulk action on bots
---

# Bulk Action on bots

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/bot/lead/bulk" path="" %}
{% api-method-summary %}
Bulk Action on bots
{% endapi-method-summary %}

{% api-method-description %}
API to take bulk action on bots
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="" type="string" required=false %}

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
    "message": "Sequences deleted successfully.",
    "lessEventsNotice": true
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
  "actionType": "delete",
  "recordIds": [
    137
  ]
}

```

