---
description: View your team’s video usage across conversations.
---

# Video Analytics

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api//v1/analytics/chat/video-analytics" path="" %}
{% api-method-summary %}
Video Sessions
{% endapi-method-summary %}

{% api-method-description %}
Retrieve data for video sessions.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter type="string" name="Authorization" required=true %}
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
    "videoAnalytics": {
      "data": {
        "graphRow": {
          "labels": [
            "18 Mar 2020",
            "18 Apr 2020",
            "18 May 2020",
            "18 Jun 2020",
            "18 Jul 2020",
            "18 Aug 2020",
            "18 Sep 2020",
            "18 Oct 2020",
            "18 Nov 2020",
            "18 Dec 2020",
            "18 Jan 2021",
            "18 Feb 2021",
            "18 Mar 2021"
          ],
          "totalSession": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            5,
            0,
            0
          ],
          "averageSessionTime": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            9,
            0,
            0
          ],
          "responseTime": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            21,
            0,
            0
          ]
        },
        "summary": {
          "totalSession": {
            "current": 5,
            "previous": 0
          },
          "averageSessionTime": {
            "current": 9,
            "previous": 0
          },
          "responseTime": {
            "current": 21,
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



