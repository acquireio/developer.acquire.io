---
description: Add a feedback question
---

# Add feedback

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/feedback" path="" %}
{% api-method-summary %}
Add Feedback
{% endapi-method-summary %}

{% api-method-description %}
Create feedback. The body requires keys of `"question"`, `"status"`, `"type"`, `"config"`, `"departments"`, and `"channels"`.   
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="channels" type="string" required=true %}
The channel that feedback will display on: "sms", "email", "chat"
{% endapi-method-parameter %}

{% api-method-parameter name="departments" type="array" required=true %}
Array of integers. The departments that will receive the feedback. 
{% endapi-method-parameter %}

{% api-method-parameter name="config" type="string" required=true %}
The values, requirements, and error messages for the feedback
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
The type of feedback question: "rating","text", "multiple\_radio", "multiple\_checkbox"
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="string" required=true %}
"active" \| "disabled"
{% endapi-method-parameter %}

{% api-method-parameter name="question" type="string" required=true %}
The question for the feedback
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
    "question": "How satisfied are you with our products/services?",
    "status": "active",
    "type": "rating",
    "config": {
      "error_message": "Invalid Input",
      "required": true,
      "rating_type": "star",
      "limit": 1,
      "multiline": false,
      "values": [
        {
          "icon": "settings/feedback-5.svg",
          "label": "LIKE",
          "value": "5"
        }
      ]
    },
    "departments": [
      1
    ],
    "channels": [
      "chat"
    ],
    "dateCreated": "2021-03-18T07:41:18.341Z",
    "id": 37
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
  "question": "How satisfied are you with our products/services?",
  "status": "active",
  "type": "rating",
  "config": {
    "error_message": "Invalid Input",
    "required": true,
    "rating_type": "star",
    "limit": 1,
    "multiline": false,
    "values": [
      {
        "icon": "settings/feedback-5.svg",
        "label": "LIKE",
        "value": "5"
      }
    ]
  },
  "departments": [
    1
  ],
  "channels": [
    "chat"
  ]
}
```

