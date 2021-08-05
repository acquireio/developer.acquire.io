---
description: Lists all the contacts for an account
---

# List all contacts

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/objects/contact" path="" %}
{% api-method-summary %}
Get contacts
{% endapi-method-summary %}

{% api-method-description %}
 Retrieve a list of all contacts from the platform's `Contact List`. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
 Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="limit" type="string" required=false %}
Limits the number of results
{% endapi-method-parameter %}

{% api-method-parameter name="select" type="array" required=false %}
dateCreate \| dateUpdated \| id \| parent
{% endapi-method-parameter %}

{% api-method-parameter name="where" type="array" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="relations" type="array" required=false %}
Can be one of company \| cases \| tags \| visits \| timeline \| fields
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
        "list": [
            {
                "dateCreated": "2020-09-09T10:01:36.000Z",
                "dateUpdated": "2020-09-09T10:02:04.000Z",
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
                "company": {
                    "dateCreated": "2020-09-09T10:02:01.000Z",
                    "dateUpdated": null,
                    "id": 3,
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
                "tags": [],
                "latestTimelineId": "12",
                "caseId": "6",
                "latestObjectType": "case",
                "title": "test : ",
                "description": "hi",
                "channel": "chat",
                "status": "active",
                "agentList": [
                    {
                        "departments": [],
                        "roles": [],
                        "id": 1,
                        "name": "Surendra Suthar",
                        "firstName": "Surendra Suthar",
                        "lastName": "",
                        "photo": "",
                        "email": "surendra@acquire.io",
                        "clientId": "",
                        "parentId": 0,
                        "title": "Surendra Suthar",
                        "url": "",
                        "alt": "Surendra Suthar"
                    }
                ],
                "departmentList": [],
                "lastViewObject": null,
                "clientUserId": null,
                "contactCompanyCount": 1,
                "companyId": 3,
                "totalTimeline": 1,
                "lastDateUpdated": "2020-09-09 10:02:04",
                "totalNotes": 0,
                "totalViews": 0,
                "totalCase": 1,
                "caseDateUpdated": "2020-09-09T10:02:04.000Z",
                "msgUnread": 0,
                "channels": [
                    "chat"
                ],
                "firstInteractionType": null,
                "lastInteractionType": "chat",
                "isBlocked": "NO",
                "lastVisit": {
                    "id": 23,
                    "contactId": 82,
                    "title": "Acquire | Test Simulate Page",
                    "url": "https://suthar.uat.env.acquire.io/simulate",
                    "source": "",
                    "dateCreated": "2020-09-09T10:01:36.000Z"
                },
                "firstVisit": {
                    "id": 24,
                    "contactId": 82,
                    "title": "Acquire | Test Simulate Page",
                    "url": "https://suthar.uat.env.acquire.io/simulate",
                    "source": "",
                    "dateCreated": "2020-09-10T03:33:38.000Z"
                },
                "interaction": [],
                "snoozeInContact": false
            },
            {
                "dateCreated": "2020-08-18T13:10:59.000Z",
                "dateUpdated": "2020-08-18T13:12:13.000Z",
                "id": 80,
                "clientType": "web",
                "clientName": "Chrome",
                "clientVersion": "84.0",
                "clientOsName": "Windows",
                "clientOsVersion": "10",
                "clientDeviceType": "Desktop",
                "clientDeviceVendor": null,
                "clientDeviceModel": null,
                "clientDetails": {
                    "ua": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/84.0.4147.125 Safari/537.36",
                    "engine": {
                        "name": "Blink",
                        "version": "84.0.4147.125"
                    },
                    "network": {
                        "type": "3g",
                        "speed": "2.25"
                    }
                },
                "fields": {
                    "city": "Barmer",
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
                    "ip": "157.37.175.233"
                },
                "company": {
                    "fields": {}
                },
                "tags": [],
                "latestTimelineId": "11",
                "viewId": "7",
                "latestObjectType": "view",
                "title": "Book a Meeting",
                "description": "Book a Meeting",
                "channel": "view",
                "status": null,
                "agentList": [],
                "departmentList": [],
                "lastViewObject": {
                    "viewId": 7,
                    "iconImageUrl": "../../../../../assets/app-store/book_a_meeting.svg",
                    "iconFont": null
                },
                "clientUserId": null,
                "contactCompanyCount": null,
                "companyId": null,
                "totalTimeline": 1,
                "lastDateUpdated": "2020-08-18 13:12:13",
                "totalNotes": 0,
                "totalViews": 1,
                "totalCase": 0,
                "msgUnread": 0,
                "channels": [
                    "view"
                ],
                "firstInteractionType": null,
                "lastInteractionType": "view",
                "isBlocked": "NO",
                "lastVisit": {
                    "id": 18,
                    "contactId": 80,
                    "title": "Acquire | Test Simulate Page",
                    "url": "https://suthar.uat.env.acquire.io/simulate",
                    "source": "",
                    "dateCreated": "2020-08-18T13:10:59.000Z"
                },
                "firstVisit": {
                    "id": 18,
                    "contactId": 80,
                    "title": "Acquire | Test Simulate Page",
                    "url": "https://suthar.uat.env.acquire.io/simulate",
                    "source": "",
                    "dateCreated": "2020-08-18T13:10:59.000Z"
                },
                "interaction": [],
                "snoozeInContact": false
            },
            {
                "dateCreated": "2020-08-18T07:02:07.000Z",
                "dateUpdated": "2020-08-18T10:56:32.000Z",
                "id": 79,
                "clientType": "web",
                "clientName": "Chrome",
                "clientVersion": "84.0",
                "clientOsName": "Windows",
                "clientOsVersion": "10",
                "clientDeviceType": "Desktop",
                "clientDeviceVendor": null,
                "clientDeviceModel": null,
                "clientDetails": {
                    "ua": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/84.0.4147.135 Safari/537.36",
                    "engine": {
                        "name": "Blink",
                        "version": "84.0.4147.135"
                    },
                    "network": {
                        "type": "4g",
                        "speed": "13.32"
                    }
                },
                "fields": {
                    "city": "Ahmedabad",
                    "state": "Gujarat",
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
                    "ip": "103.85.11.73"
                },
                "company": {
                    "fields": {}
                },
                "tags": [],
                "latestTimelineId": "10",
                "viewId": "6",
                "latestObjectType": "view",
                "title": "Book a Meeting",
                "description": "Book a Meeting",
                "channel": "view",
                "status": null,
                "agentList": [],
                "departmentList": [],
                "lastViewObject": {
                    "viewId": 6,
                    "iconImageUrl": "../../../../../assets/app-store/book_a_meeting.svg",
                    "iconFont": null
                },
                "clientUserId": null,
                "contactCompanyCount": null,
                "companyId": null,
                "totalTimeline": 2,
                "lastDateUpdated": "2020-08-18 10:56:32",
                "totalNotes": 0,
                "totalViews": 2,
                "totalCase": 0,
                "msgUnread": 0,
                "channels": [
                    "view"
                ],
                "firstInteractionType": null,
                "lastInteractionType": "view",
                "isBlocked": "NO",
                "lastVisit": {
                    "id": 11,
                    "contactId": 79,
                    "title": "Acquire | Test Simulate Page",
                    "url": "https://suthar.uat.env.acquire.io/simulate",
                    "source": "",
                    "dateCreated": "2020-08-18T07:02:07.000Z"
                },
                "firstVisit": {
                    "id": 22,
                    "contactId": 79,
                    "title": "Acquire | Test Simulate Page",
                    "url": "https://suthar.uat.env.acquire.io/simulate",
                    "source": "",
                    "dateCreated": "2020-08-24T04:15:22.000Z"
                },
                "interaction": [],
                "snoozeInContact": false
            },
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
                "company": {
                    "dateCreated": "2020-08-12T07:06:24.000Z",
                    "dateUpdated": null,
                    "id": 2,
                    "fields": {
                        "name": "Facebook",
                        "website": "facebook.com",
                        "logo": "https://organization.uat.env.acquire.io/logo/facebook.com.png"
                    }
                },
                "tags": [],
                "latestTimelineId": "8",
                "viewId": "4",
                "latestObjectType": "view",
                "title": "Book a Meeting",
                "description": "Book a Meeting",
                "channel": "view",
                "status": null,
                "agentList": [],
                "departmentList": [],
                "lastViewObject": {
                    "viewId": 4,
                    "iconImageUrl": "../../../../../assets/app-store/book_a_meeting.svg",
                    "iconFont": null
                },
                "clientUserId": null,
                "contactCompanyCount": 1,
                "companyId": 2,
                "totalTimeline": 1,
                "lastDateUpdated": "2020-08-10 09:24:59",
                "totalNotes": 0,
                "totalViews": 1,
                "totalCase": 0,
                "msgUnread": 0,
                "channels": [
                    "view"
                ],
                "firstInteractionType": null,
                "lastInteractionType": "view",
                "isBlocked": "NO",
                "lastVisit": {
                    "id": 8,
                    "contactId": 78,
                    "title": "Acquire | Test Simulate Page",
                    "url": "https://suthar.uat.env.acquire.io/simulate",
                    "source": "",
                    "dateCreated": "2020-08-10T08:32:48.000Z"
                },
                "firstVisit": {
                    "id": 10,
                    "contactId": 78,
                    "title": "Acquire | Test Simulate Page",
                    "url": "https://suthar.uat.env.acquire.io/simulate",
                    "source": "",
                    "dateCreated": "2020-08-10T08:39:05.000Z"
                },
                "interaction": [],
                "snoozeInContact": false
            },
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
                "company": {
                    "dateCreated": "2020-08-11T11:07:46.000Z",
                    "dateUpdated": "2020-08-11T11:07:46.000Z",
                    "id": 1,
                    "fields": {
                        "name": "new company"
                    }
                },
                "tags": [],
                "latestTimelineId": "6",
                "viewId": "2",
                "latestObjectType": "view",
                "title": "DocuSign: Test Email",
                "description": "DocuSign: Test Email",
                "channel": "view",
                "status": null,
                "agentList": [],
                "departmentList": [],
                "lastViewObject": {
                    "viewId": 2,
                    "iconImageUrl": "../../../../../assets/app-store/docusign.svg",
                    "iconFont": null
                },
                "clientUserId": null,
                "contactCompanyCount": 1,
                "companyId": 1,
                "totalTimeline": 6,
                "lastDateUpdated": "2020-07-08 07:10:58",
                "totalNotes": 0,
                "totalViews": 3,
                "totalCase": 3,
                "msgUnread": 0,
                "channels": [
                    "view"
                ],
                "firstInteractionType": null,
                "lastInteractionType": "view",
                "isBlocked": "NO",
                "lastVisit": {
                    "id": 2,
                    "contactId": 77,
                    "title": "Acquire | Test Simulate Page",
                    "url": "https://suthar.uat.env.acquire.io/simulate",
                    "source": "",
                    "dateCreated": "2020-05-22T06:04:45.000Z"
                },
                "firstVisit": {
                    "id": 7,
                    "contactId": 77,
                    "title": "Acquire | Test Simulate Page",
                    "url": "https://suthar.uat.env.acquire.io/simulate",
                    "source": "",
                    "dateCreated": "2020-07-08T07:03:57.000Z"
                },
                "interaction": [],
                "snoozeInContact": false
            },
            {
                "dateCreated": "2020-05-27T05:52:05.000Z",
                "dateUpdated": "2020-05-27T05:52:22.000Z",
                "id": 1,
                "clientType": "web",
                "clientName": "Chrome",
                "clientVersion": "81.0",
                "clientOsName": "Windows",
                "clientOsVersion": "10",
                "clientDeviceType": null,
                "clientDeviceVendor": null,
                "clientDeviceModel": null,
                "clientDetails": {
                    "ua": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/81.0.4044.138 Safari/537.36",
                    "engine": {
                        "name": "Blink",
                        "version": "81.0.4044.138"
                    },
                    "network": {
                        "type": "4g",
                        "speed": "4.41"
                    }
                },
                "fields": {
                    "city": "Jodhpur",
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
                    "ip": "103.61.112.45"
                },
                "company": {
                    "fields": {}
                },
                "tags": [],
                "latestTimelineId": "1",
                "caseId": "1",
                "latestObjectType": "case",
                "title": "#1 : test",
                "description": "test",
                "channel": "chat",
                "status": "closed",
                "agentList": [
                    {
                        "departments": [],
                        "roles": [],
                        "id": 1,
                        "name": "Surendra Suthar",
                        "firstName": "Surendra Suthar",
                        "lastName": "",
                        "photo": "",
                        "email": "surendra@acquire.io",
                        "clientId": "",
                        "parentId": 0,
                        "title": "Surendra Suthar",
                        "url": "",
                        "alt": "Surendra Suthar"
                    }
                ],
                "departmentList": [],
                "lastViewObject": null,
                "clientUserId": null,
                "contactCompanyCount": null,
                "companyId": null,
                "totalTimeline": 1,
                "lastDateUpdated": "2020-05-27 05:52:22",
                "totalNotes": 0,
                "totalViews": 0,
                "totalCase": 1,
                "caseDateUpdated": "2020-05-27T05:52:22.000Z",
                "msgUnread": 0,
                "channels": [
                    "chat"
                ],
                "firstInteractionType": null,
                "lastInteractionType": "chat",
                "isBlocked": "NO",
                "lastVisit": {
                    "id": 1,
                    "contactId": 1,
                    "title": "Acquire | Test Simulate Page",
                    "url": "https://suthar.uat.env.acquire.io/simulate",
                    "source": "",
                    "dateCreated": "2020-05-27T05:52:05.000Z"
                },
                "firstVisit": {
                    "id": 1,
                    "contactId": 1,
                    "title": "Acquire | Test Simulate Page",
                    "url": "https://suthar.uat.env.acquire.io/simulate",
                    "source": "",
                    "dateCreated": "2020-05-27T05:52:05.000Z"
                },
                "interaction": [],
                "snoozeInContact": false
            }
        ],
        "counts": {
            "total": 6,
            "records": 6,
            "pending": 0,
            "active": 1
        }
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/contact/list" path="" %}
{% api-method-summary %}
Filter Contact List
{% endapi-method-summary %}

