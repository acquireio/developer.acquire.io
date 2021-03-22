# Add

{% api-method method="post" host="https://{{account\_uid}}.acquire.io/api/v1" path="/kb/article/add" %}
{% api-method-summary %}
Add Article
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Bearer {{API\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Article successfully saved.
{% endapi-method-response-example-description %}

```
{
  "data": {
    "success": true,
    "message": "New Article added Successfully."
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
  "articleSlug": "",
  "featuresImage": "",
  "title": "",
  "description": "",
  "tags": [
    1
  ],
  "jsonContent": {},
  "departmentIds": [
    1,
    2
  ],
  "relatedArtIds": [
    1,
    2
  ],
  "articleCategories": [
    1,
    2
  ],
  "addCategory": [
    "name"
  ],
  "seoTitle": "string",
  "seoDescription": "string",
  "seoKeywords": "string",
  "author": 1,
  "botAssigned": "no",
  "autoRelated": "no",
  "access": "internal",
  "status": "draft"
}
```

