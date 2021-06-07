---
description: Add a new department
---

# Add

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/account/department" path="" %}
{% api-method-summary %}
Add
{% endapi-method-summary %}

{% api-method-description %}
Add a new department. The following keys must be passed in to the body of the request:   
`department_list` - Array of objects.   
`name` - The department's name. Must be unique.   
`status` - The department's status. Choose `"active"` to publish the department, choose `"disabled"` to set the department to draft. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{API\_KEY}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="status" type="string" required=true %}
Department status: "active" \| "disabled"
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=true %}
The department's name. Must be unique.
{% endapi-method-parameter %}

{% api-method-parameter name="department\_list" type="array" required=true %}
Array of objects. The department list.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "data": [
    {
      "name": "department",
      "status": "active",
      "id": 14
    }
  ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Body\(raw\)

```text
{
  "department_list": [
    {
      "name": "department",
      "status": "active"
    }
  ]
}
```

