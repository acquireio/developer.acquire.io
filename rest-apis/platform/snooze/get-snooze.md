---
description: API to get details of a specific snooze
---

# Get Snooze

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/follow-up/get" path="" %}
{% api-method-summary %}
Get Snooze
{% endapi-method-summary %}

{% api-method-description %}
API to get details of a specific snooze
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
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
    "data": {
      "id": 1,
      "objectType": "case",
      "contactId": 53,
      "scheduleDate": "2020-05-28T12:30:00.000Z"
    }
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Body\(raw\)

```text
{
  "objectId": 53,
  "objectType": "case",
  "contactId": 53
}
```

