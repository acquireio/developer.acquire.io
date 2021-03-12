# Retrieve note messages

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/note/messages?noteId=8" path="" %}
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

{% api-method-query-parameters %}
{% api-method-parameter name="noteId" type="string" required=false %}
ID of the note.
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
        "count": 2,
        "rows": [
            {
                "id": 11,
                "noteId": 8,
                "parentId": null,
                "userId": 1,
                "type": "message",
                "message": "Hello test note",
                "dateCreated": "2020-09-14T06:34:55.000Z",
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
            },
            {
                "id": 12,
                "noteId": 8,
                "parentId": null,
                "userId": 1,
                "type": "message",
                "message": "Hello test note",
                "dateCreated": "2020-09-14T06:35:08.000Z",
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
        ]
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

