---
description: Import QnA
---

# Import QnA

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/bot/qna/import" path="" %}
{% api-method-summary %}
Importing QnA
{% endapi-method-summary %}

{% api-method-description %}
Import QnA
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="qnaGroupId" type="integer" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="qnaSource" type="string" required=true %}

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
    "message": "Question Imported Successfully"
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
  "language": "en",
  "sourceLang": "en",
  "qnaGroupId": 1,
  "qnaSource": "acquire",
  "qnaPairs": [
    {
      "questions": "Test Question 1",
      "answerType": "random",
      "answers": [
        "Test Answer 1",
        "Test Answer 2",
        "Test Answer 3"
      ]
    },
    {
      "questions": "Test Question 2",
      "answerType": "random",
      "answers": [
        "-same-"
      ]
    }
  ],
  "serviceJSON": {}
}

```
