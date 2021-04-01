# List All Tags

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/tag" path="" %}
{% api-method-summary %}
List all tags
{% endapi-method-summary %}

{% api-method-description %}
Retrieve a list of all tags.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="order" type="object" required=false %}
Object type expects field name by which you want to order followed by values eg: {"id":"DESC"}
{% endapi-method-parameter %}

{% api-method-parameter name="relations" type="object" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="select" type="array" required=false %}

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
    "count": 1,
    "data": [
      {
        "id": 1,
        "name": "testings",
        "color": "#3F95FD",
        "userId": 12,
        "type": [
          "contact"
        ],
        "dateCreated": "2021-03-17T06:25:56.000Z",
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
    ]
  }
}

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

