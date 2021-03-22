---
description: API to list the available users
---

# List

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/account/user" path="" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
API to list the available users
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {api\_key}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="select" type="array" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="where" type="object" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="relations" type="object" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="order" type="object" required=false %}

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
    "count": 3,
    "data": [
      {
        "firstName": "David Guetta",
        "lastName": "",
        "id": 1,
        "type": "user",
        "status": "active",
        "lastLoginId": null,
        "parentId": null,
        "ownerId": null,
        "name": "David Guetta",
        "email": "user@example.com",
        "phone": "+91-1234567890",
        "photo": "",
        "inviteToken": null,
        "language": null,
        "clientId": null,
        "clientAppId": null,
        "clientAuthorizer": null,
        "clientPermissions": null,
        "stateId": null,
        "countryId": null,
        "dateCreated": null,
        "meta": {
          "onboard_setup": {
            "install": false,
            "welcome": false,
            "setupMail": false,
            "setupVoip": false,
            "setupAppStore": false,
            "setupSocialApp": false
          },
          "productUpdate": {
            "data": [],
            "lastSeenArticleLength": 0
          }
        }
      },
      {
        "firstName": "hello user1",
        "lastName": "",
        "id": 19,
        "type": "user",
        "status": "active",
        "lastLoginId": null,
        "parentId": null,
        "ownerId": null,
        "name": "hello user1",
        "email": "hello@acquire.io",
        "phone": null,
        "photo": null,
        "inviteToken": null,
        "language": null,
        "clientId": null,
        "clientAppId": null,
        "clientAuthorizer": null,
        "clientPermissions": null,
        "stateId": null,
        "countryId": null,
        "dateCreated": "2021-02-03T16:59:45.000Z",
        "meta": {
          "onboard_setup": {
            "install": false,
            "welcome": false,
            "setupMail": false,
            "setupVoip": false,
            "setupAppStore": false,
            "setupSocialApp": false
          }
        }
      },
      {
        "firstName": "set2",
        "lastName": "",
        "id": 20,
        "type": "user",
        "status": "active",
        "lastLoginId": null,
        "parentId": null,
        "ownerId": null,
        "name": "set2",
        "email": "set2@acquire.io",
        "phone": null,
        "photo": null,
        "inviteToken": null,
        "language": null,
        "clientId": null,
        "clientAppId": null,
        "clientAuthorizer": null,
        "clientPermissions": null,
        "stateId": null,
        "countryId": null,
        "dateCreated": "2021-02-03T17:00:26.000Z",
        "meta": {
          "onboard_setup": {
            "install": false,
            "welcome": false,
            "setupMail": false,
            "setupVoip": false,
            "setupAppStore": false,
            "setupSocialApp": false
          }
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



