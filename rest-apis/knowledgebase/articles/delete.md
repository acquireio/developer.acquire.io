# Delete

{% api-method method="delete" host="https://{{account\_uid}}.acquire.io/api/v1" path="/kb/article/delete/:id" %}
{% api-method-summary %}
Delete Article
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication token to track down who is emptying our stocks.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="groupId" type="integer" required=true %}
1
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
//Archived
{
  "data": {
    "success": true,
    "message": "Article Successfully Archived.",
    "data": {
      "id": 1646
    }
  }
}

//Deleted
{
  "data": {
    "success": true,
    "message": "Article Successfully Deleted.",
    "data": {
      "id": 1647
    }
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



