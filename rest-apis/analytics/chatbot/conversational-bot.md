---
description: Track Conversation Bot engagement and effectiveness.
---

# Conversational Bot

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api" path="/v1/analytics/bot/conversational-bot-overview?start\_date=2021-03-16%2015%3A44%3A04&end\_date=2021-03-17%2015%3A44%3A03&output=json&offset=%2B00%3A00" %}
{% api-method-summary %}
Overview
{% endapi-method-summary %}

{% api-method-description %}
View how many customers and conversations your Conversational Bot handles.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter type="string" name="Authorization" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="start\_date" required=true type="string" %}
Date From \(Date format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 00:00:00\)
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="end\_date" required=true %}
Date End \(Date Format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 23:59:59\)
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="offset" %}
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
    "conversationalBotOverview": {
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
          "customersEngaged": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            1,
            0,
            1,
            0,
            0,
            0
          ],
          "interactionsWithBot": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            1,
            0,
            1,
            0,
            0,
            0
          ],
          "resolvedIssues": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            2,
            0,
            2,
            0,
            0,
            0
          ],
          "unansweredQuestions": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            1,
            0,
            0,
            0
          ]
        },
        "summary": {
          "customersEngaged": {
            "current": 2,
            "previous": 0
          },
          "interactionsWithBot": {
            "current": 2,
            "previous": 0
          },
          "resolvedIssues": {
            "current": 4,
            "previous": 0
          },
          "unansweredQuestions": {
            "current": 1,
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

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api" path="/v1/analytics/bot/questions-report?start\_date=2020-03-16%2015%3A44%3A04&end\_date=2021-03-17%2015%3A44%3A03&output=json&offset=%2B00%3A00" %}
{% api-method-summary %}
Questions Report
{% endapi-method-summary %}

{% api-method-description %}
View how many View the number of questions added, used, and suggested to Conversational Bot. and conversations your Conversational Bot handles.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter type="string" name="Authorization" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="start\_date" required=true type="string" %}
Date From \(Date format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 00:00:00\)
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="end\_date" required=true %}
Date End \(Date Format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 23:59:59\)
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="offset" %}
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
    "questionsReport": {
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
          "totalQuestionsAdded": [
            0,
            0,
            0,
            0,
            0,
            0,
            3,
            0,
            0,
            3,
            0,
            0,
            0
          ],
          "totalQuestionsInUse": [
            0,
            0,
            0,
            0,
            0,
            0,
            3,
            0,
            0,
            2,
            0,
            0,
            0
          ],
          "totalSuggestedQuestions": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            1,
            0,
            0,
            0
          ],
          "totalQuestionGroups": [
            0,
            0,
            0,
            0,
            0,
            0,
            1,
            0,
            0,
            1,
            0,
            0,
            0
          ]
        },
        "summary": {
          "totalQuestionsAdded": {
            "current": 6,
            "previous": 0
          },
          "totalQuestionsInUse": {
            "current": 5,
            "previous": 0
          },
          "totalSuggestedQuestions": {
            "current": 1,
            "previous": 0
          },
          "totalQuestionGroups": {
            "current": 2,
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

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api" path="/v1/analytics/bot/questions-report?start\_date=2020-03-16%2015%3A44%3A04&end\_date=2021-03-17%2015%3A44%3A03&output=json&offset=%2B00%3A00" %}
{% api-method-summary %}
All Question Groups
{% endapi-method-summary %}

{% api-method-description %}
See which question groups are most active.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter type="string" name="Authorization" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="start\_date" required=true type="string" %}
Date From \(Date format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 00:00:00\)
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="end\_date" required=true %}
Date End \(Date Format = YYYY-MM-DD hh:mm:ss, e.g 2021-01-01 23:59:59\)
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="offset" %}
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
    "conversationalBotQuestionGroups": {
      "data": {
        "graphRow": {
          "data": [
            {
              "group_id": 1,
              "title": "Primary Group",
              "live": 23,
              "suggested": 23
            },
            {
              "group_id": 2,
              "title": "Primary Group2",
              "live": 32,
              "suggested": 32
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