{% api-method-description %}
Filters the contact list based on the search results or apply filters to it
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="search" type="string" required=false %}
Specify the string value to search
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
        "list": [
            {
                "id": 6545537,
                "meta": {},
                "archive": "no",
                "field_id": 2,
                "value": "viswanath.sarma@acquire.io",
                "owner": "contact",
                "object": "contact",
                "key": "email",
                "type": "text",
                "config": "{\"input\": {\"type\": \"text\", \"label\": \"Email!!!!\", \"required\": false, \"placeholder\": \"\", \"validationType\": \"format\", \"validationFormat\": \"email\", \"requiredErrorMessage\": \"Unfortunately this cannot be blank.\", \"validationErrorMessage\": \"Oops! Looks like format you entered is wrong. Can you please recheck your email?\"}, \"label\": \"Email!!!!\", \"backend\": {\"list\": false}, \"capture\": [\"api\"], \"online_order\": 9, \"offline_order\": 8492}",
                "system": "yes",
                "mainContactId": 6545537,
                "contactId": 6545537,
                "clientType": null,
                "clientName": null,
                "clientVersion": null,
                "clientOsName": null,
                "clientOsVersion": null,
                "clientDeviceType": null,
                "clientDeviceVendor": null,
                "clientDeviceModel": null,
                "companyId": 149,
                "dateCreated": "2021-07-16 11:49:24",
                "dateUpdated": "2021-07-16 11:49:51",
                "clientDetails": null,
                "fields": {
                    "email": "viswanath.sarma@acquire.io",
                    "city": "",
                    "state": null,
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
                    "ip": "2405:201:c032:1014:76e9:781c:e56d:ebc",
                    "calling_code": "1",
                    "contact_country_flag": "USA"
                },
                "tags": [],
                "company": {
                    "fields": {
                        "name": "Acquire",
                        "website": "acquire.io",
                        "logo": "https://organization.uat.env.acquire.io/logo/acquire.io.png",
                        "industry": null,
                        "description": "",
                        "source": null,
                        "employees": "100",
                        "foundation": null,
                        "address": ""
                    },
                    "id": 149,
                    "dateCreated": "2021-05-20 09:57:31",
                    "dateUpdated": "2021-05-25 06:04:13"
                }
            },
            {
                "id": 57,
                "meta": {},
                "archive": "no",
                "field_id": 2,
                "value": "viswanath.sarma@acquire.io",
                "owner": "contact",
                "object": "contact",
                "key": "email",
                "type": "text",
                "config": "{\"input\": {\"type\": \"text\", \"label\": \"Email!!!!\", \"required\": false, \"placeholder\": \"\", \"validationType\": \"format\", \"validationFormat\": \"email\", \"requiredErrorMessage\": \"Unfortunately this cannot be blank.\", \"validationErrorMessage\": \"Oops! Looks like format you entered is wrong. Can you please recheck your email?\"}, \"label\": \"Email!!!!\", \"backend\": {\"list\": false}, \"capture\": [\"api\"], \"online_order\": 9, \"offline_order\": 8492}",
                "system": "yes",
                "mainContactId": 57,
                "contactId": 57,
                "clientType": "web",
                "clientName": "Chrome",
                "clientVersion": "84.0",
                "clientOsName": "Windows",
                "clientOsVersion": "8.1",
                "clientDeviceType": null,
                "clientDeviceVendor": null,
                "clientDeviceModel": null,
                "companyId": null,
                "dateCreated": "2020-08-05 10:48:24",
                "dateUpdated": "2021-07-05 06:29:13",
                "clientDetails": {
                    "ua": "Mozilla/5.0 (Windows NT 6.3; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/84.0.4147.105 Safari/537.36",
                    "engine": {
                        "name": "Blink",
                        "version": "84.0.4147.105"
                    },
                    "network": {
                        "type": "3g",
                        "speed": "2.52"
                    }
                },
                "fields": {
                    "name": "Viswanath Sarma",
                    "email": "viswanath.sarma@acquire.io",
                    "phone": "7412356890"
                },
                "tags": [],
                "company": {
                    "fields": {}
                }
            }
        ],
        "counts": {
            "filteredCount": 2
        }
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Body\(raw\)

```text
{
  "payload": {},
  "page": 0,
  "limit": 0,
  "search": "viswanath.sarma@acquire.io"
}
```

