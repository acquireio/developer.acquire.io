---
description: Unblock a visitor
---

# Delete

{% api-method method="delete" host="https://{{account\_id}}.acquire.io/api/v1/crm/block-visitor?id={{id}}" path="" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
Unblock a visitor \(remove a visitor from the block list\). The id must be passed in to the endpoint as a path parameter. To find the id, send a Get request to the Block Visitor List endpoint. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{API\_KEY}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
Visitor's block ID.
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
    "deleted": {
      "raw": {
        "fieldCount": 0,
        "affectedRows": 0,
        "insertId": 0,
        "serverStatus": 2,
        "warningCount": 0,
        "message": "",
        "protocol41": true,
        "changedRows": 0,
        "parse": {},
        "write": {}
      },
      "affected": 0
    }
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



