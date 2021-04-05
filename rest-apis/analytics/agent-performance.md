# Agent Performance

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/agent/agent-list" path="" %}
{% api-method-summary %}
Agent List
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
{% api-method-parameter name="search" type="string" required=false %}
You can pass text that will be applicable to search in agent name or email.
{% endapi-method-parameter %}

{% api-method-parameter name="page" type="string" %}
Page number for which you want agent records if you are using pagination. If you are not passing limit or page then it will retrieve all records.
{% endapi-method-parameter %}

{% api-method-parameter name="limit" type="string" required=false %}
Number of records you want in one call. If you are not passing limit or page then it will retrieve all records.
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
    "agents_list": {
      "data": [
        {
          "id": 1,
          "name": "Test Agent",
          "email": "test@acquire.io",
          "image": null,
          "department": "Analytics12",
          "role": "Administrator",
          "rating": 3.25,
          "isOnline": "online",
          "stateChat": "yes",
          "stateMail": "yes",
          "stateVoip": "yes"
        }
      ],
      "totalCount": 1,
      "success": true
    }
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/agent/graph-data" path="" %}
{% api-method-summary %}
Agent Graph Data
{% endapi-method-summary %}

{% api-method-description %}
View agent metrics, ratings, and response times across all channels.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="agent\_id" type="string" required=true %}
Pass the id of an agent for which you want to get data.You can get agent id by calling agent list API mentioned above.
{% endapi-method-parameter %}

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
    "agentStatistics": {
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
          "totalConversations": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
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
          "totalMissed": [
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
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
          ],
          "login_scale": [
            {
              "class": "off",
              "val": 96.27,
              "diff": 83177,
              "label": "03:44:03 PM to 02:50:20 PM (23 hours 6 minutes 17 seconds)"
            },
            {
              "class": "on",
              "val": 3.23,
              "diff": 2787,
              "label": "02:50:21 PM to 03:36:48 PM (0 hours 46 minutes 27 seconds)"
            },
            {
              "val": 0.5,
              "class": "off",
              "diff": 433,
              "label": "03:36:49 PM to 03:44:02 PM (0 hours 7 minutes 13 seconds)"
            }
          ]
        },
        "summary": {
          "totalConversations": {
            "current": 0,
            "previous": 0,
            "info": "Includes all chats, calls and emails handled by an agent."
          },
          "totalChats": {
            "current": 0,
            "previous": 0
          },
          "totalMissed": {
            "current": 0,
            "previous": 0
          },
          "totalVoip": {
            "current": 0,
            "previous": 0
          },
          "totalVoipSms": {
            "current": 0,
            "previous": 0
          },
          "totalEmails": {
            "current": 0,
            "previous": 0
          },
          "totalPrivateForms": {
            "current": 0,
            "previous": 0
          },
          "averageRating": {
            "current": 0,
            "previous": 0
          },
          "averageResponseTime": {
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

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/analytics/agent/agent-leaderboard" path="" %}
{% api-method-summary %}
Agent Leaderboard
{% endapi-method-summary %}

{% api-method-description %}
A large board for displaying the ranking of the Agents.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="filter.role" type="string" %}
List of role ids for which API will return details of cases for agent.  
  
Ex. \[1,2\]
{% endapi-method-parameter %}

{% api-method-parameter name="filter.departments" type="string" %}
List of department ids for which API will return details of cases for agent.  
  
Ex. \[1,2\]
{% endapi-method-parameter %}

{% api-method-parameter name="filter.channel" type="array" required=false %}
List of channels for which API will return details of cases for agent.  
  
Ex. \[var \_utcDate = new Date\(localDate.getUTCFullYear\(\), localDate.getUTCMonth\(\), localDate.getUTCDate\(\), localDate.getUTCHours\(\), localDate.getUTCMinutes\(\), localDate.getUTCSeconds\(\)\);'chat', 'mail', 'voip'\]
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="search" %}
You can pass text that will be applicable to search in agent name or email.
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="limit" %}
Number of records you want in one call. If you are not passing limit or page then it will retrieve all records.
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="page" %}
Page number for which you want agent records if you are using pagination. If you are not passing limit or page then it will retrieve all records.
{% endapi-method-parameter %}

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
    "agentLeaderboard": {
      "data": {
        "responseData": [
          {
            "id": 12,
            "email": "viswanath.sarma@acquire.io",
            "departments": "voip,email",
            "role": "Administrator",
            "solvedCases": 21,
            "totalTimeSpent": 127,
            "avgTimeSpentPerCase": 6,
            "averageResponseTime": 5,
            "averageRatingFeedback": 0,
            "agent": {
              "name": "viswanath",
              "photo": null
            }
          },
          {
            "id": 18,
            "email": "checksum@gmail.com",
            "departments": "voip",
            "role": "Administrator",
            "solvedCases": 0,
            "totalTimeSpent": 0,
            "avgTimeSpentPerCase": 0,
            "averageResponseTime": 0,
            "averageRatingFeedback": 0,
            "agent": {
              "name": "checksusms",
              "photo": null
            }
          }
        ],
        "totalRecords": 2
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

