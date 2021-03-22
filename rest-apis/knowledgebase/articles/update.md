# Update

{% api-method method="put" host="https://{{account\_uid}}.acquire.io/api/v1" path="/kb/article/update/:id" %}
{% api-method-summary %}
Update Article
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
