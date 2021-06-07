---
description: Block a contact from the contact list and widget
---

# Add

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/block-visitor" path="" %}
{% api-method-summary %}
Add
{% endapi-method-summary %}

{% api-method-description %}
Use this endpoint to block a contact. Contacts are blocked by their ID. To find a contact's ID, log in to Acquire and hover their name or send a GET request to List all contacts. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{API\_KEY}}
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="blockTill" type="string" required=true %}
Contact block end date.
{% endapi-method-parameter %}

{% api-method-parameter name="data" type="array" required=true %}
ID of the contacts that will be blocked
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
Block type: "contact"
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "data": [
    {
      "data": [
        "10.10.10.10",
        "11.11.11.11"
      ],
      "blockTill": "2020-03-26T23:59:59.000Z",
      "type": "email",
      "blockBy": 1,
      "id": 6,
      "dateCreated": "2021-03-22T09:55:44.000Z",
      "user": {
        "permissions": [
          "*/*"
        ],
        "id": 1,
        "type": "user",
        "name": "David Guetta",
        "firstName": "David Guetta",
        "lastName": "",
        "email": "user@example.com",
        "preference": {
          "accessLevel": [
            "account"
          ],
          "cobrowseAccessUrls": []
        },
        "photo": "",
        "language": "",
        "account": {
          "uid": "5mkg3t",
          "organization": ""
        },
        "loginId": 910
      }
    }
  ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

```text
{
  "data": [
    872
  ],
  "blockTill": "2020-03-26T08:19:24.627Z",
  "type": "contact"
}
```

