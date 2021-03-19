# Update

Update a Customer.

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/objects/contact/2" path="" %}
{% api-method-summary %}
Update a customer
{% endapi-method-summary %}

{% api-method-description %}
Update a customer
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
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
        "id": 2,
        "clientType": "web",
        "clientName": "Chrome",
        "clientVersion": "81.0",
        "clientOsName": "Windows",
        "clientOsVersion": "10",
        "clientDeviceType": null,
        "clientDeviceVendor": null,
        "clientDeviceModel": null,
        "clientDetails": {},
        "meta": {},
        "archive": "no",
        "companyId": 5,
        "fields": {
            "name": "John  Deo",
            "email": "John@acquire.io",
            "phone": "9460731950",
            "city": "San Francisco",
            "state": "California",
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
            "ip": "103.61.112.45"
        }
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
        "name": "John  Deo",
        "email": "John@acquire.io",
        "phone": "9460731950",
        "city": "San Francisco",
        "state": "California",
        "countryId": "517",
        "ip": "103.61.112.45"
    },
    "dateCreated": "string",
    "dateUpdated": "string",
    "clientType": "web",
    "clientName": "Chrome",
    "clientVersion": "81.0",
    "clientOsName": "Windows",
    "clientOsVersion": "10",
    "clientDeviceType": null,
    "clientDeviceVendor": null,
    "clientDeviceModel": null,
    "clientDetails": {}
}
```

