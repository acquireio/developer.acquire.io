# Add company

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/objects/company" path="" %}
{% api-method-summary %}
Creates a new company
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to create company. The body requires a `"fields"` key. See body example below.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="dateUpdated" type="string" required=false %}
2020-09-10T11:44:05.143Z
{% endapi-method-parameter %}

{% api-method-parameter name="dateCreated" type="string" required=false %}
2020-09-10T11:44:05.143Z
{% endapi-method-parameter %}

{% api-method-parameter name="fields" type="object" required=true %}
 
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "data": {
        "fields": {
            "name": "Website.com Solutions Inc.",
            "website": "website.com",
            "industry": "IT",
            "description": "No description ",
            "source": "No source added",
            "revenue": "1050000",
            "city": "SF1",
            "state": "california",
            "logo": "https://organization.uat.env.acquire.io/logo/website.com.png"
        },
        "dateCreated": "2020-09-10T11:44:05.000Z",
        "dateUpdated": "2020-09-10T11:44:05.143Z",
        "id": 8
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

**Body \(raw\)**

```text
{
   "fields": {
       "name": "company name",
       "website": "website.com",
       "industry": "IT",
       "description": "No description ",
       "source": "No source added",
       "revenue": "1050000",
       "city": "SF1",
       "state": "california"
   },
   "dateCreated": "2020-09-10T11:44:05.143Z",
   "dateUpdated": "2020-09-10T11:44:05.143Z"
}
```

