# Update

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1" path="/kb/group/update/{{id}}" %}
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
      "id": 27,
      "name": "KB2 New",
      "isDefault": "no",
      "slugKey": "kb2",
      "createdBy": 1,
      "updatedBy": 1,
      "status": "draft",
      "internalApp": "no",
      "widgetApp": "no",
      "dateCreated": "2021-03-19T14:01:22.000Z",
      "dateUpdated": "2021-03-19T14:09:42.663Z"
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
  "name": "KB2 New",
  "language": "en",
  "customDomain": ""
}
```

