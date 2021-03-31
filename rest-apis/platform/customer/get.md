# Retrieve a contact

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/objects/contact/{{contactId}}?relations=company&relations=cases" path="" %}
{% api-method-summary %}
Single contact
{% endapi-method-summary %}

{% api-method-description %}
Identifies a contact by the **contactId** passed in the request and returns the contact information.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="select" type="string" required=false %}
Can be one of id\|clientName\|clientType\|clientVersion\|  
dateUpdated\|dateCreated\|clientOsName\|  
clientOsVersion\|clientDeviceType\|  
clientDeviceVendor\|clientDeviceModel\|  
clientDetails\|companyId
{% endapi-method-parameter %}

{% api-method-parameter name="relations" type="string" required=false %}
Can be one of company \| cases \| fields \| tags \| visits \| timeline
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
        "dateCreated": "2020-08-11T07:25:59.000Z",
        "dateUpdated": "2020-08-11T07:27:14.000Z",
        "id": 1,
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
                "type": "3g",
                "speed": "2.52"
            }
        },
        "meta": {},
        "archive": "no",
        "company": {
            "dateCreated": "2020-08-11T07:26:24.000Z",
            "dateUpdated": null,
            "id": 1,
            "fields": {
                "name": "Yahoo!",
                "website": "yahoo.com",
                "logo": "https://organization.acquire.io/logo/yahoo.com.png"
            }
        },
        "cases": [
            {
                "dateCreated": "2020-08-11T07:26:23.000Z",
                "dateUpdated": "2020-08-11T07:26:28.000Z",
                "id": 1,
                "contactId": 1,
                "closedBy": null,
                "visitId": 1,
                "title": "test : ",
                "description": "",
                "channel": "chat",
                "status": "active",
                "closingState": "handled",
                "dateQueue": "2020-08-11T07:26:23.000Z",
                "datePending": "2020-08-11T07:26:23.000Z",
                "dateActive": "2020-08-11T07:26:28.000Z",
                "dateClosed": null,
                "queueId": null,
                "queueOrder": null,
                "meta": {
                    "_routes": {}
                },
                "parentId": null,
                "userId": null,
                "waitTime": 0,
                "users": [
                    {
                        "id": 2,
                        "caseId": 1,
                        "type": "user",
                        "userId": 1,
                        "role": "owner",
                        "status": "active",
                        "dateCreated": "2020-08-11T07:26:22.000Z",
                        "dateLastAssigned": "2020-10-15T09:01:54.000Z",
                        "closed": "no",
                        "meta": null
                    },
                    {
                        "id": 3,
                        "caseId": 1,
                        "type": "user",
                        "userId": 6,
                        "role": "owner",
                        "status": "rejected",
                        "dateCreated": "2020-08-11T07:26:22.000Z",
                        "dateLastAssigned": "2020-10-15T09:01:54.000Z",
                        "closed": "no",
                        "meta": null
                    },
                    {
                        "id": 4,
                        "caseId": 1,
                        "type": "user",
                        "userId": 7,
                        "role": "owner",
                        "status": "rejected",
                        "dateCreated": "2020-08-11T07:26:22.000Z",
                        "dateLastAssigned": "2020-10-15T09:01:54.000Z",
                        "closed": "no",
                        "meta": null
                    },
                    {
                        "id": 5,
                        "caseId": 1,
                        "type": "user",
                        "userId": 8,
                        "role": "owner",
                        "status": "rejected",
                        "dateCreated": "2020-08-11T07:26:22.000Z",
                        "dateLastAssigned": "2020-10-15T09:01:54.000Z",
                        "closed": "no",
                        "meta": null
                    },
                    {
                        "id": 6,
                        "caseId": 1,
                        "type": "user",
                        "userId": 9,
                        "role": "owner",
                        "status": "rejected",
                        "dateCreated": "2020-08-11T07:26:22.000Z",
                        "dateLastAssigned": "2020-10-15T09:01:54.000Z",
                        "closed": "no",
                        "meta": null
                    },
                    {
                        "id": 7,
                        "caseId": 1,
                        "type": "user",
                        "userId": 10,
                        "role": "owner",
                        "status": "rejected",
                        "dateCreated": "2020-08-11T07:26:22.000Z",
                        "dateLastAssigned": "2020-10-15T09:01:54.000Z",
                        "closed": "no",
                        "meta": null
                    },
                    {
                        "id": 1,
                        "caseId": 1,
                        "type": "contact",
                        "userId": 1,
                        "role": "owner",
                        "status": "active",
                        "dateCreated": "2020-08-11T07:26:22.000Z",
                        "dateLastAssigned": "2020-10-15T09:01:54.000Z",
                        "closed": "no",
                        "meta": null
                    }
                ],
                "threadId": 1
            },
            {
                "dateCreated": "2020-08-11T07:27:14.000Z",
                "dateUpdated": "2020-08-11T07:27:19.000Z",
                "id": 2,
                "contactId": 1,
                "closedBy": null,
                "visitId": 2,
                "title": "test : ",
                "description": "",
                "channel": "chat",
                "status": "active",
                "closingState": "handled",
                "dateQueue": "2020-08-11T07:27:14.000Z",
                "datePending": "2020-08-11T07:27:14.000Z",
                "dateActive": "2020-08-11T07:27:18.000Z",
                "dateClosed": null,
                "queueId": null,
                "queueOrder": null,
                "meta": {
                    "_routes": {}
                },
                "parentId": null,
                "userId": null,
                "waitTime": 0,
                "users": [
                    {
                        "id": 9,
                        "caseId": 2,
                        "type": "user",
                        "userId": 1,
                        "role": "owner",
                        "status": "active",
                        "dateCreated": "2020-08-11T07:27:13.000Z",
                        "dateLastAssigned": "2020-10-15T09:01:54.000Z",
                        "closed": "no",
                        "meta": null
                    },
                    {
                        "id": 10,
                        "caseId": 2,
                        "type": "user",
                        "userId": 6,
                        "role": "owner",
                        "status": "rejected",
                        "dateCreated": "2020-08-11T07:27:13.000Z",
                        "dateLastAssigned": "2020-10-15T09:01:54.000Z",
                        "closed": "no",
                        "meta": null
                    },
                    {
                        "id": 11,
                        "caseId": 2,
                        "type": "user",
                        "userId": 7,
                        "role": "owner",
                        "status": "rejected",
                        "dateCreated": "2020-08-11T07:27:13.000Z",
                        "dateLastAssigned": "2020-10-15T09:01:54.000Z",
                        "closed": "no",
                        "meta": null
                    },
                    {
                        "id": 12,
                        "caseId": 2,
                        "type": "user",
                        "userId": 8,
                        "role": "owner",
                        "status": "rejected",
                        "dateCreated": "2020-08-11T07:27:13.000Z",
                        "dateLastAssigned": "2020-10-15T09:01:54.000Z",
                        "closed": "no",
                        "meta": null
                    },
                    {
                        "id": 13,
                        "caseId": 2,
                        "type": "user",
                        "userId": 9,
                        "role": "owner",
                        "status": "rejected",
                        "dateCreated": "2020-08-11T07:27:13.000Z",
                        "dateLastAssigned": "2020-10-15T09:01:54.000Z",
                        "closed": "no",
                        "meta": null
                    },
                    {
                        "id": 14,
                        "caseId": 2,
                        "type": "user",
                        "userId": 10,
                        "role": "owner",
                        "status": "rejected",
                        "dateCreated": "2020-08-11T07:27:13.000Z",
                        "dateLastAssigned": "2020-10-15T09:01:54.000Z",
                        "closed": "no",
                        "meta": null
                    },
                    {
                        "id": 8,
                        "caseId": 2,
                        "type": "contact",
                        "userId": 1,
                        "role": "owner",
                        "status": "active",
                        "dateCreated": "2020-08-11T07:27:13.000Z",
                        "dateLastAssigned": "2020-10-15T09:01:54.000Z",
                        "closed": "no",
                        "meta": null
                    }
                ],
                "threadId": 2
            }
        ],
        "fields": {
            "name": "test",
            "email": "test@yahoo.com",
            "phone": "1343435454545",
            "city": "Sikar",
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
            "ip": "157.37.227.248"
        }
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

