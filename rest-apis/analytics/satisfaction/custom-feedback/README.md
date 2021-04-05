# Custom Feedback

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/satisfaction/overview" path="" %}
{% api-method-summary %}
Overview
{% endapi-method-summary %}

{% api-method-description %}
Reporting on all varieties of feedback implemented.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter type="string" name="Authorization" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="start\_date" type="string" required=true %}
Date From \(Date format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 00:00:00\)
{% endapi-method-parameter %}

{% api-method-parameter name="end\_date" required=true type="string" %}
Date End \(Date Format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 23:59:59\)
{% endapi-method-parameter %}

{% api-method-parameter name="offset" type="string" %}
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
    "overview": {
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
          "totalCustomFeedback": [
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
          ],
          "thumbRating": [
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
          ],
          "checkboxFeedback": [
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
          ],
          "radioButtonFeedback": [
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
          ],
          "textFeedback": [
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
          "totalCustomFeedback": {
            "current": 0
          },
          "thumbRating": {
            "current": 0,
            "previous": 0
          },
          "checkboxFeedback": {
            "current": 0,
            "previous": 0
          },
          "radioButtonFeedback": {
            "current": 0,
            "previous": 0
          },
          "textFeedback": {
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

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/satisfaction/number-rating" path="" %}
{% api-method-summary %}
Numbers Rating
{% endapi-method-summary %}

{% api-method-description %}
Reporting on all varieties of feedback implemented.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter type="string" name="Authorization" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="start\_date" type="string" required=true %}
Date From \(Date format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 00:00:00\)
{% endapi-method-parameter %}

{% api-method-parameter name="end\_date" required=true type="string" %}
Date End \(Date Format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 23:59:59\)
{% endapi-method-parameter %}

{% api-method-parameter name="offset" type="string" %}
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
    "numberRating": {
      "data": [
        {
          "id": 7,
          "question": "Rating - Number",
          "question_limit": "5",
          "answer": "3",
          "channel": "chat",
          "channels": "[\"chat\", \"sms\", \"email\"]",
          "answers": {
            "3": {
              "count": 4,
              "email": 0,
              "chat": 4,
              "sms": 0
            },
            "4": {
              "count": 1,
              "email": 0,
              "chat": 1,
              "sms": 0
            }
          }
        }
      ],
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

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/satisfaction/star-rating" path="" %}
{% api-method-summary %}
Star Rating
{% endapi-method-summary %}

{% api-method-description %}
Reporting on all varieties of feedback implemented.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter type="string" name="Authorization" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="start\_date" type="string" required=true %}
Date From \(Date format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 00:00:00\)
{% endapi-method-parameter %}

{% api-method-parameter name="end\_date" required=true type="string" %}
Date End \(Date Format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 23:59:59\)
{% endapi-method-parameter %}

{% api-method-parameter name="offset" type="string" %}
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
    "starRating": {
      "data": [
        {
          "id": 1,
          "question": "How was your conversation with us today?",
          "q_options": "[{\"icon\": \"settings/feedback-1.png\", \"label\": \"TERRIBLE\", \"value\": \"1\"}, {\"icon\": \"settings/feedback-2.png\", \"label\": \"BAD\", \"value\": \"2\"}, {\"icon\": \"settings/feedback-3.png\", \"label\": \"FAIR\", \"value\": \"3\"}, {\"icon\": \"settings/feedback-4.png\", \"label\": \"LIKE IT\", \"value\": \"4\"}, {\"icon\": \"settings/feedback-5.png\", \"label\": \"LOVE IT\", \"value\": \"5\"}]",
          "answer": "5",
          "channel": "chat",
          "channels": "[\"chat\", \"sms\", \"email\"]",
          "answers": {
            "2": {
              "count": 1,
              "email": 0,
              "chat": 1,
              "sms": 0
            },
            "3": {
              "count": 11,
              "email": 0,
              "chat": 11,
              "sms": 0
            },
            "4": {
              "count": 7,
              "email": 0,
              "chat": 7,
              "sms": 0
            },
            "5": {
              "count": 2,
              "email": 0,
              "chat": 2,
              "sms": 0
            }
          }
        },
        {
          "id": 2,
          "question": "Rating Analytics Test",
          "q_options": "[{\"icon\": \"settings/feedback-1.png\", \"label\": \"Very bad\", \"value\": \"1\"}, {\"icon\": \"settings/feedback-2.png\", \"label\": \"Bad\", \"value\": \"2\"}, {\"icon\": \"settings/feedback-3.png\", \"label\": \"Average\", \"value\": \"3\"}, {\"icon\": \"settings/feedback-4.png\", \"label\": \"Good\", \"value\": \"4\"}, {\"icon\": \"settings/feedback-5.png\", \"label\": \"Very good\", \"value\": \"5\"}]",
          "answer": "4",
          "channel": "chat",
          "channels": "[\"chat\", \"email\", \"sms\"]",
          "answers": {
            "3": {
              "count": 2,
              "email": 0,
              "chat": 2,
              "sms": 0
            },
            "4": {
              "count": 5,
              "email": 0,
              "chat": 5,
              "sms": 0
            }
          }
        },
        {
          "id": 8,
          "question": "Image - Feedback",
          "q_options": "[{\"key\": \"WzEzOCwibWVkaWEvMjAyMC8xMi9BdmljY2ktY2RlMGViZjc0MWRkYzkzYmIwODcwOWQ2LnBuZyIsIjR3aWM0ZSIsIkF2aWNjaS5wbmciLDE0OTQ1MzBd\", \"icon\": \"\", \"label\": \"A\", \"value\": \"1\"}, {\"key\": \"WzEzOSwibWVkaWEvMjAyMC8xMi9hOWY0ZDU3Mi02MmJkLTQ1OTAtYjMwYy02MDEyNDI4YTlmODQtNmFhYWYyZmFhMzhhOTgzMGI4NzE0YTgzLmpwZyIsIjR3aWM0ZSIsImE5ZjRkNTcyLTYyYmQtNDU5MC1iMzBjLTYwMTI0MjhhOWY4NC5qcGciLDY0NzIwXQ==\", \"icon\": \"\", \"label\": \"B\", \"value\": \"2\"}, {\"key\": \"WzE0MCwibWVkaWEvMjAyMC8xMi81YjhkYTg2YWMzMzM4M2U1ZDk0ODBhY2YzZTE0YjA4OC0yOTg0ZmJlZWU5ZDllMTZjMmZlMDFhOGMuanBnIiwiNHdpYzRlIiwiNWI4ZGE4NmFjMzMzODNlNWQ5NDgwYWNmM2UxNGIwODguanBnIiwxMDgxNDdd\", \"icon\": \"\", \"label\": \"G\", \"value\": \"3\"}]",
          "answer": "1",
          "channel": "chat",
          "channels": "[]",
          "answers": {
            "1": {
              "count": 1,
              "email": 0,
              "chat": 1,
              "sms": 0
            },
            "2": {
              "count": 2,
              "email": 0,
              "chat": 2,
              "sms": 0
            }
          }
        }
      ],
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

