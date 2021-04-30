---
description: Retrieve a single department
---

# Get

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/account/department/{{departmentId}}" path="" %}
{% api-method-summary %}
Get
{% endapi-method-summary %}

{% api-method-description %}
API to get a single department by it's ID
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="departmentId" type="integer" required=true %}
ID of the department
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {API\_KEY}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="select" type="array" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="relations" type="object" required=false %}

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
    "id": 11,
    "name": "moi",
    "status": "active"
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



