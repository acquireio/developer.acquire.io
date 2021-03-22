# Add Category

{% api-method method="post" host="https://{{account\_uid}}.acquire.io/api/v1" path="/kb/category/add" %}
{% api-method-summary %}
Add New Category
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Authentication token to track down who is emptying our stocks.
{% endapi-method-parameter %}
{% endapi-method-headers %}
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



