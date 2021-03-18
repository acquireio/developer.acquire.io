---
description: API to publish or draft by QnA_ID
---

# Publish

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/bot/qna/move/{id}" path="" %}
{% api-method-summary %}
Publish QnA
{% endapi-method-summary %}

{% api-method-description %}
API to publish or draft QnA
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="number" required=true %}
Specify QnA id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
API KEY
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
    "message": "Question Published Successfully",
    "movedId": 3775
  }
}

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

