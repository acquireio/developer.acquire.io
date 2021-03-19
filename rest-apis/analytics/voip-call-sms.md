---
description: See an overview of all call and SMS interactions.
---

# VoIP - Call SMS

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api" path="/v1/analytics/voip/calls-overview?start\_date=2020-03-16%2015%3A44%3A07&end\_date=2021-03-17%2015%3A44%3A06&output=json&offset=%2B00%3A00" %}
{% api-method-summary %}
Calls Overview
{% endapi-method-summary %}

{% api-method-description %}
View call metrics including number of calls and duration.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="start\_date" required=true type="string" %}
Date From \(Date format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 00:00:00\)
{% endapi-method-parameter %}

{% api-method-parameter name="end\_date" type="string" required=true %}
Date End \(Date Format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 23:59:59\)
{% endapi-method-parameter %}

{% api-method-parameter name="offset" required=false type="string" %}
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
    "callsOverview": {
      "data": {
        "graphRow": {
          "labels": [
            "16 Mar 2020",
            "16 Apr 2020",
            "16 May 2020",
            "16 Jun 2020",
            "16 Jul 2020",
            "16 Aug 2020",
            "16 Sep 2020",
            "16 Oct 2020",
            "16 Nov 2020",
            "16 Dec 2020",
            "16 Jan 2021",
            "16 Feb 2021",
            "16 Mar 2021"
          ],
          "outgoingCalls": [
            0,
            0,
            0,
            0,
            0,
            0,
            7,
            3,
            19,
            2,
            0,
            5,
            0
          ],
          "incomingCalls": [
            0,
            0,
            0,
            0,
            0,
            0,
            11,
            7,
            34,
            2,
            1,
            0,
            0
          ],
          "missedCalls": [
            0,
            0,
            0,
            0,
            0,
            0,
            6,
            0,
            8,
            2,
            1,
            0,
            0
          ],
          "averageCallTime": [
            0,
            0,
            0,
            0,
            0,
            0,
            12,
            5.7,
            20.75,
            0,
            0,
            37.5,
            0
          ]
        },
        "summary": {
          "outgoingCalls": {
            "current": 36,
            "previous": 0
          },
          "incomingCalls": {
            "current": 55,
            "previous": 0
          },
          "missedCalls": {
            "current": 17,
            "previous": 0
          },
          "averageCallTime": {
            "current": 18,
            "previous": 0
          },
          "averageResponseTime": {
            "current": 26247,
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

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api" path="/v1/analytics/voip/sms-metrics?start\_date=2020-03-16%2015%3A44%3A07&end\_date=2021-03-17%2015%3A44%3A06&output=json&offset=%2B00%3A00" %}
{% api-method-summary %}
SMS Metrics
{% endapi-method-summary %}

{% api-method-description %}
See how many SMS messages your team receives and responds to.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="start\_date" required=true type="string" %}
Date From \(Date format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 00:00:00\)
{% endapi-method-parameter %}

{% api-method-parameter name="end\_date" type="string" required=true %}
Date End \(Date Format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 23:59:59\)
{% endapi-method-parameter %}

{% api-method-parameter name="offset" required=false type="string" %}
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
    "smsMetrics": {
      "data": {
        "graphRow": {
          "labels": [
            "16 Mar 2020",
            "16 Apr 2020",
            "16 May 2020",
            "16 Jun 2020",
            "16 Jul 2020",
            "16 Aug 2020",
            "16 Sep 2020",
            "16 Oct 2020",
            "16 Nov 2020",
            "16 Dec 2020",
            "16 Jan 2021",
            "16 Feb 2021",
            "16 Mar 2021"
          ],
          "incomingSms": [
            0,
            0,
            0,
            0,
            0,
            0,
            2,
            1,
            17,
            0,
            0,
            0,
            0
          ],
          "outgoingSms": [
            0,
            0,
            0,
            0,
            0,
            0,
            8,
            0,
            28,
            1,
            1,
            0,
            0
          ],
          "failedSms": [
            0,
            0,
            0,
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
            458.75,
            0,
            0,
            0,
            0
          ]
        },
        "summary": {
          "outgoingSms": {
            "current": 38,
            "previous": 0
          },
          "incomingSms": {
            "current": 20,
            "previous": 0
          },
          "failedSms": {
            "current": 0,
            "previous": 0
          },
          "averageResponseTime": {
            "current": 459,
            "previous": null
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

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api" path="/v1/analytics/voip/calls-overview?start\_date=2020-03-16%2015%3A44%3A07&end\_date=2021-03-17%2015%3A44%3A06&output=json&offset=%2B00%3A00" %}
{% api-method-summary %}
Call Analysis
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
{% api-method-parameter name="start\_date" required=true type="string" %}
Date From \(Date format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 00:00:00\)
{% endapi-method-parameter %}

{% api-method-parameter name="end\_date" type="string" required=true %}
Date End \(Date Format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 23:59:59\)
{% endapi-method-parameter %}

{% api-method-parameter name="offset" required=false type="string" %}
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
    "callAnalysis": {
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
          "peopleAddedInCall": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
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
          "peopleLeftIVR": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
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
          "peopleLeftFromHold": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
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
          "averageIVRTime": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
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
          "averageHoldTime": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
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
          "peopleAddedInCall": {
            "current": 0,
            "previous": 0
          },
          "peopleLeftIVR": {
            "current": 0,
            "previous": 0
          },
          "peopleLeftFromHold": {
            "current": 0,
            "previous": 0
          },
          "averageIVRTime": {
            "current": 0
          },
          "averageHoldTime": {
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



