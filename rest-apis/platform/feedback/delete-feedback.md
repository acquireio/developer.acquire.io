---
description: Delete Feedback
---

# Delete Feedback

{% api-method method="delete" host="https://{{account\_id}}.acquire.io/api/v1/crm/feedback?id=37" path="" %}
{% api-method-summary %}
Delete Feedback
{% endapi-method-summary %}

{% api-method-description %}
API to delete feedback
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
\*\*\*\*\*YOUR API KEY\*\*\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="id" type="array" required=true %}
Array of Feedback id's to be deleted
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

