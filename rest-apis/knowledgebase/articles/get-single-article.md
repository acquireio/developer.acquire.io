---
description: API to get a single article by the article id
---

# Get Single Article

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/kb/article/single/1/86" path="" %}
{% api-method-summary %}
Get Single Article
{% endapi-method-summary %}

{% api-method-description %}
API to get a single article by the article id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="groupId" type="number" required=true %}
Specify the group id of the article
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="number" required=true %}
Specify the id of the article
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
            "id": 86,
            "groupId": {
                "id": 1
            },
            "title": "Updating the title of the articles",
            "description": "",
            "content": "<br/>\n",
            "jsonContent": {
                "blocks": [
                    {
                        "key": "8j0nq",
                        "text": "",
                        "type": "unstyled",
                        "depth": 0,
                        "inlineStyleRanges": [],
                        "entityRanges": [],
                        "data": {}
                    }
                ],
                "entityMap": {}
            },
            "articleSlug": "string",
            "featuresImage": null,
            "category": [],
            "relatedArticles": [
                {
                    "id": 2,
                    "title": "Test",
                    "articleSlug": "test"
                }
            ],
            "departments": [],
            "author": 0,
            "updatedBy": {
                "users": {
                    "28": {
                        "departments": [],
                        "roles": [
                            {
                                "id": 1,
                                "roleName": "Administrator"
                            }
                        ],
                        "id": 28,
                        "name": "myuser",
                        "firstName": "myuser",
                        "lastName": "",
                        "photo": "",
                        "email": "myuser@acquire.io",
                        "type": "user",
                        "accessLevel": null
                    }
                }
            },
            "createdBy": 0,
            "dateCreated": "2021-04-06T10:19:35.000Z",
            "dateUpdated": "2021-04-06T10:32:28.000Z",
            "autoRelated": "no",
            "botAssigned": "no",
            "access": "internal",
            "status": "draft",
            "seo": {
                "title": "string",
                "description": "string"
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

