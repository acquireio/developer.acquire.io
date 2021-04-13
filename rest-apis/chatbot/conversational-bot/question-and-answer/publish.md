---
description: Change the status of a QnA
---

# Publish

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/bot/qna/move/{{id}}" path="" %}
{% api-method-summary %}
Publish QnA
{% endapi-method-summary %}

{% api-method-description %}
Publish or draft a QnA. The QnA id must be passed in to the endpoint as a path parameter. If a question is a draft, it will be published. If a question is published, it will be set to draft. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
Specify QnA id
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
    "message": "Question Published Successfully",
    "movedId": 3775
  }
}

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

