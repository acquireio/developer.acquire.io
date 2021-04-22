# Overview

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/chat/chat-overview" path="" %}
{% api-method-summary %}
Overview
{% endapi-method-summary %}

{% api-method-description %}
Retrieve overview data for chat.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="start\_date" type="string" required=true %}
Date From \(Date format = YYYY-MM-
{% endapi-method-parameter %}

{% api-method-parameter name="start\_date" type="string" required=true %}
DD hh:mm:ss, e.g 2021-01-01 00:00:00\)
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="end\_date" required=true %}
Date End \(Date Format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 23:59:59\)
{% endapi-method-parameter %}

{% api-method-parameter name="offset" type="string" %}
This parameter is used for the timezone value and the default timezone will be "GMT". e.g. +05:30 for particular timezone. Default is +00:00
{% endapi-method-parameter %}

{% api-method-parameter name="output" type="string" %}
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
    "chatOverview": {
      "data": {
        "graphRow": {
          "labels": [
            "05 AM",
            "06 AM",
            "07 AM",
            "08 AM",
            "09 AM",
            "10 AM",
            "11 AM",
            "12 PM",
            "01 PM",
            "02 PM",
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
            "04 AM"
          ],
          "totalChats": [
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
          "totalAnsweredChats": [
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
          "totalOfflineChats": [
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
          "totalMissedChats": [
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
          "averageResponseTime": [
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
          "totalChats": {
            "current": 0,
            "previous": 0
          },
          "totalAnsweredChats": {
            "current": 0,
            "previous": 0
          },
          "totalOfflineChats": {
            "current": 0,
            "previous": 0
          },
          "totalMissedChats": {
            "current": 0,
            "previous": 0
          },
          "averageResponseTime": {
            "current": 0,
            "previous": 0
          },
          "averageChatTime": {
            "current": 0,
            "previous": 0
          },
          "averageRating": {
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

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/chat/chat-handle-time" path="" %}
{% api-method-summary %}
Chat Handle Time
{% endapi-method-summary %}

{% api-method-description %}
Retrieve data for chat handle time.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

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

{% api-method-parameter name="output" type="string" %}
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
    "chatHandleTime": {
      "data": {
        "graphRow": {
          "labels": [
            "05 AM",
            "06 AM",
            "07 AM",
            "08 AM",
            "09 AM",
            "10 AM",
            "11 AM",
            "12 PM",
            "01 PM",
            "02 PM",
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
            "04 AM"
          ],
          "zeroToThirty": [
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
          "thirtyToTwo": [
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
          "twoToFive": [
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
          "fiveOrMore": [
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
          "averageHandlingTime": [
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
          "zeroToThirty": {
            "current": 0,
            "previous": 0
          },
          "thirtyToTwo": {
            "current": 0,
            "previous": 0
          },
          "twoToFive": {
            "current": 0,
            "previous": 0
          },
          "fiveOrMore": {
            "current": 0,
            "previous": 0
          },
          "totalHandlingTime": {
            "current": 0,
            "previous": 0,
            "info": "The total amount of time your team spent on chats during the selected period."
          },
          "averageHandlingTime": {
            "current": null,
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

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api//v1/analytics/chat/busiest-periods-chats" path="" %}
{% api-method-summary %}
Busiest Periods for Inbound Chats
{% endapi-method-summary %}

{% api-method-description %}
Retrieve data for busiest period for inbound chats.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

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

{% api-method-parameter name="output" type="string" %}
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
    "busiestPeriodsChats": {
      "data": {
        "graphRow": {
          "data": [
            {
              "label": "05 AM",
              "00 AM": 0,
              "02 AM": 0,
              "04 AM": 0,
              "06 AM": 0,
              "08 AM": 0,
              "10 AM": 0,
              "12 PM": 0,
              "14 PM": 0,
              "16 PM": 0,
              "18 PM": 0,
              "20 PM": 0,
              "22 PM": 0
            },
            {
              "label": "06 AM",
              "00 AM": 0,
              "02 AM": 0,
              "04 AM": 0,
              "06 AM": 0,
              "08 AM": 0,
              "10 AM": 0,
              "12 PM": 0,
              "14 PM": 0,
              "16 PM": 0,
              "18 PM": 0,
              "20 PM": 0,
              "22 PM": 0
            },
            {
              "label": "07 AM",
              "00 AM": 0,
              "02 AM": 0,
              "04 AM": 0,
              "06 AM": 0,
              "08 AM": 0,
              "10 AM": 0,
              "12 PM": 0,
              "14 PM": 0,
              "16 PM": 0,
              "18 PM": 0,
              "20 PM": 0,
              "22 PM": 0
            },
            {
              "label": "08 AM",
              "00 AM": 0,
              "02 AM": 0,
              "04 AM": 0,
              "06 AM": 0,
              "08 AM": 0,
              "10 AM": 0,
              "12 PM": 0,
              "14 PM": 0,
              "16 PM": 0,
              "18 PM": 0,
              "20 PM": 0,
              "22 PM": 0
            },
            {
              "label": "09 AM",
              "00 AM": 0,
              "02 AM": 0,
              "04 AM": 0,
              "06 AM": 0,
              "08 AM": 0,
              "10 AM": 0,
              "12 PM": 0,
              "14 PM": 0,
              "16 PM": 0,
              "18 PM": 0,
              "20 PM": 0,
              "22 PM": 0
            },
            {
              "label": "10 AM",
              "00 AM": 0,
              "02 AM": 0,
              "04 AM": 0,
              "06 AM": 0,
              "08 AM": 0,
              "10 AM": 0,
              "12 PM": 0,
              "14 PM": 0,
              "16 PM": 0,
              "18 PM": 0,
              "20 PM": 0,
              "22 PM": 0
            },
            {
              "label": "11 AM",
              "00 AM": 0,
              "02 AM": 0,
              "04 AM": 0,
              "06 AM": 0,
              "08 AM": 0,
              "10 AM": 0,
              "12 PM": 0,
              "14 PM": 0,
              "16 PM": 0,
              "18 PM": 0,
              "20 PM": 0,
              "22 PM": 0
            },
            {
              "label": "12 PM",
              "00 AM": 0,
              "02 AM": 0,
              "04 AM": 0,
              "06 AM": 0,
              "08 AM": 0,
              "10 AM": 0,
              "12 PM": 0,
              "14 PM": 0,
              "16 PM": 0,
              "18 PM": 0,
              "20 PM": 0,
              "22 PM": 0
            },
            {
              "label": "01 PM",
              "00 AM": 0,
              "02 AM": 0,
              "04 AM": 0,
              "06 AM": 0,
              "08 AM": 0,
              "10 AM": 0,
              "12 PM": 0,
              "14 PM": 0,
              "16 PM": 0,
              "18 PM": 0,
              "20 PM": 0,
              "22 PM": 0
            },
            {
              "label": "02 PM",
              "00 AM": 0,
              "02 AM": 0,
              "04 AM": 0,
              "06 AM": 0,
              "08 AM": 0,
              "10 AM": 0,
              "12 PM": 0,
              "14 PM": 0,
              "16 PM": 0,
              "18 PM": 0,
              "20 PM": 0,
              "22 PM": 0
            },
            {
              "label": "03 PM",
              "00 AM": 0,
              "02 AM": 0,
              "04 AM": 0,
              "06 AM": 0,
              "08 AM": 0,
              "10 AM": 0,
              "12 PM": 0,
              "14 PM": 0,
              "16 PM": 0,
              "18 PM": 0,
              "20 PM": 0,
              "22 PM": 0
            },
            {
              "label": "04 PM",
              "00 AM": 0,
              "02 AM": 0,
              "04 AM": 0,
              "06 AM": 0,
              "08 AM": 0,
              "10 AM": 0,
              "12 PM": 0,
              "14 PM": 0,
              "16 PM": 0,
              "18 PM": 0,
              "20 PM": 0,
              "22 PM": 0
            },
            {
              "label": "05 PM",
              "00 AM": 0,
              "02 AM": 0,
              "04 AM": 0,
              "06 AM": 0,
              "08 AM": 0,
              "10 AM": 0,
              "12 PM": 0,
              "14 PM": 0,
              "16 PM": 0,
              "18 PM": 0,
              "20 PM": 0,
              "22 PM": 0
            },
            {
              "label": "06 PM",
              "00 AM": 0,
              "02 AM": 0,
              "04 AM": 0,
              "06 AM": 0,
              "08 AM": 0,
              "10 AM": 0,
              "12 PM": 0,
              "14 PM": 0,
              "16 PM": 0,
              "18 PM": 0,
              "20 PM": 0,
              "22 PM": 0
            },
            {
              "label": "07 PM",
              "00 AM": 0,
              "02 AM": 0,
              "04 AM": 0,
              "06 AM": 0,
              "08 AM": 0,
              "10 AM": 0,
              "12 PM": 0,
              "14 PM": 0,
              "16 PM": 0,
              "18 PM": 0,
              "20 PM": 0,
              "22 PM": 0
            },
            {
              "label": "08 PM",
              "00 AM": 0,
              "02 AM": 0,
              "04 AM": 0,
              "06 AM": 0,
              "08 AM": 0,
              "10 AM": 0,
              "12 PM": 0,
              "14 PM": 0,
              "16 PM": 0,
              "18 PM": 0,
              "20 PM": 0,
              "22 PM": 0
            },
            {
              "label": "09 PM",
              "00 AM": 0,
              "02 AM": 0,
              "04 AM": 0,
              "06 AM": 0,
              "08 AM": 0,
              "10 AM": 0,
              "12 PM": 0,
              "14 PM": 0,
              "16 PM": 0,
              "18 PM": 0,
              "20 PM": 0,
              "22 PM": 0
            },
            {
              "label": "10 PM",
              "00 AM": 0,
              "02 AM": 0,
              "04 AM": 0,
              "06 AM": 0,
              "08 AM": 0,
              "10 AM": 0,
              "12 PM": 0,
              "14 PM": 0,
              "16 PM": 0,
              "18 PM": 0,
              "20 PM": 0,
              "22 PM": 0
            },
            {
              "label": "11 PM",
              "00 AM": 0,
              "02 AM": 0,
              "04 AM": 0,
              "06 AM": 0,
              "08 AM": 0,
              "10 AM": 0,
              "12 PM": 0,
              "14 PM": 0,
              "16 PM": 0,
              "18 PM": 0,
              "20 PM": 0,
              "22 PM": 0
            },
            {
              "label": "12 AM",
              "00 AM": 0,
              "02 AM": 0,
              "04 AM": 0,
              "06 AM": 0,
              "08 AM": 0,
              "10 AM": 0,
              "12 PM": 0,
              "14 PM": 0,
              "16 PM": 0,
              "18 PM": 0,
              "20 PM": 0,
              "22 PM": 0
            },
            {
              "label": "01 AM",
              "00 AM": 0,
              "02 AM": 0,
              "04 AM": 0,
              "06 AM": 0,
              "08 AM": 0,
              "10 AM": 0,
              "12 PM": 0,
              "14 PM": 0,
              "16 PM": 0,
              "18 PM": 0,
              "20 PM": 0,
              "22 PM": 0
            },
            {
              "label": "02 AM",
              "00 AM": 0,
              "02 AM": 0,
              "04 AM": 0,
              "06 AM": 0,
              "08 AM": 0,
              "10 AM": 0,
              "12 PM": 0,
              "14 PM": 0,
              "16 PM": 0,
              "18 PM": 0,
              "20 PM": 0,
              "22 PM": 0
            },
            {
              "label": "03 AM",
              "00 AM": 0,
              "02 AM": 0,
              "04 AM": 0,
              "06 AM": 0,
              "08 AM": 0,
              "10 AM": 0,
              "12 PM": 0,
              "14 PM": 0,
              "16 PM": 0,
              "18 PM": 0,
              "20 PM": 0,
              "22 PM": 0
            },
            {
              "label": "04 AM",
              "00 AM": 0,
              "02 AM": 0,
              "04 AM": 0,
              "06 AM": 0,
              "08 AM": 0,
              "10 AM": 0,
              "12 PM": 0,
              "14 PM": 0,
              "16 PM": 0,
              "18 PM": 0,
              "20 PM": 0,
              "22 PM": 0
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

