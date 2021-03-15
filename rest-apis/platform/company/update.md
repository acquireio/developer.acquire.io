# Update

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
        "dateCreated": "string",
        "dateUpdated": "string",
        "id": 5,
        "fields": {
            "name": "ZeryUpdated",
            "website": "zeryUpdated.com",
            "logo": "IT",
            "industry": "IT",
            "description": "No description ",
            "source": "No source added",
            "revenue": "1050000",
            "city": "SF1",
            "state": "california",
            "country": {
                "name": "United States",
                "name_official": "United States of America",
                "cca2": "US",
                "ccn3": "84",
                "cca3": "USA",
                "calling_code1": 1,
                "region_id": 496,
                "lat": "38",
                "lng": "-97",
                "voip_enable": true
            },
            "countryId": "517",
            "address": "SF, california",
            "employees": "50-100",
            "foundation": "2020"
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

