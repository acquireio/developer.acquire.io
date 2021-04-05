---
description: Track Sequence Bot conversions and conversations.
---

# Sequence Bot

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/bot/sequence-bot-overview" path="" %}
{% api-method-summary %}
Overview
{% endapi-method-summary %}

{% api-method-description %}
View how many conversations your Sequence Bot handles.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="start\_date" type="string" required=true %}
Date From \(Date format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 00:00:00\)
{% endapi-method-parameter %}

{% api-method-parameter name="end\_date" required=true type="string" %}
Date End \(Date Format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 23:59:59\)
{% endapi-method-parameter %}

{% api-method-parameter name="offset" type="string" required=false %}
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
    "sequenceBotOverview": {
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
          "initiated": [
            0,
            0,
            0,
            0,
            0,
            0,
            1,
            4,
            0,
            4,
            0,
            0,
            0
          ],
          "completed": [
            0,
            0,
            0,
            0,
            0,
            0,
            1,
            1,
            0,
            1,
            0,
            0,
            0
          ],
          "liveHandOffs": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            3,
            0,
            2,
            0,
            0,
            0
          ],
          "abandoned": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            3,
            0,
            3,
            0,
            0,
            0
          ]
        },
        "summary": {
          "initiated": {
            "current": 9,
            "previous": 0,
            "info": "The number of times a visitor started a conversation with a Sequence Bot."
          },
          "completed": {
            "current": 3,
            "previous": 0,
            "info": "The number of times a visitor completes a full sequence."
          },
          "liveHandOffs": {
            "current": 5,
            "previous": 0,
            "info": "Any time a sequence bot transfer conversation to a human."
          },
          "abandoned": {
            "current": 6,
            "previous": 0,
            "info": "The number of time visitors leave a chat without completing the sequence."
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

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/bot/leads-generated" path="" %}
{% api-method-summary %}
Leads Generated
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="start\_date" type="string" required=true %}
Date From \(Date format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 00:00:00\)
{% endapi-method-parameter %}

{% api-method-parameter name="end\_date" required=true type="string" %}
Date End \(Date Format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 23:59:59\)
{% endapi-method-parameter %}

{% api-method-parameter name="offset" type="string" required=false %}
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
    "leadsGenerated": {
      "data": {
        "graphRow": {
          "data": [
            {
              "lead_name": "Sales Sequence",
              "initiated": 1,
              "completed": 1,
              "transferred": 0,
              "incompleted": 0
            },
            {
              "lead_name": "PNB Bank",
              "initiated": 8,
              "completed": 2,
              "transferred": 5,
              "incompleted": 6
            }
          ]
        }
      },
      "success": true,
      "output": "json"
    }
  }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/bot/leads-generated" path="" %}
{% api-method-summary %}
Path Analysis
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="leadId" type="string" required=true %}
Lead id of lead to get details of lead. You can get lead i by calling bot-lead-details api mentioned below.
{% endapi-method-parameter %}

{% api-method-parameter name="start\_date" type="string" required=true %}
Date From \(Date format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 00:00:00\)
{% endapi-method-parameter %}

{% api-method-parameter name="end\_date" required=true type="string" %}
Date End \(Date Format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 23:59:59\)
{% endapi-method-parameter %}

{% api-method-parameter name="offset" type="string" required=false %}
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
    "botPathAnalysis": {
      "data": {
        "graphRow": {
          "data": [
            {
              "from_branch": "Initiated",
              "to_branch": "Welcome",
              "count": 1,
              "from_visible_order": 0,
              "to_visible_order": 1
            },
            {
              "from_branch": "Welcome",
              "to_branch": "Explore branch",
              "count": 1,
              "from_visible_order": 1,
              "to_visible_order": 4
            },
            {
              "from_branch": "Explore branch",
              "to_branch": "Just browsing",
              "count": 1,
              "from_visible_order": 4,
              "to_visible_order": 8
            }
          ]
        }
      },
      "success": true,
      "output": "json"
    }
  }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/bot/bot-lead-details" path="" %}
{% api-method-summary %}
Lead Details
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "data": {
    "botLeadDetails": {
      "leads": [
        {
          "id": 1,
          "title": "Out Of Office Sequence",
          "details": [
            {
              "next_branch": "0,3,4",
              "id": 5,
              "title": "Welcome"
            },
            {
              "next_branch": "0,1,2",
              "id": 4,
              "title": "Leave a message"
            },
            {
              "next_branch": "0",
              "id": 3,
              "title": "Just browsing"
            },
            {
              "next_branch": "0",
              "id": 2,
              "title": "Our customer"
            },
            {
              "next_branch": "0",
              "id": 1,
              "title": "New customer"
            }
          ]
        }
      ],
      "success": true
    }
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

