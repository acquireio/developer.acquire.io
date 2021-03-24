# Case List

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/objects/case?limit=2&relations=contact&select=channel" path="" %}
{% api-method-summary %}
Get case list
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

{% api-method-query-parameters %}
{% api-method-parameter name="where" type="array" %}
Specifies the condition to filter, Condition with the column name followed by the expression and the value. For eg: status\|eq\|active
{% endapi-method-parameter %}

{% api-method-parameter name="select" type="string" required=false %}
dateCreated\|dateUpdated\|id\|contactId\| closedBy\|visitId\|title\|description\|status\| closingState\|dateQueue\|dateActive\|dateClosed\| queueId\|meta\|parentId
{% endapi-method-parameter %}

{% api-method-parameter name="relations" type="string" required=false %}
You can pass multiple relations along with the case. Allowed relations : contact\|messages\|cases\|users \|fields\|tags\|feedbacks\|timeline\|parent\| datePending\|queueOrder\|userId\|waitTime
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
        "limit": 2,
        "count": 72,
        "data": [
            {
                "id": 1,
                "channel": "chat",
                "contact": {
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
                    "companyId": 1
                },
                "threadId": 1
            },
            {
                "id": 2,
                "channel": "chat",
                "contact": {
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
                    "companyId": 1
                },
                "threadId": 2
            }
        ]
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



