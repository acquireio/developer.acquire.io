---
description: View lead data from all your installed business applications.
---

# Business Applications

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/app/business-apps-list" path="" %}
{% api-method-summary %}
App List
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter type="string" name="Authorization" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="category\_id" type="string" required=true %}
Pass \*8\* as category id for business apps list
{% endapi-method-parameter %}

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
              "appId": "freshdesk",
              "appName": "Freshdesk",
              "iconSmall": "./assets/app-store/freshdesk.svg",
              "iconColor": "#24c46c",
              "dateInstalled": "21-10-2020",
              "itemsCount": 206,
              "appTooltipTitle": "Total Leads",
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
            },
            {
              "appId": "hubspot",
              "appName": "HubSpot",
              "iconSmall": "./assets/app-store/hubspot.svg",
              "iconColor": "#fc741c",
              "dateInstalled": "21-10-2020",
              "itemsCount": 0,
              "appTooltipTitle": "Total Leads",
              "chartType": "bar",
              "config": {
                "backgroundColor": "#00363d",
                "barThickness": 10,
                "maxBarThickness": 10
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

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/app/business-app-graph-data" path="" %}
{% api-method-summary %}
App Graph Data
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter type="string" name="Authorization" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter type="string" name="app\_id" required=true %}
Pass the id of an app for which you want to get data.You can get app id by calling app list API mentioned above.
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="start\_date" required=true %}
Date From \(Date format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 00:00:00\)
{% endapi-method-parameter %}

{% api-method-parameter name="end\_date" type="string" required=true %}
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
        "leads": [
          0,
          0,
          0,
          0,
          0,
          0,
          0,
          0,
          0,
          0,
          0,
          0,
          0,
          0,
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

