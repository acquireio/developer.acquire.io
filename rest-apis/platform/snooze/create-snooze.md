---
description: >-
  API to create a Snooze, Where Snooze can be created both at the Contact Level
  and Case Levels as well
---

# Create Snooze

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/follow-up/create" path="" %}
{% api-method-summary %}
Create Snooze
{% endapi-method-summary %}

{% api-method-description %}
API to create a snooze
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
\*\*\*\*\*YOUR API KEY\*\*\*\*\*
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
    "success": true,
    "message": "Snooze added successfully",
    "data": {
      "id": 3,
      "objectType": "case",
      "contactId": 53,
      "scheduleDate": "2020-05-28 12:30:00",
      "objectId": 53,
      "userId": 12,
      "message": "This is simple message",
      "users": [
        {
          "1": {
            "id": 1,
            "email": "user@gmail.com",
            "name": "User Name"
          }
        }
      ]
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
  "scheduleDate": "2020-05-28 12:30:00",
  "message": "This is simple message",
  "objectId": 53,
  "contactId": 53,
  "objectType": "case",
  "users": [
    {
      "1": {
        "id": 1,
        "email": "user@gmail.com",
        "name": "User Name"
      }
    }
  ]
}
```

