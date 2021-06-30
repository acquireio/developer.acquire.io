---
description: Add a contact.
---

# Add contact

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/objects/contact" path="" %}
{% api-method-summary %}
Add a contact
{% endapi-method-summary %}

{% api-method-description %}
Add a contact. Contacts may be created with attributes such as `"name"`, `"email"`, `"phone"`, `"city"`, etc. See example body below.   
  
You may use Custom Attributes during a POST request. If you're using radio or drop-down fields, ensure that the input matches the options. Use the Custom Attribute key in the fields body. You may find the Custom Attribute key in **Settings &gt; Account Settings &gt; Custom Attributes**. For example:   
`"fields":{  
   "custom attribute key": "my custom attribute"  
}`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="phone" type="string" required=false %}
Contact's phone
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=false %}
Contact's email
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=false %}
Contact's name
{% endapi-method-parameter %}

{% api-method-parameter name="fields" type="object" required=false %}
field body
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
        "dateCreated": "2021-03-10T07:27:53.593Z",
        "dateUpdated": "string",
        "clientType": "web",
        "clientName": "Chrome",
        "clientVersion": "81.0",
        "clientOsName": "Windows",
        "clientOsVersion": "10",
        "clientDeviceType": null,
        "clientDeviceVendor": null,
        "clientDeviceModel": null,
        "clientDetails": {},
        "archive": "no",
        "companyId": null,
        "id": 12,
        "fields": {
            "name": "API  Deo",
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
        "name": "API  Deo",
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

