---
description: Update a QnA
---

# Update

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/bot/qna/{{id}}" path="" %}
{% api-method-summary %}
Update QnA
{% endapi-method-summary %}

{% api-method-description %}
Update a QnA. The QnA id must be passed in to the endpoint as a path parameter. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
QnA ID
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
    "message": "Question Updated Successfully",
    "updatedObject": {
      "id": 3781,
      "type": "suggested",
      "subtype": "user_added",
      "status": "active",
      "language": "en",
      "answerType": "random",
      "actionEnabled": "active",
      "wantFeedback": "active",
      "allowRelatedQue": "active",
      "relatedQueIds": "1",
      "createdBy": 1,
      "updatedBy": 1,
      "dateCreated": "2021-03-18T07:13:02.000Z",
      "dateUpdated": "2021-03-18T07:21:57.746Z",
      "qnaMainQuestions": [
        {
          "id": 5777,
          "question": "Test Question 1"
        },
        {
          "id": 5778,
          "question": "Test Question 2"
        }
      ],
      "qnaMainAnswers": [
        {
          "id": 4599,
          "answer": "Test Answer 122",
          "answerJson": null
        },
        {
          "id": 4600,
          "answer": "Test Answer 222",
          "answerJson": null
        }
      ],
      "qnaGroup": {
        "id": 1,
        "title": "Group Title",
        "description": "Group Description",
        "isDefault": "no",
        "askFeedback": "active",
        "cascadeApplicable": "disabled",
        "createdBy": 1,
        "updatedBy": 1,
        "dateCreated": "2020-05-26T07:56:04.000Z",
        "dateUpdated": "2021-03-17T12:06:37.000Z"
      }
    }
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
  "type": "suggested",
  "subtype": "user_added",
  "answerType": "random",
  "status": "active",
  "language": "en",
  "actionEnabled": "active",
  "wantFeedback": "active",
  "allowRelatedQue": "active",
  "relatedQueIds": "1",
  "qnaMainQuestions": [
    {
      "question": "Test Question 1"
    },
    {
      "question": "Test Question 2"
    }
  ],
  "qnaMainAnswers": [
    {
      "answer": "Test Answer 122"
    },
    {
      "answer": "Test Answer 222"
    }
  ],
  "qnaMainActions": []
}

```

