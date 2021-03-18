---
description: API to get the tag by it's ID
---

# Get Single Tag

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/tag/{TAG\_ID}" path="" %}
{% api-method-summary %}
Get single tag
{% endapi-method-summary %}

{% api-method-description %}
API to get a specific tag by its ID
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
ID of the tag for which you need to get details
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
\*\*\*\*\*YOUR API KEY\*\*\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="relations" type="object" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="select" type="array" required=false %}
Specify fields which you want to get in the list
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
    "id": 1,
    "name": "testings",
    "color": "#3F95FD",
    "userId": 12,
    "type": [
      "contact"
    ],
    "dateCreated": "2021-03-17T06:25:56.000Z"
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



