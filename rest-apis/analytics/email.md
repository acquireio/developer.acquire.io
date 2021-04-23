---
description: Track email metrics including response times and reader activity.
---

# Email

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/mail/all-email-overview" path="" %}
{% api-method-summary %}
All Email Overview
{% endapi-method-summary %}

{% api-method-description %}
View email data including total sent, received, and average response time.
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

{% api-method-parameter name="end\_date" required=true type="string" %}
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
    "allEmailOverview": {
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
          "totalEmails": [
            0,
            0,
            0,
            0,
            0,
            0,
            4,
            16,
            43,
            5,
            5,
            1,
            0
          ],
          "totalEmailsSent": [
            0,
            0,
            0,
            0,
            0,
            0,
            4,
            8,
            25,
            4,
            3,
            1,
            0
          ],
          "totalEmailsReceived": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            8,
            18,
            1,
            2,
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
            13,
            848.2727,
            0,
            66673.5,
            0,
            0
          ]
        },
        "summary": {
          "totalEmails": {
            "current": 74,
            "previous": 0,
            "info": "All emails received and sent by your team."
          },
          "totalEmailsSent": {
            "current": 45,
            "previous": 0
          },
          "totalEmailsReceived": {
            "current": 29,
            "previous": 0
          },
          "averageResponseTime": {
            "current": 4345.342857142857,
            "previous": null
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
  
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/mail/email-activity" path="" %}
{% api-method-summary %}
Activity
{% endapi-method-summary %}

{% api-method-description %}
View the most active times for emails that were read, unread, delivered, and replied to, and bounced.
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

{% api-method-parameter name="end\_date" required=true type="string" %}
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
    "emailActivity": {
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
          "totalMailRead": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
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
          "totalMailUnread": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
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
          "totalMailDelivered": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
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
          "totalMailReplied": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
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
          "totalMailBounced": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
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
          "totalMailRead": {
            "current": 0,
            "previous": 0
          },
          "totalMailUnread": {
            "current": 0,
            "previous": 0
          },
          "totalMailDelivered": {
            "current": 0,
            "previous": 0
          },
          "totalMailReplied": {
            "current": 0,
            "previous": 0
          },
          "totalMailBounced": {
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

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/mail/all-email-overview" path="" %}
{% api-method-summary %}
Busiest Periods for Email
{% endapi-method-summary %}

{% api-method-description %}
View periods when emails were sent and received.
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

{% api-method-parameter name="end\_date" required=true type="string" %}
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
    "busiestPeriodsEmail": {
      "data": {
        "graphRow": {
          "data": [
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
            },
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



