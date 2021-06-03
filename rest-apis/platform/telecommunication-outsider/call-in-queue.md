---
description: This endpoint allows you to capture data while call in a queue.
---

# Call in queue

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/voip/call-in-queue" path="" %}
{% api-method-summary %}
Create a call in queue
{% endapi-method-summary %}

{% api-method-description %}
Create a call in queue.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="CallId" type="string" required=true %}
Id of the call
{% endapi-method-parameter %}

{% api-method-parameter name="To" type="string" required=true %}
Callee phone number 'To'
{% endapi-method-parameter %}

{% api-method-parameter name="From" type="string" required=true %}
Caller phone number 'From'
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

## Body\(raw\)

```text
{
  "From": "+1234567890",
  "To": "+1789451230",
  "CallId": "CA12345678904567890"
}
```

