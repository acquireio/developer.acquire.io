---
description: Create a question and set its status to draft.
---

# Push QnA To Suggestions

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/bot/qna/push" path="" %}
{% api-method-summary %}
Push QnA to Suggestions
{% endapi-method-summary %}

{% api-method-description %}
Create a QnA and set its status to draft. If a similar question exists within the group, the added question will be merged to that QnA group. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="qnaGroupId" type="integer" required=false %}
The ID of the group you'd like to add the question to. 
{% endapi-method-parameter %}

{% api-method-parameter name="question" type="string" required=true %}
A question you want to add to your Conversational Bot 
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

