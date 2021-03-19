---
description: API to list all the available groups
---

# List

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/bot/group" path="" %}
{% api-method-summary %}
List Groups
{% endapi-method-summary %}

{% api-method-description %}
API to list all the available groups
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
    "rows": [
      {
        "id": 1,
        "title": "Primary Group",
        "description": "Default question group created at the time of account registration.",
        "isDefault": "yes",
        "askFeedback": "disabled",
        "cascadeApplicable": "disabled",
        "createdBy": 1,
        "updatedBy": 1,
        "dateCreated": "2020-06-22T16:17:32.000Z",
        "dateUpdated": "2021-01-19T05:05:08.000Z"
      }
    ]
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



