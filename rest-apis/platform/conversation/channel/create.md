# Create

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/channel" path="" %}
{% api-method-summary %}
Create a channel
{% endapi-method-summary %}

{% api-method-description %}
Create a channel with the given channel data and returns a channel object.
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
  "data": {
    "name": "string",
    "iconType": "internal",
    "icon": "string",
    "messageWebhook": "https://test.com",
    "status": "active",
    "userId": 1,
    "id": "ezwlfc5il3",
    "dateCreated": "2021-03-11T07:37:54.000Z",
    "internal": null
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

**Body \(raw\)**

```text
{
  "name": "string",
  "iconType": "internal",
  "icon": "string",
  "messageWebhook": "https://test.com",
  "status": "active"
}
```

