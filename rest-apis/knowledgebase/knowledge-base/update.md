# Update

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/kb/group/update/{{id}}" path="" %}
{% api-method-summary %}
Update Knowledge base
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="number" required=true %}
Knowledge Base ID
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

{% endapi-method-response-example-description %}

```javascript
{
  "data": {
    "success": true,
    "message": "Knowledge base updated successfully.",
    "data": {
      "id": 4,
      "name": "Custom Group Articles of Acquire's KB",
      "isDefault": "no",
      "slugKey": "kb-custom-group-acquire",
      "createdBy": 28,
      "updatedBy": 28,
      "status": "draft",
      "internalApp": "no",
      "widgetApp": "no",
      "dateCreated": "2021-04-06T09:27:15.000Z",
      "dateUpdated": "2021-04-06T09:30:34.980Z",
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
  "name": "Custom Group Articles of Acquire's KB",
  "customDomain": "custom-grp-articles.acquire.io",
  "language": "en"
}
```

