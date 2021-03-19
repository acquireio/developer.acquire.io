---
description: View visitor activity and location information.
---

# Visitor Analytics



{% api-method method="get" host="https://{{account\_id}}.acquire.io/api" path="/v1/analytics/chat/visitors-by-location?start\_date=2021-03-18%2005%3A50%3A55&end\_date=2021-03-19%2005%3A50%3A54&output=json&offset=%2B00%3A00" %}
{% api-method-summary %}
All Visitors by Location
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
    "visitorsByLocation": {
      "data": {
        "graphRow": {
          "data": [
            {
              "name": "French Southern and Antarctic Lands",
              "cca3": "ATF",
              "id": 313,
              "countryKey": "296",
              "visitorCount": 1,
              "caseCount": 3,
              "chatCount": 3,
              "emailCount": 0,
              "cobrowseCount": 0,
              "screenShareCount": 0,
              "videocall": 0,
              "audiocall": 0,
              "totalVoip": 0,
              "voipCallCount": 0,
              "voipSmsCount": 0,
              "lat": "-49.25",
              "lng": "69.167"
            },
            {
              "name": "Benin",
              "cca3": "BEN",
              "id": 317,
              "countryKey": "303",
              "visitorCount": 1,
              "caseCount": 2,
              "chatCount": 2,
              "emailCount": 0,
              "cobrowseCount": 0,
              "screenShareCount": 0,
              "videocall": 0,
              "audiocall": 0,
              "totalVoip": 0,
              "voipCallCount": 0,
              "voipSmsCount": 0,
              "lat": "9.5",
              "lng": "2.25"
            },
            {
              "name": "Burkina Faso",
              "cca3": "BFA",
              "id": 318,
              "countryKey": "304",
              "visitorCount": 1,
              "caseCount": 1,
              "chatCount": 1,
              "emailCount": 0,
              "cobrowseCount": 0,
              "screenShareCount": 0,
              "videocall": 0,
              "audiocall": 0,
              "totalVoip": 0,
              "voipCallCount": 0,
              "voipSmsCount": 0,
              "lat": "13",
              "lng": "-2"
            },
            {
              "name": "India",
              "cca3": "IND",
              "id": 1,
              "countryKey": "387",
              "visitorCount": 100,
              "caseCount": 178,
              "chatCount": 158,
              "emailCount": 17,
              "cobrowseCount": 12,
              "screenShareCount": 0,
              "videocall": 2,
              "audiocall": 1,
              "totalVoip": 0,
              "voipCallCount": 0,
              "voipSmsCount": 0,
              "lat": "20",
              "lng": "77"
            },
            {
              "name": "Jordan",
              "cca3": "JOR",
              "id": 7508,
              "countryKey": "397",
              "visitorCount": 1,
              "caseCount": 1,
              "chatCount": 1,
              "emailCount": 0,
              "cobrowseCount": 0,
              "screenShareCount": 0,
              "videocall": 0,
              "audiocall": 0,
              "totalVoip": 0,
              "voipCallCount": 0,
              "voipSmsCount": 0,
              "lat": "31",
              "lng": "36"
            },
            {
              "name": "United States",
              "cca3": "USA",
              "id": 308,
              "countryKey": "517",
              "visitorCount": 27,
              "caseCount": 44,
              "chatCount": 35,
              "emailCount": 1,
              "cobrowseCount": 7,
              "screenShareCount": 0,
              "videocall": 3,
              "audiocall": 2,
              "totalVoip": 0,
              "voipCallCount": 0,
              "voipSmsCount": 0,
              "lat": "38",
              "lng": "-97"
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

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api" path="/v1/analytics/chat/most-active-visit-times?start\_date=2021-03-18%2005%3A50%3A55&end\_date=2021-03-19%2005%3A50%3A54&output=json&offset=%2B00%3A00" %}
{% api-method-summary %}
Most Active Visit Times
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
    "mostActiveVisitTimes": {
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

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api" path="/v1/analytics/chat/pages-with-most-chats?start\_date=2021-03-18%2005%3A50%3A55&end\_date=2021-03-19%2005%3A50%3A54&output=json&offset=%2B00%3A00" %}
{% api-method-summary %}
Pages with Most Chats
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
    "pagesWithMostChats": {
      "data": {
        "graphRow": {
          "data": [
            {
              "url": "https://test1.acquire.io/simulate",
              "chats": 195,
              "percentage": "89.86"
            },
            {
              "url": "https://test1.acquire.io/simulate?page=features",
              "chats": 11,
              "percentage": "5.07"
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

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api" path="/v1/analytics/chat/visitor-reference?start\_date=2021-03-18%2005%3A50%3A55&end\_date=2021-03-19%2005%3A50%3A54&output=json&offset=%2B00%3A00" %}
{% api-method-summary %}
Visitor Reference
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
    "visitorReference": {
      "data": {
        "graphRow": {
          "data": [
            {
              "source": "https://test1.acquire.io/simulate?page=contact",
              "chats": 3,
              "percentage": "37.50"
            },
            {
              "source": "http://test1.acquire.io/acquire_widget/index.html",
              "chats": 2,
              "percentage": "25.00"
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



