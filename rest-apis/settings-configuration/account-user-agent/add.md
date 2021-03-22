---
description: API to add a new user
---

# Add

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/account/user" path="" %}
{% api-method-summary %}
Add
{% endapi-method-summary %}

{% api-method-description %}
API to add a new user
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {api\_key}
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
    "user": {
      "firstName": "",
      "lastName": "",
      "name": "testing User",
      "email": "testings@acquire.io",
      "type": "user",
      "status": "active",
      "dateCreated": "2021-03-22T10:37:36.981Z",
      "lastLoginId": null,
      "parentId": null,
      "ownerId": null,
      "phone": null,
      "photo": null,
      "inviteToken": null,
      "language": null,
      "clientId": null,
      "clientAppId": null,
      "clientAuthorizer": null,
      "stateId": null,
      "countryId": null,
      "meta": {
        "onboard_setup": {
          "welcome": false,
          "install": false,
          "setupMail": false,
          "setupVoip": false,
          "setupSocialApp": false,
          "setupAppStore": false
        }
      },
      "id": 24,
      "clientPermissions": null,
      "departments": [
        null
      ],
      "roles": [
        {
          "id": 1,
          "roleName": "Administrator",
          "permissions": [
            "*/*"
          ],
          "permissionType": null,
          "meta": null
        }
      ]
    },
    "success": true,
    "message": "New User added Successfully."
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
  "name": "testing User",
  "email": "testings@acquire.io",
  "password": "Acquire@2020",
  "departments": [
    1
  ],
  "roles": [
    1
  ],
  "additionalProp1": {}
}
```

