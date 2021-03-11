# Note message

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/note/add-message" path="" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
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
    "userId": 1,
    "message": "this is test notewwwwwwwwwwwwwwwwwww",
    "type": "message",
    "parentId": 0,
    "dateCreated": "2021-03-11T12:35:32.000Z",
    "note": {
      "id": 10,
      "contactId": 1794,
      "userId": 1,
      "type": "note",
      "title": "this is test note title",
      "description": null,
      "dateCreated": "2020-09-16T06:49:16.000Z"
    },
    "id": 16,
    "user": {
      "departments": [],
      "roles": [],
      "id": 1,
      "name": "Surendra Suthar",
      "firstName": "Surendra Suthar",
      "lastName": "",
      "photo": "https://uat-drive.acquire.io/suthar/media/2020/10/IMG_2353-(3)-201aff39871a8ccc0f3e9ff0.jpg",
      "email": "surendra@acquire.io",
      "clientId": "",
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

**Body\(row\)**

```text
{
  "type": "message",
  "mentionUsers": [
    "00"
  ],
  "message": "this is test note message",
  "parent_id": 0,
  "note_id": 10,
  "contact_id": 90
}
```

