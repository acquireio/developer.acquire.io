---
description: Delete a Knowledge Base.
---

# Delete

{% api-method method="delete" host="https://{{account\_id}}.acquire.io/api/v1/kb/group/delete/{{id}}" path="" %}
{% api-method-summary %}
Delete Knowledge base
{% endapi-method-summary %}

{% api-method-description %}
Delete a Knowledge Base. The id must be passed in to the endpoint as a path parameter. **Warning**: This action cannot be undone. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="KnowledgeBaseId" type="integer" required=true %}
ID of the Knowledge Base group to be deleted
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

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

```javascript
{
  "data": {
    "success": true,
    "message": "Knowledge base successfully deleted.",
    "data": {
      "raw": {
        "fieldCount": 0,
        "affectedRows": 1,
        "insertId": 0,
        "serverStatus": 2,
        "warningCount": 0,
        "message": "",
        "protocol41": true,
        "changedRows": 0,
        "parse": {},
        "write": {}
      },
      "affected": 1
    }
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

