---
description: Delete a specific tag
---

# Delete Tag

{% api-method method="delete" host="https://{{account\_id}}.acquire.io/api/v1/crm/tag?id=2" path="" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
API to delete tags
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="ids" type="array" required=true %}
Array of tag ids to delete tags
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
    "deleted": 1
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

