---
description: API to get the feedback details by it's FEEDBACK_ID
---

# Get Single Feedback

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/feedback/{FEEDBACK\_ID}" path="" %}
{% api-method-summary %}
Get Single Feedback
{% endapi-method-summary %}

{% api-method-description %}
Get the feedback details for the FEEDBACK\_ID specified
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="ID" type="string" required=true %}
Specify ID of the feedback for which you need to get the details
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
\*\*\*\*\*YOUR API KEY\*\*\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="relations" type="object" required=false %}
Specify the relations
{% endapi-method-parameter %}

{% api-method-parameter name="select" type="string" required=false %}
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

