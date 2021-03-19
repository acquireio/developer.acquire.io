# Get

{% api-method method="get" host="https://{{account\_uid}}.acquire.io/api/v1" path="/kb/group" %}
{% api-method-summary %}
Get All Knowledge base
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
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "data": {
    "success": true,
    "data": [
      {
        "baseGroupsLang": [
          {
            "id": 31,
            "name": "English",
            "code": "en",
            "isDefault": "no"
          }
        ],
        "createdBy": 1,
        "dateCreated": "2021-03-19T14:01:22.000Z",
        "dateUpdated": "2021-03-19T14:20:19.000Z",
        "id": 27,
        "isDefault": "no",
        "name": "KB2 New",
        "slugKey": "kb2",
        "status": "draft",
        "updatedBy": 1,
        "isSetup": true,
        "customDomain": ""
      },
    ]
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://{{account\_uid}}.acquire.io/api/v1" path="/kb/group/:id" %}
{% api-method-summary %}
Get Single Knowledge base
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
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "data": {
    "success": true,
    "data": [
      {
        "baseGroupsLang": [
          {
            "id": 31,
            "name": "English",
            "code": "en",
            "isDefault": "no"
          }
        ],
        "createdBy": 1,
        "dateCreated": "2021-03-19T14:01:22.000Z",
        "dateUpdated": "2021-03-19T14:20:19.000Z",
        "id": 27,
        "isDefault": "no",
        "name": "KB2 New",
        "slugKey": "kb2",
        "status": "draft",
        "updatedBy": 1,
        "isSetup": true,
        "customDomain": ""
      }
    ]
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

