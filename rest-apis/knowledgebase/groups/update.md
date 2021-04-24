---
description: Update details for a group in the Knowledge base.
---

# Update

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/kb/group/update/{{id}}" path="" %}
{% api-method-summary %}
Update Knowledge base
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to update details for a Knowledge Base group. The id must be passed in to the endpoint as a path parameter.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
Knowledge Base ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{API\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="name" type="string" required=false %}
The name of the Knowledge Base
{% endapi-method-parameter %}

{% api-method-parameter name="customDomain" type="string" required=false %}
The URL for the custom domain the Knowledge Base will be hosted on
{% endapi-method-parameter %}

{% api-method-parameter name="language" type="string" required=false %}
The ISO language code the Knowledge Base will be written in 
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
  "data": {
    "success": true,
    "message": "Knowledge base updated successfully.",
    "data": {
      "id": 4,
      "name": "Acquire's Customized KB Articles",
      "isDefault": "no",
      "slugKey": "kb-custom-group-acquire",
      "createdBy": 28,
      "updatedBy": 28,
      "status": "draft",
      "internalApp": "no",
      "widgetApp": "no",
      "dateCreated": "2021-04-06T09:27:15.000Z",
      "dateUpdated": "2021-04-06T09:32:38.203Z",
      "scrapingToken": null
    }
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### Body \(row\)

```javascript
{
  "name": "Acquire's Customized KB Articles",
  "customDomain": "custom-articles.acquire.io",
  "language": "en"
}
```

