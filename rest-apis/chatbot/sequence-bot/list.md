---
description: API to list the bot sequences available
---

# List

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/bot/lead" path="" %}
{% api-method-summary %}
List Sequence
{% endapi-method-summary %}

{% api-method-description %}
API to list the bot sequences available
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
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
    "count": 1,
    "limit": 12,
    "page": 1,
    "rows": [
      {
        "id": 137,
        "title": "Sales Sequence 05",
        "description": "A sequence designed to generate leads.",
        "status": "publish",
        "greeting": "active",
        "askFeedback": "disabled",
        "identifier": "salesSequence",
        "identifierCount": 6,
        "isImported": "no",
        "isCloned": "no",
        "clonedCount": 0,
        "createdBy": 1,
        "updatedBy": 1,
        "dateCreated": "2020-12-15T08:36:02.000Z",
        "dateUpdated": "2021-02-24T06:18:39.000Z",
        "bots": {
          "id": 198,
          "userId": 1,
          "slug": "sequence_bot",
          "title": "Sequence Bot",
          "assistantName": "Virtual Assistant",
          "assistantIcon": "",
          "params": null,
          "createdBy": 1,
          "updatedBy": 1,
          "dateCreated": "2021-01-18T04:52:57.000Z",
          "dateUpdated": "2021-01-18T04:52:57.000Z"
        }
      }
    ]
  }
}

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



