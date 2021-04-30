---
description: Delete a user
---

# Delete

{% api-method method="delete" host="https://{{account\_id}}.acquire.io/api/v1/account/user?userId={{userId}}" path="" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
Delete a user. The user's ID must be passed in to the endpoint as a query parameter. Warning: This action cannot be undone.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{API\_KEY}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="userId" type="integer" required=true %}
Delete a user
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

