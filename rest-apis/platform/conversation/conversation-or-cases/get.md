# Get

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/objects/case/{caseId}?relations=contact&select=status" path="" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="caseId" type="string" required=false %}
The Id of the case to retrieve
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="select" type="string" required=false %}
channel \| status \| dateCreated \| dateUpdated \| id \| contactId \| closedBy \| visitId \| title \| description \| closingState \| dateQueue \| datePending \| dateActive \| dateClosed \| queueId \| queueOrder \| meta \| parentId \| userId \| waitTime
{% endapi-method-parameter %}

{% api-method-parameter name="relations" type="string" required=false %}
contact
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
        "id": 30,
        "channel": "chat",
        "status": "active",
        "contact": {
            "dateCreated": "2020-12-10T11:54:24.000Z",
            "dateUpdated": "2021-03-03T10:19:49.000Z",
            "id": 5,
            "clientType": "web",
            "clientName": "Chrome",
            "clientVersion": "88.0",
            "clientOsName": "Windows",
            "clientOsVersion": "10",
            "clientDeviceType": "Desktop",
            "clientDeviceVendor": null,
            "clientDeviceModel": null,
            "clientDetails": {
                "ua": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/88.0.4324.190 Safari/537.36",
                "engine": {
                    "name": "Blink",
                    "version": "88.0.4324.190"
                },
                "network": {
                    "type": "4g",
                    "speed": "18"
                }
            },
            "meta": {},
            "archive": "no",
            "companyId": null
        },
        "threadId": 30
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

