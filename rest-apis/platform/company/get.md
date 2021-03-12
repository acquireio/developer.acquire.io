---
description: Gets the specified company.
---

# Retrieve a company

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/objects/company/{{companyId}}?relations=fields" path="" %}
{% api-method-summary %}
Single Company
{% endapi-method-summary %}

{% api-method-description %}
This API is used to obtain specific company details.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
Bearer \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*YOUR\_API\_KEY\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\* 
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="relations" type="string" required=false %}
Can be one of fields \| contacts \| companies
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
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
        "id": 7,
        "fields": {
            "name": "Zery12",
            "website": "zery12.com",
            "logo": "IT",
            "industry": "IT",
            "description": "No description ",
            "source": "No source added",
            "revenue": "1050000",
            "city": "SF1",
            "state": "california"
        },
        "contacts": []
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}
