# Reopen Case

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/messenger/chat/reopen" path="" %}
{% api-method-summary %}
Reopen a case
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

**Body \(raw\)**

```text
{
  "user_id": 1,
  "description": "You can add description for open this chat",
  "id": 28
}
```

