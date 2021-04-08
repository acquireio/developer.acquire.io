---
description: API to get the default bot group
---

# Get Default Group

{% api-method method="get" host="https:/{{account\_id}}.acquire.io/api/v1/bot/group/default" path="" %}
{% api-method-summary %}
Get Default Group
{% endapi-method-summary %}

{% api-method-description %}
API to get the default bot group
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" required=true type="string" %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
 
{% endapi-method-response-example-description %}

{% tabs %}
{% tab title="Plain Text" %}
```
{
  "data": {
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
}
```
{% endtab %}
{% endtabs %}
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

