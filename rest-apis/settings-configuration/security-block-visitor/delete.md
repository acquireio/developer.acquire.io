---
description: API to delete the block visitor contact
---

# Delete

{% api-method method="delete" host="https://{{account\_id}}.acquire.io/api/v1/crm/block-visitor?contactId=111&id=111" path="" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
API to delete the block visitor contact
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="contactid" type="array" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="id" type="array" required=false %}

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

