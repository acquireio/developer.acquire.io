---
description: Add a new user
---

# Add

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/account/user" path="" %}
{% api-method-summary %}
Add
{% endapi-method-summary %}

{% api-method-description %}
Add a new user. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{API\_KEY}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="name" type="string" required=true %}
Name of the user.
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=true %}
Email of the user. Must be unique.
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" required=true %}
Password of the user \(can be changed later\).
{% endapi-method-parameter %}

{% api-method-parameter name="roles" type="array" required=true %}
Array of integers. The role ID\(s\) the user will be assigned to. 
{% endapi-method-parameter %}

{% api-method-parameter name="department" type="array" required=true %}
Array of integers. The department ID\(s\) the user will be assigned to. Pass empty array if not assigning any department to it
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

