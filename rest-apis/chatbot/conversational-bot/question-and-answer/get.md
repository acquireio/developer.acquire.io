---
description: Retrieve a single QnA
---

# Get

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/bot/qna/detail/{{id}}" path="" %}
{% api-method-summary %}
Get
{% endapi-method-summary %}

{% api-method-description %}
Retrieve a single QnA. The QnA id must be passed in to the endpoint as a path parameter.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
Specify ID for the QnA to get the details
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
    "id": 1,
    "type": "live",
    "subtype": "pre_defined",
    "status": "active",
    "language": "en",
    "answerType": "random",
    "actionEnabled": "disabled",
    "wantFeedback": "active",
    "askedCount": 29,
    "allowRelatedQue": "disabled",
    "relatedQueIds": "",
    "createdBy": 1,
    "updatedBy": 1,
    "dateCreated": "2020-06-22T16:17:32.000Z",
    "dateUpdated": "2020-10-18T16:16:35.000Z",
    "qnaMainQuestions": [
      {
        "id": 1,
        "question": "Hi"
      }
    ],
    "qnaMainAnswers": [
      {
        "id": 1,
        "answer": "Hello {{ visitor_name | there }}!",
        "answerJson": null
      }
    ],
    "qnaMainActions": []
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



