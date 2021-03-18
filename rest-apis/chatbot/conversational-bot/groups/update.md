---
description: API to update bot group
---

# Update

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/bot/group/{id}" path="" %}
{% api-method-summary %}
Update Group
{% endapi-method-summary %}

{% api-method-description %}
API to update a specific bot group
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="number" required=true %}
GroupID to be updated
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
YOUR API KEY
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
    "message": "Group Updated Successfully."
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Body\(raw\)

```text
{
  "description": "Group Description",
  "title": "Group Title",
  "isDefault": "no",
  "askFeedback": "active"
}
```

