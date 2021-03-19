---
description: API to Update a specific tag details
---

# Update Tag

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/crm/tag/2?name=test&color=%233F95FD&id=12" path="" %}
{% api-method-summary %}
Update Tag
{% endapi-method-summary %}

{% api-method-description %}
API to update a specific case
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
ID of tag
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="name" type="string" required=false %}
Specify name with the updated name
{% endapi-method-parameter %}

{% api-method-parameter name="color" type="string" required=false %}
Specify color code to be updated color code
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="array" required=false %}
Specify the assignment to contact or case
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
    "id": 2,
    "name": null,
    "color": null,
    "userId": 12,
    "type": null,
    "dateCreated": "2021-03-18T08:11:17.000Z",
    "user": {
      "departments": [],
      "roles": [],
      "id": 12,
      "name": "vivek",
      "firstName": "vivek",
      "lastName": "",
      "photo": "",
      "email": "vivek@acquire.io",
      "clientId": "",
      "meta": {
        "fields": {
          "onboard_setup": {
            "structValue": {
              "fields": {
                "install": {
                  "boolValue": false,
                  "kind": "boolValue"
                },
                "welcome": {
                  "boolValue": false,
                  "kind": "boolValue"
                },
                "setupMail": {
                  "boolValue": false,
                  "kind": "boolValue"
                },
                "setupVoip": {
                  "boolValue": false,
                  "kind": "boolValue"
                },
                "setupAppStore": {
                  "boolValue": false,
                  "kind": "boolValue"
                },
                "setupSocialApp": {
                  "boolValue": false,
                  "kind": "boolValue"
                }
              }
            },
            "kind": "structValue"
          }
        }
      },
      "parentId": 0,
      "metaDetails": {
        "isBotClient": false,
        "label": ""
      },
      "type": "user",
      "accessLevel": null
    }
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

