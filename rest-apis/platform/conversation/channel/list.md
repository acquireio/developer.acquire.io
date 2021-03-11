# List

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/channel?limit=20&select=id&select=name&select=iconType&select=icon&select=messageWebhook&select=userId&select=dateCreated&select=internal&select=status" path="" %}
{% api-method-summary %}
List all channels
{% endapi-method-summary %}

{% api-method-description %}
It returns a list of the channels
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="limit" type="string" required=false %}
The maximum number of results to display per page.
{% endapi-method-parameter %}

{% api-method-parameter name="select" type="string" required=false %}
id\|name\|iconType\|icon\|messageWebhook\|  
userId\|dateCreated\|internal\|status
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
    "page": 0,
    "offset": 0,
    "limit": 20,
    "count": 7,
    "data": [
      {
        "id": "audio-call",
        "name": "Audio Call",
        "iconType": "internal",
        "icon": "audio-call",
        "messageWebhook": null,
        "userId": 1,
        "dateCreated": "2020-11-06T19:14:15.000Z",
        "internal": "yes",
        "status": "active"
      },
      {
        "id": "chat",
        "name": "Chat",
        "iconType": "internal",
        "icon": "conversation-sms",
        "messageWebhook": null,
        "userId": 1,
        "dateCreated": "2020-10-10T21:03:17.000Z",
        "internal": "yes",
        "status": "active"
      },
      {
        "id": "mail",
        "name": "Mail",
        "iconType": "internal",
        "icon": "email",
        "messageWebhook": null,
        "userId": 1,
        "dateCreated": "2020-10-10T19:14:15.000Z",
        "internal": "yes",
        "status": "active"
      },
      {
        "id": "private-form",
        "name": "Private Form",
        "iconType": "internal",
        "icon": "chat-queue2",
        "messageWebhook": null,
        "userId": 1,
        "dateCreated": "2020-11-06T19:14:15.000Z",
        "internal": "yes",
        "status": "active"
      },
      {
        "id": "sms",
        "name": "SMS",
        "iconType": "internal",
        "icon": "sms",
        "messageWebhook": null,
        "userId": 1,
        "dateCreated": "2020-11-17T19:14:15.000Z",
        "internal": "yes",
        "status": "active"
      },
      {
        "id": "video-call",
        "name": "Video Call",
        "iconType": "internal",
        "icon": "video-call",
        "messageWebhook": null,
        "userId": 1,
        "dateCreated": "2020-11-06T19:14:15.000Z",
        "internal": "yes",
        "status": "active"
      },
      {
        "id": "voip",
        "name": "Voip",
        "iconType": "internal",
        "icon": "audio-call",
        "messageWebhook": null,
        "userId": 1,
        "dateCreated": "2020-10-10T21:03:20.000Z",
        "internal": "yes",
        "status": "active"
      }
    ]
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

