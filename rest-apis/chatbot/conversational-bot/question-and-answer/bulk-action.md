---
description: Take bulk action on QnAs
---

# Bulk Action

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/bot/qna/bulk" path="" %}
{% api-method-summary %}
Bulk Update
{% endapi-method-summary %}

{% api-method-description %}
API to take bulk action on QnA
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
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
    "message": "Questions deleted successfully",
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
    3773, 3752
  ],
  "targetGroup": [
    "1"
  ]
}

```

