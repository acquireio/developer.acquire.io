# Update Feedback

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/crm/feedback/{{feedbackId}}" path="" %}
{% api-method-summary %}
Update Feedback
{% endapi-method-summary %}

{% api-method-description %}
Update feedback. The **feedbackId** must be passed in to the endpoint as a path parameter. The body requires keys of `"question"`, `"status"`, `"type"`, `"config"`, `"departments"`, and `"channels"`. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="feedbackId" type="integer" required=true %}
The feedback's ID
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
    "id": 36,
    "question": "How satisfied are you with our products?",
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
    "dateCreated": "2021-03-18T07:41:18.000Z",
    "status": "active"
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
  "id": "36",
  "question": "How satisfied are you with our products?",
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

