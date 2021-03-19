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

```
{
  "data": {
    "success": true,
    "message": "Knowledge base created successfully.",
    "data": {
      "name": "KB2",
      "slugKey": "kb2",
      "createdBy": 1,
      "updatedBy": 1,
      "dateCreated": "2021-03-19T14:01:22.000Z",
      "dateUpdated": "2021-03-19T14:01:22.000Z",
      "id": 27,
      "isDefault": "no",
      "status": "draft",
      "internalApp": "no",
      "widgetApp": "no"
    }
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
  "name": "KB2",
  "customDomain": "",
  "languages": "en"
}
```

