---
description: Take bulk action on QnAs
---

# Bulk Action

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/bot/qna/bulk" path="" %}
{% api-method-summary %}
Bulk Update
{% endapi-method-summary %}

{% api-method-description %}
Perform a bulk action on multiple QnAs. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="tab" type="string" required=true %}
Specify the section. Current sections: "qna"
{% endapi-method-parameter %}

{% api-method-parameter name="recordIds" type="array" required=true %}
Array of integers. The IDs of the QnAs.  
{% endapi-method-parameter %}

{% api-method-parameter name="groupId" type="integer" required=true %}
The QnA's group
{% endapi-method-parameter %}

{% api-method-parameter name="actionType" type="string" required=true %}
Specify which action to take. Current actions: "delete".
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
    "message": "Questions deleted successfully",
    "lessEventsNotice": true
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
   "actionType":"delete",
   "groupId":1,
   "recordIds":[
      2,
      1
   ],
   "tab":"qna"
}
```

