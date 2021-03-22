---
description: API to list out the blocked visitors
---

# List

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/block-visitor" path="" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
API to list out the blocked visitors
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
Bearer {api\_key}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="select" type="array" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="relations" type="object" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="where" type="object" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="order" type="object" required=false %}

{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{"data":[{"data":["198.61.45.122"],"blockTill":"2021-03-24T18:29:59.000Z","type":"ip","blockBy":12,"id":4,"dateCreated":"2021-03-22T04:19:01.000Z","user":{"permissions":["*/*"],"id":12,"type":"user","name":"viswanath","firstName":"viswanath","lastName":"","email":"viswanath.sarma@acquire.io","preference":{"accessLevel":["account"],"cobrowseAccessUrls":[]},"photo":"","language":"","account":{"uid":"35qto1","organization":""},"loginId":295}}]}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

