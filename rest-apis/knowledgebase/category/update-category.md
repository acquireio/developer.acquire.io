---
description: >-
  This endpoint allows you to update the details of existing category in the
  knowledge base.
---

# Update Category

{% api-method method="put" host="https://{{account\_uid}}.acquire.io/api/v1/kb/category/update/{{id}}" path="" %}
{% api-method-summary %}
Update Category
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to update the details of existing category in the knowledge base.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="number" required=true %}
1
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{API\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Category successfully updated.
{% endapi-method-response-example-description %}

```
{
  "data": {
    "success": true,
    "message": "Category successfully updated."
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### Body \(row\)

```text
{
  "groupId": 1,
  "parentCategory": 0,
  "name": "new",
  "description": "new",
  "categoryIcon": "string",
  "visibleOrder": 0,
  "status": "active"
}
```

