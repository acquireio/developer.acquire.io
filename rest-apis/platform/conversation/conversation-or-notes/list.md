# List all notes

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/note?lcontact\_id={{contact\_id}}" path="" %}
{% api-method-summary %}
List all Notes
{% endapi-method-summary %}

{% api-method-description %}
Retrieve a list of notes. The **contact\_id** must be passed in to the endpoint as a query parameter.   
  
**contact\_id** - The contact's ID. All notes are attached to a contact. To find a contact\_id, log in to Acquire, go to `Contact List` and hover a contact's name or submit a GET request to List All Contacts.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="contact\_id" type="integer" required=true %}
ID of the contact.
{% endapi-method-parameter %}

{% api-method-parameter name="page" type="integer" required=false %}
The page number.
{% endapi-method-parameter %}

{% api-method-parameter name="limit" type="integer" required=false %}
The maximum number of results to display per page.
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
        "count": 5,
        "rows": [
            {
                "id": 7,
                "contactId": 1,
                "userId": 22,
                "type": "note",
                "title": "this is test note titleeqqw",
                "description": null,
                "dateCreated": "2020-09-11T12:33:04.000Z",
                "users": [
                    {
                        "id": 7,
                        "noteId": 7,
                        "userId": 22
                    }
                ],
                "lastMessage": {
                    "id": 9,
                    "noteId": 7,
                    "parentId": null,
                    "userId": 22,
                    "type": "message",
                    "message": "this is test notessssssssssssssssssssssssssssssssssssssss",
                    "dateCreated": "2020-09-11T12:33:04.000Z"
                }
            },
            {
                "id": 4,
                "contactId": 1,
                "userId": 22,
                "type": "note",
                "title": "this is test note title",
                "description": null,
                "dateCreated": "2020-09-11T12:24:28.000Z",
                "users": [
                    {
                        "id": 4,
                        "noteId": 4,
                        "userId": 22
                    }
                ],
                "lastMessage": {
                    "id": 17,
                    "noteId": 4,
                    "parentId": 0,
                    "userId": 93,
                    "type": "message",
                    "message": "this is test note by surendra",
                    "dateCreated": "2021-03-12T05:23:25.000Z"
                }
            },
            {
                "id": 3,
                "contactId": 1,
                "userId": 22,
                "type": "note",
                "title": "this is test note title",
                "description": null,
                "dateCreated": "2020-09-11T12:23:11.000Z",
                "users": [
                    {
                        "id": 3,
                        "noteId": 3,
                        "userId": 22
                    }
                ],
                "lastMessage": {
                    "id": 3,
                    "noteId": 3,
                    "parentId": null,
                    "userId": 22,
                    "type": "message",
                    "message": "this is test note",
                    "dateCreated": "2020-09-11T12:23:11.000Z"
                }
            },
            {
                "id": 2,
                "contactId": 1,
                "userId": 1,
                "type": "note",
                "title": "this is test note title",
                "description": null,
                "dateCreated": "2020-09-11T12:22:09.000Z",
                "users": [
                    {
                        "id": 2,
                        "noteId": 2,
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
                            "metaDetails": {
                                "isBotClient": false,
                                "label": ""
                            },
                            "type": "user",
                            "accessLevel": null
                        }
                    }
                ],
                "lastMessage": {
                    "id": 2,
                    "noteId": 2,
                    "parentId": null,
                    "userId": 1,
                    "type": "message",
                    "message": "this is test note",
                    "dateCreated": "2020-09-11T12:22:09.000Z"
                }
            },
            {
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
                            "metaDetails": {
                                "isBotClient": false,
                                "label": ""
                            },
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
        ]
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

