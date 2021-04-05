---
description: >-
  Create a snooze. A snooze can be created both at the contact level and case
  level.
---

# Create Snooze

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/follow-up/create" path="" %}
{% api-method-summary %}
Create Snooze
{% endapi-method-summary %}

{% api-method-description %}
Create a snooze. The body requires the following:   
  
`"contactId"` and/or `"caseId"`    
  
 `"objectType"` set to `"case"`    
  
`"scheduleDate"`  in `"YYYY-MM-DD HH:MM:SS"` format.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="scheduleDate" type="string" required=true %}
Date when the snooze elapses. YYYY-MM-DD HH:MM:SS format. 
{% endapi-method-parameter %}

{% api-method-parameter name="objectType" type="string" required=true %}
"case"
{% endapi-method-parameter %}

{% api-method-parameter name="caseId" type="integer" required=true %}
The case ID \(not required if contactId is present\)
{% endapi-method-parameter %}

{% api-method-parameter name="contactId" type="integer" required=true %}
The contact ID \(not required if caseId is present\)
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
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
    caseId: null,
    contactId: 768,
    message: "",
    objectId: 768,
    objectType: "contact",
    scheduleDate: "2021-04-05T13:44:12.000Z",
    users: []
}
```

