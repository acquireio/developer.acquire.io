---
description: >-
  This endpoint allows you to update the details of an existing article in the
  knowledge base.
---

# Update Article

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/kb/article/update/{{id}}" path="" %}
{% api-method-summary %}
Update Article
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to update the details of an existing article in the knowledge base.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="number" required=true %}
Article ID
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
Article successfully updated.
{% endapi-method-response-example-description %}

```
{
  "data": {
    "success": true,
    "message": "Article update successfully"
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
  "articleSlug": "string",
  "featuresImage": "string",
  "groupId": 0,
  "title": "",
  "tags": [
    0
  ],
  "description": "",
  "jsonContent": {},
  "departmentIds": [
    1,
    2
  ],
  "relatedArtIds": [
    1,
    2
  ],
  "addCategory": [
    "name"
  ],
  "articleCategories": [
    0
  ],
  "seoTitle": "string",
  "seoDescription": "string",
  "author": 0,
  "botAssigned": "no",
  "autoRelated": "no",
  "access": "internal",
  "status": "draft"
}
```

