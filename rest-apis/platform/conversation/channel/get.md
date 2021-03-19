# Get

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/channel/{channelId}" path="" %}
{% api-method-summary %}
Get a Channel
{% endapi-method-summary %}

{% api-method-description %}
Read channels object recognized with channelId
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="channelId" type="string" required=true %}
 'chat' ID of the channel
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

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

