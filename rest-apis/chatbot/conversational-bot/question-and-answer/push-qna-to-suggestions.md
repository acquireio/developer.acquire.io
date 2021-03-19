---
description: API to push the QnA to the suggestion list
---

# Push QnA To Suggestions

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/bot/qna/push" path="" %}
{% api-method-summary %}
Push QnA to Suggestions
{% endapi-method-summary %}

{% api-method-description %}
API to push QnA to the suggestion list
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
    "message": "Question merged to existing similar question"
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
  "question": "Test Question",
  "qnaGroupId": 1
}

```

