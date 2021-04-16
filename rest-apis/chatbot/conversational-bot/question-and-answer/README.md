---
description: >-
  Conversational Bots collect visitor questions and answer (QnA) them using
  agent or AI-created answers.
---

# Question And Answer

### Attributes 

| ATTRIBUTE | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| id | Integer | Specify the ID of the QnA. |
| type | String | Specify if QnA is published or not. |
| subtype | String | Specify the source of the QnA. |
| language | String | Specify the language of the QnA. |
| answerType | String | Specify the among random, formatted or article. |
| actionEnabled | String | Specify if post actions should be triggered or not. |
| wantFeedback | String | Specify to show upvote/downvote thumbs on the visitor side. |
| allowRelatedQue | String | Specify if you want to show related questions. |
| relatedQueIds | String | Specify related questions with comma-separated. |
| createdBy | Integer | Specify the owner or created user. |
| updatedBy | Integer | Specify the updated by user id. |
| dateCreated | datetime | Specify the creation of the QnA date stamp. |
| dateUpdated | datetime | Specify the update of the QnA date stamp. |
| qnaMainQuestions | JSON Array Object | Specify the Questions collection |
| qnaMainAnswers | JSON Array Object | Specify the Answers collection. |

### Permissions

To request a QnA endpoint, you will need a valid API Key with conversational chatbot QnA access permissions.

