---
description: Add a new category in the Knowledge Base.
---

# Add Category

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/kb/category/add" path="" %}
{% api-method-summary %}
Add New Category
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to add a new category in the Knowledge Base.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Authentication token to track down who is emptying our stocks.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="name" type="string" required=true %}
Name of the category. Must be unique.
{% endapi-method-parameter %}

{% api-method-parameter name="groupId" type="integer" required=true %}
ID of the Knowledge Base group you are adding the category to
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Category successfully added.
{% endapi-method-response-example-description %}

```
{
  "data": {
    "success": true,
    "message": "Category successfully added."
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
  "name": "string",
  "description": "string",
  "categoryIcon": "string",
  "visibleOrder": 0,
  "status": "draft"
}
```



