---
description: API to close a case
---

# Close Case

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/messenger/chat/close" path="" %}
{% api-method-summary %}
Close a case
{% endapi-method-summary %}

{% api-method-description %}
Closes a case. The **caseId** must be passed in the body of the request. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="caseId" type="integer" required=true %}
The cases's ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

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
    "0": {
      "foreverClosed": true,
      "leftUser": true,
      "caseId": 5,
      "contactId": 6
    },
    "userId": 1,
    "userType": "user"
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

**Body \(raw\)**

```text
{
  "archive": "yes",
  "closingState": "handled",
  "meta": {
    "additionalProp1": {}
  },
  "forceClose": false,
  "leaveOnly": false,
  "leaveEvent": true,
  "askFeedback": true,
  "caseId": 5
}
```

