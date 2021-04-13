---
description: Delete a QnA
---

# Delete

{% api-method method="delete" host="https://{{account\_id}}.acquire.io/api/v1/bot/qna/{{id}}" path="" %}
{% api-method-summary %}
Delete QnA
{% endapi-method-summary %}

{% api-method-description %}
Delete a QnA. The QnA `"id"` must be passed in to the endpoint as a path parameter. **Warning**: This action cannot be undone. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
Specify the QnA id to delete
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
    "message": "Question Deleted Successfully",
    "delId": 3776
  }
}

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



