# Block Contact

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/block-visitor​" path="" %}
{% api-method-summary %}
Block a contact
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "data": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

**Body\(raw\)**

```text
{
    "data": [
        827
    ],
    "type": "contact",
    "blockTill": "2021-09-09T07:08:12.658Z"
}
```

