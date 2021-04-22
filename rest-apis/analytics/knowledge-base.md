---
description: 'View article visits, reader satisfaction, and popular categories.'
---

# Knowledge Base

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/kb/overview" path="" %}
{% api-method-summary %}
Overview
{% endapi-method-summary %}

{% api-method-description %}
View data on content creation, search volume, and article feedback.
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
    "overview": {
      "data": {
        "graphRow": {
          "publishedArticles": [
            0,
            0
          ],
          "views": [
            0,
            0
          ],
          "reactions": [
            0,
            0
          ],
          "comments": [
            0,
            0
          ]
        },
        "summary": {
          "totalAngryReactions": {
            "current": 0,
            "previous": 0
          },
          "totalHappyReactions": {
            "current": 0,
            "previous": 0
          },
          "totalNormalReactions": {
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

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/kb/searches" path="" %}
{% api-method-summary %}
Searches
{% endapi-method-summary %}

{% api-method-description %}
An overview of how easily searchable your Knowledge Base is.
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
    "searches": {
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
          "totalSearches": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            3,
            3,
            14,
            0,
            13,
            0
          ],
          "successfulSearches": [
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
            7,
            0
          ],
          "unsuccessfulSearches": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            3,
            11,
            0,
            6,
            0
          ]
        },
        "summary": {
          "totalSearches": {
            "current": 33,
            "previous": 0,
            "info": "The number of times a user queried your Knowledge Base."
          },
          "successfulSearches": {
            "current": 13,
            "previous": 0,
            "info": "The number of times a Knowledge Base query produced an article that was clicked."
          },
          "unsuccessfulSearches": {
            "current": 20,
            "previous": 0,
            "info": "The number of times a Knowledge Base query resulted in no article clicks."
          },
          "successRate": {
            "current": 39.39,
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

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/kb/most-popular-searches" path="" %}
{% api-method-summary %}
Most Popular Searches
{% endapi-method-summary %}

{% api-method-description %}
The most frequently searched terms in your Knowledge Base.
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
    "mostPopularSearches": {
      "data": {
        "graphRow": {
          "labels": [
            "test"
          ],
          "searches": [
            5
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

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/kb/all-questions-reporting" path="" %}
{% api-method-summary %}
All Questions Reporting
{% endapi-method-summary %}

{% api-method-description %}
Retrieve view count and reaction data for articles.
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
    "allQuestionsReporting": {
      "data": {
        "graphRow": {
          "data": [
            {
              "article": "test1",
              "views": 1,
              "positive": 0,
              "satisfied": 0,
              "negative": 1
            },
            {
              "article": "test2",
              "views": 2,
              "positive": 1,
              "satisfied": 0,
              "negative": 0
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

