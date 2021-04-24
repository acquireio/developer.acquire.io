---
description: Retrieve details for a single Knowledge Base.
---

# Get Single

{% api-method method="get" host="https://{{account\_uid}}.acquire.io/api/v1/kb/group?id={{id}}" path="" %}
{% api-method-summary %}
Get single Knowledge Base
{% endapi-method-summary %}

{% api-method-description %}
Retrieve details for a single Knowledge Base. The id must be passed in to the endpoint as a query parameter.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{API\_Key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
Knowledge Base ID
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
        "success": true,
        "data": [
            {
                "baseGroupsLang": [
                    {
                        "id": 7,
                        "name": "English",
                        "code": "en",
                        "isDefault": "no"
                    }
                ],
                "createdBy": 107,
                "dateCreated": "2021-04-23T23:52:38.000Z",
                "dateUpdated": "2021-04-23T23:54:05.000Z",
                "id": 6,
                "isDefault": "no",
                "name": "updated kb group",
                "slugKey": "kb-from-api",
                "status": "draft",
                "updatedBy": 107,
                "isSetup": true,
                "customDomain": null
            }
        ]
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



