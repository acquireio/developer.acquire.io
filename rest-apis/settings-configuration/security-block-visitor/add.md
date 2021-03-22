---
description: API to add a new block-visitor
---

# Add

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/block-visitor" path="" %}
{% api-method-summary %}
Add
{% endapi-method-summary %}

{% api-method-description %}
API to add a new block-visitor
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {api\_token}
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
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
    "10.10.10.10",
    "11.11.11.11"
  ],
  "blockTill": "2020-03-26T08:19:24.627Z",
  "type": "email"
}
```

