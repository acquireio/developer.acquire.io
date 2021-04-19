---
description: Add a new article to a Knowledge Base
---

# Add Article

{% api-method method="post" host="https://{{account\_uid}}.acquire.io/api/v1/kb/article/add" path="" %}
{% api-method-summary %}
Add New Article
{% endapi-method-summary %}

{% api-method-description %}
Add a new article to a Knowledge Base. The body must have the required keys:   
   
`"groupId"` - The Knowledge Base ID   
  
`"title"` - Title of the article   
  
`"slug"` - The slug for the article
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
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
  "articleSlug": "New",
  "featuresImage": "",
  "title": "New Article samples",
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

