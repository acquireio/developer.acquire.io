---
description: Delete a feedback question.
---

# Delete feedback

{% api-method method="delete" host="https://{{account\_id}}.acquire.io/api/v1/crm/feedback?id={{id}}" path="" %}
{% api-method-summary %}
Delete Feedback
{% endapi-method-summary %}

{% api-method-description %}
Delete feedback. The **id** must be passed in to the endpoint as a query parameter. **Warning**: this action cannot be undone. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The feedback ID
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
    "deleted": 1
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

