# Get Articles

{% api-method method="get" host="https://{{account\_uid}}.acquire.io/api/v1" path="/kb/article" %}
{% api-method-summary %}
Get All Articles
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{API\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="groupId" type="number" required=true %}
1
{% endapi-method-parameter %}

{% api-method-parameter name="page" type="number" required=false %}
1
{% endapi-method-parameter %}

{% api-method-parameter name="limit" type="number" required=false %}
50
{% endapi-method-parameter %}

{% api-method-parameter name="search" type="string" required=false %}
Hello
{% endapi-method-parameter %}

{% api-method-parameter name="categoryId" type="number" required=false %}
1
{% endapi-method-parameter %}

{% api-method-parameter name="ids" type="array" required=false %}
\[1, 2, 3\]
{% endapi-method-parameter %}

{% api-method-parameter name="author" type="number" required=false %}
1
{% endapi-method-parameter %}

{% api-method-parameter name="access" type="string" required=false %}
internal **\[internal, protected, active\]**
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="string" required=false %}
draft **\[draft, active, archive\]**
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

{% api-method method="get" host="https://{{account\_uid}}.acquire.io/api/v1" path="/kb/article/:groupId/:id" %}
{% api-method-summary %}
Get Single Article
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="groupId" type="number" required=true %}
1
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="number" required=true %}
1
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "data": {
    "success": true,
    "articles": {
      "id": 1646,
      "groupId": {
        "id": 16
      },
      "title": "new",
      "description": "",
      "content": "",
      "jsonContent": {},
      "articleSlug": "new",
      "featuresImage": null,
      "category": [],
      "relatedArticles": [],
      "departments": [],
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
      "autoRelated": "yes",
      "botAssigned": "no",
      "access": "active",
      "status": "archive",
      "seo": {
        "title": "",
        "description": ""
      },
      "tags": []
    }
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

