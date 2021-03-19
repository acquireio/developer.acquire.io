# Others Rating

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api" path="/v1/analytics/satisfaction/radio-feedback?start\_date=2020-03-16%2015%3A44%3A07&end\_date=2021-03-17%2015%3A44%3A06&output=json&offset=%2B00%3A00" %}
{% api-method-summary %}
Radio
{% endapi-method-summary %}

{% api-method-description %}

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

{% api-method-parameter type="string" name="end\_date" required=true %}
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
    "radioFeedback": {
      "data": {
        "graphRow": {
          "data": [
            {
              "label": "Radio type Feedback - 1",
              "options": [
                {
                  "label": "First",
                  "value": "first",
                  "count": 2
                },
                {
                  "label": "Second",
                  "value": "second",
                  "count": 5
                },
                {
                  "label": "Third",
                  "value": "third",
                  "count": 1
                }
              ]
            },
            {
              "label": "Radio 21",
              "options": [
                {
                  "label": "R11",
                  "value": "r11",
                  "count": 1
                },
                {
                  "label": "R21",
                  "value": "r21",
                  "count": 1
                },
                {
                  "label": "R31",
                  "value": "r31",
                  "count": 1
                }
              ]
            }
          ]
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

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api" path="/v1/analytics/satisfaction/checkbox-feedback?start\_date=2020-03-16%2015%3A44%3A07&end\_date=2021-03-17%2015%3A44%3A06&output=json&offset=%2B00%3A00" %}
{% api-method-summary %}
Checkbox
{% endapi-method-summary %}

{% api-method-description %}

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

{% api-method-parameter type="string" name="end\_date" required=true %}
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
    "checkboxFeedback": {
      "data": {
        "graphRow": {
          "data": [
            {
              "id": 4,
              "label": "Checkbox1",
              "options": {
                "4": {
                  "count": 0,
                  "label": "4",
                  "value": "4"
                },
                "5": {
                  "count": 0,
                  "label": "5",
                  "value": "5"
                },
                "6": {
                  "count": 1,
                  "label": "6",
                  "value": "6"
                },
                "7": {
                  "count": 1,
                  "label": "7",
                  "value": "7"
                },
                "8": {
                  "count": 0,
                  "label": "8",
                  "value": "8"
                },
                "9": {
                  "count": 0,
                  "label": "9",
                  "value": "9"
                },
                "10": {
                  "count": 1,
                  "label": "10",
                  "value": "10"
                },
                "first": {
                  "count": 0,
                  "label": "First",
                  "value": "first"
                },
                "second": {
                  "count": 5,
                  "label": "Second",
                  "value": "second"
                },
                "third": {
                  "count": 2,
                  "label": "Third",
                  "value": "third"
                }
              }
            },
            {
              "id": 10,
              "label": "Checkbox 2",
              "options": {
                "c1": {
                  "count": 1,
                  "label": "C1",
                  "value": "c1"
                },
                "c2": {
                  "count": 4,
                  "label": "C2",
                  "value": "c2"
                },
                "c3_update": {
                  "count": 0,
                  "label": "C3 update",
                  "value": "c3_update"
                }
              }
            }
          ]
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

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api" path="/v1/analytics/satisfaction/text-feedback?start\_date=2020-03-16%2015%3A44%3A07&end\_date=2021-03-17%2015%3A44%3A06&output=json&offset=%2B00%3A00" %}
{% api-method-summary %}
Text
{% endapi-method-summary %}

{% api-method-description %}

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

{% api-method-parameter type="string" name="end\_date" required=true %}
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
    "textFeedback": {
      "data": {
        "graphRow": {
          "data": [
            {
              "label": "Text Feedback",
              "answer": "asd",
              "visitor": "feedback test"
            },
            {
              "label": "Text Feedback",
              "answer": "ss",
              "visitor": "feedback test"
            },
            {
              "label": "Text Feedback",
              "answer": "",
              "visitor": "--"
            },
            {
              "label": "Text Feedback",
              "answer": "dddddd",
              "visitor": "--"
            },
            {
              "label": "Text Feedback",
              "answer": "sdf",
              "visitor": "--"
            },
            {
              "label": "Text Feedback",
              "answer": "adfsdf",
              "visitor": "kaushal"
            }
          ]
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

