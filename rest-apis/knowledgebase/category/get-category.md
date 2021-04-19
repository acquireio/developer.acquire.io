# Get Category

{% api-method method="get" host="https://{{account\_uid}}.acquire.io/api/v1/kb/category" path="" %}
{% api-method-summary %}
Get All Categories
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{API\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="page" type="number" required=false %}
1
{% endapi-method-parameter %}

{% api-method-parameter name="limit" type="number" required=false %}
50
{% endapi-method-parameter %}

{% api-method-parameter name="search" type="string" required=false %}
Hello
{% endapi-method-parameter %}

{% api-method-parameter name="groupId" type="number" required=true %}
1
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="string" %}
active **\[active, draft\]**
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
  "data": {
    "categoryCount": 1,
    "limit": 50,
    "page": 1,
    "category": [
      {
        "id": 69,
        "parentCategory": null,
        "slug": "new-data",
        "name": "new data",
        "description": "new",
        "createdBy": {
          "users": {
            "1": {
              "departments": [],
              "roles": [
                {
                  "id": 1,
                  "roleName": "Administrator"
                }
              ],
              "id": 1,
              "name": "gdfgfd",
              "firstName": "gdfgfd",
              "lastName": "",
              "photo": "https://local-dev-drive.acquire.io/vrsx1t/media/2020/12/profile-9f6d2ac37a873b12756e057c.jpeg",
              "email": "new@acquire.io",
              "type": "user",
              "accessLevel": null
            }
          }
        },
        "updatedBy": {
          "users": {
            "1": {
              "departments": [],
              "roles": [
                {
                  "id": 1,
                  "roleName": "Administrator"
                }
              ],
              "id": 1,
              "name": "gdfgfd",
              "firstName": "gdfgfd",
              "lastName": "",
              "photo": "https://local-dev-drive.acquire.io/vrsx1t/media/2020/12/profile-9f6d2ac37a873b12756e057c.jpeg",
              "email": "new@acquire.io",
              "type": "user",
              "accessLevel": null
            }
          }
        },
        "dateCreated": "2021-03-22T07:01:30.000Z",
        "dateUpdated": "2021-03-22T07:01:30.000Z",
        "visibleOrder": 0,
        "status": "draft",
        "categoryIcon": "",
        "articleCount": 0,
        "internal": 0,
        "publish": 0,
        "archive": 0
      }
    ]
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



