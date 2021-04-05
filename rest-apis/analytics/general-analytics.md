# General Analytics

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/general/cases-overview" path="" %}
{% api-method-summary %}
Overview
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
{% api-method-parameter name="start\_date" type="string" required=true %}
Date From \(Date format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 00:00:00\)
{% endapi-method-parameter %}

{% api-method-parameter name="end\_date" type="string" required=true %}
Date End \(Date Format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 23:59:59\)
{% endapi-method-parameter %}

{% api-method-parameter name="offset" type="string" required=false %}
This parameter is used for the timezone value and the default timezone will be "GMT". e.g. +05:30 for particular timezone. Default is +00:00
{% endapi-method-parameter %}

{% api-method-parameter name="output" type="string" required=false %}
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
    "casesOverview": {
      "data": {
        "graphRow": {
          "labels": [
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
            "02 PM",
            "03 PM",
            "04 PM"
          ],
          "total": [
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
            7,
            0,
            0,
            4,
            5,
            6
          ],
          "pendingToActive": [
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
            7,
            0,
            0,
            4,
            5,
            6
          ],
          "activeToClose": [
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
            6,
            0,
            0,
            4,
            5,
            6
          ],
          "reopened": [
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
          "avgPendingToActiveTime": [
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
            4.5714,
            0,
            0,
            5.25,
            3.8,
            5
          ],
          "avgActiveToCloseTime": [
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
            4,
            0,
            0,
            6,
            6.4,
            7.8333
          ]
        },
        "summary": {
          "total": {
            "current": 22,
            "previous": 0
          },
          "pendingToActive": {
            "current": 22,
            "previous": 0
          },
          "activeToClose": {
            "current": 21,
            "previous": 0
          },
          "reopened": {
            "current": 0,
            "previous": 0
          },
          "avgPendingToActiveTime": {
            "current": 5,
            "previous": 0
          },
          "avgActiveToCloseTime": {
            "current": 6,
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

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/general/cases-by-channel" path="" %}
{% api-method-summary %}
By Channel
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
{% api-method-parameter name="start\_date" type="string" required=true %}
Date From \(Date format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 00:00:00\)
{% endapi-method-parameter %}

{% api-method-parameter name="end\_date" type="string" required=true %}
Date End \(Date Format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 23:59:59\)
{% endapi-method-parameter %}

{% api-method-parameter name="offset" type="string" required=false %}
This para
{% endapi-method-parameter %}

{% api-method-parameter name="offset" type="string" required=false %}
meter is used for the timezone value and the default timezone will be "GMT". e.g. +05:30 for particular timezone. Default is +00:00
{% endapi-method-parameter %}

{% api-method-parameter name="output" type="string" required=false %}
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
    "casesByChannel": {
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
          "totalCases": [
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
          "totalMails": [
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
          "totalVoip": [
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
          "totalPrivateForms": [
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
          "socialAppsCases": [
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
          "totalCases": {
            "current": 0,
            "previous": 1
          },
          "totalChats": {
            "current": 0,
            "previous": 0
          },
          "totalMails": {
            "current": 0,
            "previous": 0
          },
          "totalVoip": {
            "current": 0,
            "previous": 0
          },
          "socialAppsCases": {
            "current": 0,
            "previous": 0
          },
          "totalPrivateForms": {
            "current": 0,
            "previous": 1
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

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/general/busiest-periods-cases" path="" %}
{% api-method-summary %}
By Busiest Periods for Cases
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
{% api-method-parameter name="start\_date" type="string" required=true %}
Date From \(Date format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 00:00:00\)
{% endapi-method-parameter %}

{% api-method-parameter name="end\_date" type="string" required=true %}
Date End \(Date Format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 23:59:59\)
{% endapi-method-parameter %}

{% api-method-parameter name="offset" type="string" required=false %}
This parameter is used for the timezone value and the default timezone will be "GMT". e.g. +05:30 for particular timezone. Default is +00:00
{% endapi-method-parameter %}

{% api-method-parameter name="output" type="string" required=false %}
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
    "busiestPeriodsCases": {
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



