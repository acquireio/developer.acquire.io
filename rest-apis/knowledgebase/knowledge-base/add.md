# Add

{% api-method method="post" host="https://{{account\_uid}}.acquire.io/api/v1" path="/kb/group/add" %}
{% api-method-summary %}
Add Knowledge base
{% endapi-method-summary %}

{% api-method-description %}

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

{% endapi-method-response-example-description %}

```javascript
{
  "data": {
    "success": true,
    "message": "Knowledge base created successfully.",
    "data": {
      "name": "KB Custom Group Acquire",
      "slugKey": "kb-custom-group-acquire",
      "createdBy": 28,
      "updatedBy": 28,
      "dateCreated": "2021-04-06T09:27:15.000Z",
      "dateUpdated": "2021-04-06T09:27:15.000Z",
      "id": 4,
      "isDefault": "no",
      "status": "draft",
      "internalApp": "no",
      "widgetApp": "no",
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
  "name": "KB Custom Group Acquire",
  "customDomain": "customkb-acquire.com",
  "language": "en"
}
```



