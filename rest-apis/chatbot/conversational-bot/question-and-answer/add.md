---
description: Add a new QnA
---

# Add

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/bot/qna" path="" %}
{% api-method-summary %}
Add QnA
{% endapi-method-summary %}

{% api-method-description %}
Create a new QnA. The body must contain the following parameters:   
  
qnaGroupId - The ID of the group the QnA will be added to.   
  
qnaMainQuestions - An array of objects. Each question object must have a key of "question" with a value of the question you intend to add. Questions may be separated by a comma.   
  
qnaMainAnswers -  An array of objects. Each answer object must have a key of "answer" with a value of the answer you intend to add. Answers may be separated by a comma.   
  
qnaMainActions - An array with a single object. Must have the keys "actionType" and "actionVal". 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="qnaMainActions" type="array" required=true %}
Array of objects. 
{% endapi-method-parameter %}

{% api-method-parameter name="qnaMainAnswers" type="array" required=true %}
Array of objects. Each answer should be written as a string. 
{% endapi-method-parameter %}

{% api-method-parameter name="qnaMainQuestions" type="array" required=true %}
Array of objects. Each question should be written as a string.
{% endapi-method-parameter %}

{% api-method-parameter name="qnaGroupId" type="integer" required=true %}
Group ID that the QnA will be added to
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
    "message": "Question Added Successfully",
    "addedObject": {
      "id": 3781,
      "type": "suggested",
      "subtype": "user_added",
      "status": "active",
      "language": "en",
      "answerType": "random",
      "actionEnabled": "active",
      "wantFeedback": "active",
      "askedCount": 0,
      "allowRelatedQue": "active",
      "relatedQueIds": "1",
      "createdBy": 1,
      "updatedBy": 1,
      "dateCreated": "2021-03-18T07:13:02.390Z",
      "dateUpdated": "2021-03-18T07:13:02.390Z",
      "qnaMainQuestions": [
        {
          "question": "Test Question 1",
          "id": 5773
        },
        {
          "question": "Test Question 2",
          "qnaMain": {
            "type": "suggested",
            "subtype": "user_added",
            "status": "active",
            "language": "en",
            "answerType": "random",
            "actionEnabled": "active",
            "wantFeedback": "active",
            "askedCount": 0,
            "allowRelatedQue": "active",
            "relatedQueIds": "1",
            "createdBy": 1,
            "updatedBy": 1,
            "dateCreated": "2021-03-18T07:13:02.390Z",
            "dateUpdated": "2021-03-18T07:13:02.390Z",
            "qnaMainQuestions": [
              {
                "question": "Test Question 1",
                "id": 5773
              },
              {
                "question": "Test Question 2",
                "id": 5774
              }
            ],
            "qnaMainAnswers": [
              {
                "answer": "Test Answer 1",
                "answerJson": null,
                "id": 4595
              },
              {
                "answer": "Test Answer 2",
                "answerJson": null,
                "id": 4596
              }
            ],
            "qnaMainActions": [
              {
                "parent": null,
                "triggerType": "auto",
                "buttonVal": "",
                "actionType": "follow_up",
                "actionVal": "Test1",
                "id": 182
              }
            ],
            "id": 3781
          },
          "id": 5774
        }
      ],
      "qnaMainAnswers": [
        {
          "answer": "Test Answer 1",
          "answerJson": null,
          "id": 4595
        },
        {
          "answer": "Test Answer 2",
          "answerJson": null,
          "qnaMain": {
            "type": "suggested",
            "subtype": "user_added",
            "status": "active",
            "language": "en",
            "answerType": "random",
            "actionEnabled": "active",
            "wantFeedback": "active",
            "askedCount": 0,
            "allowRelatedQue": "active",
            "relatedQueIds": "1",
            "createdBy": 1,
            "updatedBy": 1,
            "dateCreated": "2021-03-18T07:13:02.390Z",
            "dateUpdated": "2021-03-18T07:13:02.390Z",
            "qnaMainQuestions": [
              {
                "question": "Test Question 1",
                "id": 5773
              },
              {
                "question": "Test Question 2",
                "id": 5774
              }
            ],
            "qnaMainAnswers": [
              {
                "answer": "Test Answer 1",
                "answerJson": null,
                "id": 4595
              },
              {
                "answer": "Test Answer 2",
                "answerJson": null,
                "id": 4596
              }
            ],
            "qnaMainActions": [
              {
                "parent": null,
                "triggerType": "auto",
                "buttonVal": "",
                "actionType": "follow_up",
                "actionVal": "Test1",
                "id": 182
              }
            ],
            "id": 3781
          },
          "id": 4596
        }
      ],
      "tenantId": "r4b4fl"
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
  "qnaGroupId": 1,
  "type": "suggested",
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
      "answer": "Test Answer 1"
    },
    {
      "answer": "Test Answer 2"
    }
  ],
  "qnaMainActions": [
    {
      "actionType": "follow_up",
      "actionVal": "Test1",
      "qnaMainActions": [],
      "triggerType": "auto"
    }
  ]
}

```

