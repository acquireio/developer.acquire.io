---
description: View data from all your installed messenger apps.
---

# Messenger App

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/app/messenger-apps-list" path="" %}
{% api-method-summary %}
Apps Installed
{% endapi-method-summary %}

{% api-method-description %}
Get list of all installed messenger apps list
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter type="string" name="offset" required=true %}
This parameter is used for the timezone value and the default timezone will be "GMT". e.g. +05:30 for particular timezone. Default is +00:00
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
    "applications": {
      "success": true,
      "data": {
        "graphRow": {
          "data": [
            {
              "appId": "article_search",
              "appName": "Article Search",
              "iconSmall": "./assets/app-store/article_search.svg",
              "iconColor": "#ec2c54",
              "dateInstalled": "21-10-2020",
              "itemsCount": 33,
              "keys": [
                {
                  "key": "totalBooked",
                  "tooltip": "Total Searched",
                  "summaryTitle": "Total Searched"
                },
                {
                  "key": "failed",
                  "tooltip": "",
                  "summaryTitle": "Total Failed"
                },
                {
                  "key": "success",
                  "tooltip": "",
                  "summaryTitle": "Total Success"
                }
              ],
              "appTooltipTitle": "Total Searched",
              "chartType": "line",
              "config": {
                "fill": false,
                "backgroundColor": "#1798C1",
                "borderColor": "#1798C1",
                "pointRadius": 0,
                "pointHoverBorderWidth": 4,
                "pointHoverRadius": 8,
                "pointHoverBorderColor": "#ffffff",
                "pointHoverBackgroundColor": "#1798C1"
              }
            }
          ]
        }
      },
      "output": "json"
    }
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/app/messenger-app-graph-data" path="" %}
{% api-method-summary %}
App Graph Data
{% endapi-method-summary %}

{% api-method-description %}
Get list of all installed messenger apps list
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" required=true type="string" %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="app\_id" type="string" required=true %}
App id for which you want graph data.You can get app id by calling app list API mentioned above.
{% endapi-method-parameter %}

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
    "success": true,
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
        "totalBooked": [
          0,
          0,
          0,
          0,
          0,
          0,
          0,
          0,
          0,
          0,
          0,
          0,
          0,
          0,
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
        "totalBooked": 0,
        "failed": 0,
        "success": 0
      }
    },
    "output": "json"
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

