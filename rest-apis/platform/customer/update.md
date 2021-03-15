# Update

Update a Customer.

| Parameter | Value |
| :--- | :--- |
| **Path** | [https://{{account\_id}}.acquire.io/api/v1/crm/objects/contact/2](https://{{account_id}}.acquire.io/api/v1/crm/objects/contact/{{contactId}}) |
| **Method** | **PUT** |
| **Authorization** | Bearer \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*YOUR\_API\_KEY\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\* |
| **Content-type** | application/json |

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

**Response JSON**

```text
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

