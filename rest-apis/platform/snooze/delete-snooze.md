---
description: Delete a specific Snooze
---

# Delete Snooze

{% api-method method="delete" host="https://{{acount\_id}}.acquire.io/api/v1/crm/follow-up/1" path="" %}
{% api-method-summary %}
Delete Snooze
{% endapi-method-summary %}

{% api-method-description %}
API to delete a specific snooze based on its ID
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
ID of the snooze to be deleted
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

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
    "message": "Snooze has been removed successfully"
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



