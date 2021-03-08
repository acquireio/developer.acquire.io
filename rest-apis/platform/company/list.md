---
description: Lists all companies in the account.
---

# List

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/objects/company?limit=20&relations=contacts" path="" %}
{% api-method-summary %}
All Companies
{% endapi-method-summary %}

{% api-method-description %}
This API can be used to retrieve a list of companies with contact objects.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
Bearer \*\*\*\*\*\*\*\*\*\*\*\*YOUR\_API\_KEY\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="select" type="string" required=false %}
Can be one of dateCreated \| dateUpdated \| id \| parent
{% endapi-method-parameter %}

{% api-method-parameter name="relations" type="string" required=false %}
Can be one of contacts \| fields \| parent \| companies
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
        "page": 0,
        "offset": 0,
        "limit": 20,
        "count": 5,
        "data": [
            {
                "dateCreated": "2020-08-11T11:07:46.000Z",
                "dateUpdated": "2020-08-11T11:07:46.000Z",
                "id": 1,
                "parent": null,
                "companies": [],
                "contacts": [
                    {
                        "dateCreated": "2020-05-22T06:04:45.000Z",
                        "dateUpdated": "2020-08-11T11:07:46.000Z",
                        "id": 77,
                        "clientType": "web",
                        "clientName": "Chrome",
                        "clientVersion": "83.0",
                        "clientOsName": "Windows",
                        "clientOsVersion": "10",
                        "clientDeviceType": null,
                        "clientDeviceVendor": null,
                        "clientDeviceModel": null,
                        "clientDetails": {
                            "ua": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/83.0.4103.116 Safari/537.36",
                            "engine": {
                                "name": "Blink",
                                "version": "83.0.4103.116"
                            },
                            "network": {
                                "type": "4g",
                                "speed": "16.56"
                            }
                        },
                        "companyId": 1,
                        "fields": {
                            "name": "Surendra Sutahr",
                            "email": "surendra@docusign.com",
                            "city": "Jaipur",
                            "state": "Rajasthan",
                            "country": {
                                "name": "India",
                                "name_official": "Republic of India",
                                "cca2": "IN",
                                "ccn3": "35",
                                "cca3": "IND",
                                "calling_code1": 91,
                                "region_id": 366,
                                "lat": "20",
                                "lng": "77",
                                "voip_enable": true
                            },
                            "countryId": "387",
                            "ip": "157.37.236.36"
                        },
                        "objectCounts": {
                            "totalCases": 3,
                            "totalNotes": 0,
                            "totalViews": 3
                        }
                    }
                ],
                "fields": {
                    "name": "new company"
                }
            },
            {
                "dateCreated": "2020-08-12T07:06:24.000Z",
                "dateUpdated": null,
                "id": 2,
                "parent": null,
                "companies": [],
                "contacts": [
                    {
                        "dateCreated": "2020-08-10T08:32:48.000Z",
                        "dateUpdated": "2020-08-12T07:06:19.000Z",
                        "id": 78,
                        "clientType": "web",
                        "clientName": "Chrome",
                        "clientVersion": "84.0",
                        "clientOsName": "Windows",
                        "clientOsVersion": "10",
                        "clientDeviceType": null,
                        "clientDeviceVendor": null,
                        "clientDeviceModel": null,
                        "clientDetails": {
                            "ua": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/84.0.4147.105 Safari/537.36",
                            "engine": {
                                "name": "Blink",
                                "version": "84.0.4147.105"
                            },
                            "network": {
                                "type": "4g",
                                "speed": "1.62"
                            }
                        },
                        "companyId": 2,
                        "fields": {
                            "email": "test@facebook.com",
                            "city": "Jaipur",
                            "state": "Rajasthan",
                            "country": {
                                "name": "India",
                                "name_official": "Republic of India",
                                "cca2": "IN",
                                "ccn3": "35",
                                "cca3": "IND",
                                "calling_code1": 91,
                                "region_id": 366,
                                "lat": "20",
                                "lng": "77",
                                "voip_enable": true
                            },
                            "countryId": "387",
                            "ip": "157.37.148.6"
                        },
                        "objectCounts": {
                            "totalCases": 0,
                            "totalNotes": 0,
                            "totalViews": 1
                        }
                    }
                ],
                "fields": {
                    "name": "Facebook",
                    "website": "facebook.com",
                    "logo": "https://organization.uat.env.acquire.io/logo/facebook.com.png"
                }
            },
            {
                "dateCreated": "2020-09-09T10:02:01.000Z",
                "dateUpdated": null,
                "id": 3,
                "parent": null,
                "companies": [],
                "contacts": [
                    {
                        "dateCreated": "2020-09-09T10:01:36.000Z",
                        "dateUpdated": "2020-09-09T10:01:58.000Z",
                        "id": 82,
                        "clientType": "web",
                        "clientName": "Chrome",
                        "clientVersion": "85.0",
                        "clientOsName": "Windows",
                        "clientOsVersion": "10",
                        "clientDeviceType": "Desktop",
                        "clientDeviceVendor": null,
                        "clientDeviceModel": null,
                        "clientDetails": {
                            "ua": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/85.0.4183.83 Safari/537.36",
                            "engine": {
                                "name": "Blink",
                                "version": "85.0.4183.83"
                            },
                            "network": {
                                "type": "4g",
                                "speed": "18"
                            }
                        },
                        "companyId": 3,
                        "fields": {
                            "name": "test",
                            "email": "test@gmailc.om",
                            "phone": "23232323",
                            "city": "Kanpur",
                            "state": "Uttar Pradesh",
                            "country": {
                                "name": "India",
                                "name_official": "Republic of India",
                                "cca2": "IN",
                                "ccn3": "35",
                                "cca3": "IND",
                                "calling_code1": 91,
                                "region_id": 366,
                                "lat": "20",
                                "lng": "77",
                                "voip_enable": true
                            },
                            "countryId": "387",
                            "ip": "112.196.188.108"
                        },
                        "objectCounts": {
                            "totalCases": 1,
                            "totalNotes": 0,
                            "totalViews": 0
                        }
                    }
                ],
                "fields": {
                    "name": "Gmail",
                    "website": "gmailc.om",
                    "logo": null,
                    "industry": null,
                    "description": null,
                    "source": null,
                    "address": null,
                    "employees": null,
                    "foundation": null
                }
            },
            {
                "dateCreated": "2020-09-10T11:44:05.000Z",
                "dateUpdated": "2020-09-10T11:44:05.000Z",
                "id": 4,
                "parent": null,
                "companies": [],
                "contacts": [],
                "fields": {
                    "name": "new company"
                }
            },
            {
                "dateCreated": "2020-09-10T11:44:05.000Z",
                "dateUpdated": "2020-09-10T11:49:52.000Z",
                "id": 5,
                "parent": null,
                "companies": [],
                "contacts": [],
                "fields": {
                    "name": "Zery",
                    "website": "zery.com",
                    "industry": "IT",
                    "description": "No description ",
                    "source": "No source added",
                    "revenue": "100000",
                    "city": "SF",
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
        ]
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

