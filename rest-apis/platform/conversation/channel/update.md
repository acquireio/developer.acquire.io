# Update

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/crm/channel/{channelId}" path="" %}
{% api-method-summary %}
Update a channel
{% endapi-method-summary %}

{% api-method-description %}
Update a channel with the given channel data and return the channel object.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="channelId" type="string" required=true %}
The ID of the channel
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

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
    "id": "ezwlfc5il3",
    "name": "string12",
    "iconType": "internal",
    "icon": "string",
    "messageWebhook": "https://testtest.com",
    "userId": 1,
    "dateCreated": "2021-03-11T07:37:54.000Z",
    "internal": null,
    "status": "active"
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

**Body\(row\)**

```text
{
  "name": "string",
  "iconType": "internal",
  "icon": "string",
  "messageWebhook": "https://test.com",
  "status": "active"
}
```

