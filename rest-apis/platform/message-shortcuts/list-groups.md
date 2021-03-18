---
description: API to list all the different shortcut groups available
---

# List Groups

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/message-shortcut/list-all-group" path="" %}
{% api-method-summary %}
List Message Shortcut Groups
{% endapi-method-summary %}

{% api-method-description %}
API to list all the different shortcut groups
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
API TOKEN
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
    "groupList": [
      "TYUYUY"
    ]
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

