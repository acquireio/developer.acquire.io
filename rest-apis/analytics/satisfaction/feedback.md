---
description: See an overview of your visitor and customer feedback.
---

# Feedback

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/satisfaction/feedback" path="" %}
{% api-method-summary %}
Feedback Analytics
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter type="string" name="start\_date" required=true %}
Date From \(Date format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 00:00:00\)
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="end\_date" required=true %}
Date End \(Date Format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 23:59:59\)
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="offset" %}
This parameter is used for the timezone value and the default timezone will be "GMT". e.g. +05:30 for particular timezone. Default is +00:00
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="output" %}
json or csv
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
    "feedback": {
      "data": {
        "graphRow": {
          "labels": [
            "03 PM",
            "04 PM",
            "05 PM",
            "06 PM",
            "07 PM",
            "08 PM",
            "09 PM",
            "10 PM",
            "11 PM",
            "12 AM",
            "01 AM",
            "02 AM",
            "03 AM",
            "04 AM",
            "05 AM",
            "06 AM",
            "07 AM",
            "08 AM",
            "09 AM",
            "10 AM",
            "11 AM",
            "12 PM",
            "01 PM",
            "02 PM"
          ],
          "averageRating": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0
          ]
        },
        "summary": {
          "totalFeedbackCount": {
            "current": 0,
            "previous": 0
          },
          "defaultFeedbackCount": {
            "current": 0,
            "previous": 0
          },
          "customFeedbackCount": {
            "current": 0,
            "previous": 0
          },
          "fiveStarRating": {
            "current": 0,
            "previous": 0
          },
          "fourStarRating": {
            "current": 0,
            "previous": 0
          },
          "threeStarRating": {
            "current": 0,
            "previous": 0
          },
          "twoStarRating": {
            "current": 0,
            "previous": 0
          },
          "oneStarRating": {
            "current": 0,
            "previous": 0
          }
        }
      },
      "success": true,
      "output": "json"
    }
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

