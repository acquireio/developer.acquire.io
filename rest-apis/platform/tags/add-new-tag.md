# Add New Tag

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/tag" path="" %}
{% api-method-summary %}
Add a new tag
{% endapi-method-summary %}

{% api-method-description %}
Add a new tag. To choose a color, use hex colors codes and set them to the key of `"color"`. See example body below. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
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
    "dateCreated": "2021-03-18T08:11:17.000Z",
    "userId": 12,
    "name": null,
    "color": null,
    "type": null,
    "id": 2,
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

### Body

```text
{
        "name": "apitest3",
        "color": "#c034eb",
        "type": ["case", "contact"]
}
```

