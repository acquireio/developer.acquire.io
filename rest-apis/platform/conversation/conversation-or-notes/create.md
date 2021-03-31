# Create

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/note/create?contactId={{contactId}}" path="" %}
{% api-method-summary %}
Create a Note
{% endapi-method-summary %}

{% api-method-description %}
Create a note. The **contact\_id** must be passed in to the body as a query parameter. The body must contain a `"type"` key set to `"note"`.   
  
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="contactId" type="integer" required=true %}
The contact's ID
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
    "contactId": "90",
    "userId": 1,
    "title": "this is test note title",
    "description": "this is test note description",
    "type": "note",
    "dateCreated": "2021-03-11T11:47:51.874Z",
    "id": 13,
    "users": [
      {
        "note": {
          "contactId": "90",
          "userId": 1,
          "title": "this is test note title",
          "description": "this is test note description",
          "type": "note",
          "dateCreated": "2021-03-11T11:47:51.874Z",
          "id": 13
        },
        "userId": 1
      }
    ],
    "lastMessage": {
      "userId": 1,
      "message": "this is test note",
      "type": "message",
      "parentId": null,
      "dateCreated": "2021-03-11T11:47:52.000Z",
      "note": {
        "id": 13,
        "contactId": 90,
        "userId": 1,
        "type": "note",
        "title": "this is test note title",
        "description": "this is test note description",
        "dateCreated": "2021-03-11T11:47:52.000Z"
      },
      "id": 15,
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
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

**Body \(raw\)**

```text
{
  "type": "note",
  "title": "this is test note title",
  "description": "this is test note description",
  "message": "this is test note",
  "mentionUsers": [
    "00"
  ]
}
```

