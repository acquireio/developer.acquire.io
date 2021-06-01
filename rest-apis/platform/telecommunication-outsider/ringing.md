# Ringing

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/voip/call-ringing" path="" %}
{% api-method-summary %}
Create a call ringing
{% endapi-method-summary %}

{% api-method-description %}
Create a call ringing
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="email" type="string" required=false %}
Email of the callee. 
{% endapi-method-parameter %}

{% api-method-parameter name="Direction" type="string" required=true %}
The direction of the caller 'outgoing/incoming'
{% endapi-method-parameter %}

{% api-method-parameter name="CallId" type="string" required=true %}
Id of the caller
{% endapi-method-parameter %}

{% api-method-parameter name="To" type="string" required=true %}
Phone number of the caller 'To'
{% endapi-method-parameter %}

{% api-method-parameter name="From" type="string" required=true %}
Phone number of the caller 'From'
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "data": {
    "success": true,
    "message": "Successfully saved"
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
  "From": "+1234567890",
  "To": "+1789451230",
  "CallId": "CA12345678904567890",
  "Direction": "incoming",
  "email": "user@example.com"
}
```

