---
description: This endpoint allows you to get all the existing articles in Knowledge Base.
---

# Get Articles

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/kb/article?groupdId={{groupId}}" path="" %}
{% api-method-summary %}
Get All Articles
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get all the existing articles in Knowledge Base.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{API\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="groupId" type="integer" required=true %}
The Knowledge Base group ID
{% endapi-method-parameter %}

{% api-method-parameter name="page" type="integer" required=false %}
Limit the number of pages you receive if you are using pagination. 
{% endapi-method-parameter %}

{% api-method-parameter name="limit" type="number" required=false %}
Limit the number of articles you receive.
{% endapi-method-parameter %}

{% api-method-parameter name="search" type="string" required=false %}
Search for article keywords. 
{% endapi-method-parameter %}

{% api-method-parameter name="categoryId" type="integer" required=false %}
Retrieve articles from a category with its  categoryId.  
{% endapi-method-parameter %}

{% api-method-parameter name="ids" type="array" required=false %}
Array of integers. Retrieve articles by their Ids. Example: \[1, 2, 3\]
{% endapi-method-parameter %}

{% api-method-parameter name="author" type="integer" required=false %}
Retrieve articles written by an author with the author's ID. Example: 1
{% endapi-method-parameter %}

{% api-method-parameter name="access" type="string" required=false %}
Indicate article permissions: **\[internal, protected, active\]**
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="string" required=false %}
Indicate draft status: **\[draft, active, archive\]**
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
    "articleCount": 1,
    "limit": 1,
    "page": 1,
    "articles": [
      {
        "id": 1646,
        "title": "new",
        "description": "",
        "articleSlug": "new",
        "featuresImage": null,
        "category": [],
        "author": {
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
        "dateCreated": "2021-03-22T05:54:37.000Z",
        "dateUpdated": "2021-03-22T05:54:37.000Z",
        "botAssigned": "no",
        "autoRelated": "yes",
        "access": "active",
        "status": "archive"
      }
    ]
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

