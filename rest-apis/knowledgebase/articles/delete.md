---
description: Delete an article.
---

# Delete Article

{% api-method method="delete" host="https://{{account\_id}}.acquire.io/api/v1/kb/article/delete/{{articleId}}?groupId={{groupdId}}" path="" %}
{% api-method-summary %}
Delete Article
{% endapi-method-summary %}

{% api-method-description %}
Delete an article. The id must be passed in the endpoint as a path parameter. The groupId must be passed in the endpoint as a query parameter. Warning: This action cannot be undone.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="articleId" type="integer" required=true %}
Article's ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Authentication token to track down who is emptying our stocks.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="groupId" type="integer" required=true %}
The group the article belongs to. 
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



