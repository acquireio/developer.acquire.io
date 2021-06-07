---
description: Retrieve information for a single user
---

# Get Single

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/account/user/{{userId}}" path="" %}
{% api-method-summary %}
Get Single User
{% endapi-method-summary %}

{% api-method-description %}
Retrieve information for a single user. A `userId` must be passed in to the endpoint as a path parameter. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="userId" type="integer" required=true %}
ID of the user
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" required=true type="string" %}
Bearer {{API\_KEY}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="select" type="array" required=false %}
Specify which fields you'd like in the response
{% endapi-method-parameter %}

{% api-method-parameter name="relations" type="string" required=false %}
Specify the relations with other entities 
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
    },
    "logo": null,
    "organization": "ABC Organization",
    "sso": false
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

