---
description: Delete a specific Snooze
---

# \[Under Construction\] Delete Snooze

{% api-method method="delete" host="https://{{acount\_id}}.acquire.io/api/v1/crm/follow-up/{{snoozeId}}" path="" %}
{% api-method-summary %}
Delete Snooze
{% endapi-method-summary %}

{% api-method-description %}
**This endpoint is under construction**   
  
Delete a specific snooze based on its ID. The **snoozeId** must be passed in to the endpoint as a path parameter. Snoozes may _only_ be deleted by the agent who created them. **Warning**: This action cannot be undone. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="snoozeId" type="integer" required=true %}
ID of the snooze 
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
    "success": true,
    "message": "Snooze has been removed successfully"
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


