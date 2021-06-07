---
description: Retrieve a single feedback question
---

# Get single feedback

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/feedback/{{feedbackId}}" path="" %}
{% api-method-summary %}
Get Single Feedback
{% endapi-method-summary %}

{% api-method-description %}
Retrieve a single feedback question. The **feedbackId** must be passed in to the endpoint as a path parameter.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="feedbackId" type="integer" required=true %}
The ID of the feedback
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="relations" type="object" required=false %}
Specify the relation to "case" or "contact"
{% endapi-method-parameter %}

{% api-method-parameter name="select" type="array" required=false %}
Specify the selected fields
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "data": {
    "id": 36,
    "question": "How satisfied?",
    "type": "rating",
    "config": {
      "values": [
        {
          "icon": "settings/feedback-5.svg",
          "label": "DISLIKE",
          "value": "5"
        }
      ],
      "required": true,
      "rating_type": "star",
      "error_message": "Invalid Input"
    },
    "departments": [],
    "channels": [
      "email"
    ],
    "dateCreated": "2021-03-17T04:27:48.000Z",
    "status": "active"
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

