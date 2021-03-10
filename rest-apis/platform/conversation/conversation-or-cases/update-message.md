# Update Message

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/messenger/chat/message/{messageId}" path="" %}
{% api-method-summary %}
Update a message
{% endapi-method-summary %}

{% api-method-description %}
Using this API you can modify the current message in a Conversation. The messageId in the path parameter is required to update the message.  
  
`messageId-` Message-ID, it can be found in the webhook endpoint URL.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="messageId" type="string" required=false %}
The Id of a message
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

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



