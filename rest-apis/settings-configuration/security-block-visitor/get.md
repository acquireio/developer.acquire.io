---
description: API to get the blocked visitor by id
---

# Get

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/block-visitor/1" path="" %}
{% api-method-summary %}
Get
{% endapi-method-summary %}

{% api-method-description %}
API to get the blocked visitor by id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
ID of the blocked visitor
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {api\_key}
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
    "id": 1,
    "data": {
      "id": 597304,
      "ip": "2402:8100:21fa:4213:bd98:f32c:7d38:872d",
      "email": "",
      "phone": ""
    },
    "dateCreated": "2021-02-04T20:00:46.000Z",
    "blockTill": "2022-02-04T23:59:59.000Z",
    "blockBy": 1,
    "type": "contact"
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

