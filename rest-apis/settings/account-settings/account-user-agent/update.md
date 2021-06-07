---
description: Update a user
---

# Update

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/account/user/{{userId}}" path="" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Update a user's information. Their userId must be passed in to the endpoint as a path parameter.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="userId" type="integer" required=true %}
ID of the user
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

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
  "data": [
    {
      "firstName": "QA teams",
      "lastName": "",
      "id": 24,
      "type": "user",
      "status": "active",
      "lastLoginId": null,
      "parentId": null,
      "ownerId": null,
      "name": "QA teams",
      "email": "testings@acquire.io",
      "phone": "+91-7418529632",
      "photo": null,
      "inviteToken": null,
      "language": null,
      "clientId": null,
      "clientAppId": null,
      "clientAuthorizer": null,
      "clientPermissions": null,
      "stateId": "ALV",
      "countryId": "291",
      "dateCreated": "2021-03-22T10:37:37.000Z",
      "meta": {
        "onboard_setup": {
          "install": false,
          "welcome": false,
          "setupMail": false,
          "setupVoip": false,
          "setupAppStore": false,
          "setupSocialApp": false
        }
      },
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
      ],
      "departments": []
    }
  ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Body\(raw\)

```text
{
  "id": "24",
  "name": "QA teams",
  "email": "qateams@acquire.io",
  "type": "user",
  "status": "active",
  "password": "Acquire@2020",
  "newPwd": "Acquire@2020",
  "phone": "+91-7418529632",
  "stateId": "ALV",
  "countryId": "291",
  "photo": "WzgxLCJjaGF0L2QwbXdmbGkxcWN1LWRhcmstbG9nby0xNT",
  "departments": [
    1
  ],
  "roles": [
    1
  ],
  "additionalProp1": {}
}
```

