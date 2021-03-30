# Update company

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/crm/objects/company/{{companyId}}" path="" %}
{% api-method-summary %}
Update a Company
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
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
       "dateCreated": "2020-09-10T11:44:05.000Z",
       "dateUpdated": "2020-09-10T11:44:05.000Z",
       "id": 77,
       "fields": {
           "name": "Updated Company",
           "website": "website.com",
           "industry": "IT",
           "description": "No description ",
           "source": "No source added",
           "revenue": "1050000",
           "city": "SF1",
           "state": "california"
       }
   }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

**Body \(raw\)**

```javascript
{
    "fields": {
        "name": "ZeryUpdated",
        "website": "zeryUpdated.com",
        "logo": "IT",
        "industry": "IT",
        "description": "No description ",
        "source": "No source added",
        "revenue": "1050000",
        "city": "SF1",
        "state": "california"
    },
    "dateCreated": "string",
    "dateUpdated": "string"
}
```

