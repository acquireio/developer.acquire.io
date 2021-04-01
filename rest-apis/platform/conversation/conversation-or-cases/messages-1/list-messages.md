# Retrieve a list of messages

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/messenger/chat/messages?contactId={{contactId}}&threadId={{threadId}}" path="" %}
{% api-method-summary %}
Get message List
{% endapi-method-summary %}

{% api-method-description %}
Retrieve a list of messages. The following query parameters must be present: **threadId** and **contactId**.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="-x-user-type" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="threadId" type="integer" required=true %}
ID of the thread.
{% endapi-method-parameter %}

{% api-method-parameter name="contactId" type="integer" required=true %}
ID of the customer/contact.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
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

