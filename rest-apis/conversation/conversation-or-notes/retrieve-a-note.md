---
description: Retrieve a single note.
---

# Retrieve a note

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/note/get/{{noteId}}" path="" %}
{% api-method-summary %}
Single Note
{% endapi-method-summary %}

{% api-method-description %}
Retrieve a single note. The **noteId** must be passed in to the endpoint as a path parameter.   
  
**noteId** - The note's ID. To retrieve a list of noteIds, submit a GET request to List all notes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="noteId" type="integer" required=true %}
ID of the note
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
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
        "id": 1,
        "contactId": 1,
        "userId": 1,
        "type": "note",
        "title": "this is test note titleeqqw",
        "description": null,
        "dateCreated": "2020-09-11T12:17:33.000Z",
        "users": [
            {
                "id": 1,
                "noteId": 1,
                "userId": 1,
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
                    "type": "user",
                    "accessLevel": null
                }
            }
        ],
        "lastMessage": {
            "id": 1,
            "noteId": 1,
            "parentId": null,
            "userId": 1,
            "type": "message",
            "message": "Instantly engage your customers on any channel using the best communication tools, all from one dashboard.",
            "dateCreated": "2020-09-11T12:17:33.000Z"
        }
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



