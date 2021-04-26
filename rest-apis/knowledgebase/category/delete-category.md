---
description: This endpoint allows you to delete a category from the knowledge base
---

# Delete Category

{% api-method method="delete" host="https://{{account\_id}}.acquire.io/api/v1/kb/category/delete/{{articleId}}?groupId={{groupId}}" path="" %}
{% api-method-summary %}
Delete Category
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to delete a category from the Knowledge Base. The article ID must be passed in to the endpoint as a path parameter. Warning: This action cannot be undone.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="articleId" type="integer" required=true %}
The article ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{API\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="groupId" type="integer" required=true %}
The Knowledge Base group ID
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Category successfully deleted.
{% endapi-method-response-example-description %}

```
{
  "data": {
    "success": true,
    "message": "Category Successfully deleted.",
    "data": 67
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



