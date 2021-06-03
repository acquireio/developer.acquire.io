---
description: Capture data when a call ends.
---

# Call end

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/voip/call-answered" path="" %}
{% api-method-summary %}
Create an end call
{% endapi-method-summary %}

{% api-method-description %}
Create an ended call.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="Email" type="string" required=false %}
Email of the callee. Email is optional for the incoming call.
{% endapi-method-parameter %}

{% api-method-parameter name="From" type="string" required=true %}
Phone number of the caller 'From'
{% endapi-method-parameter %}

{% api-method-parameter name="To" type="string" required=true %}
Phone number of the callee 'To'
{% endapi-method-parameter %}

{% api-method-parameter name="CallId" type="string" required=true %}
Specify the Id of the call.
{% endapi-method-parameter %}

{% api-method-parameter name="CallStatus" type="string" required=true %}
Specify the status of the call.   
\['busy',  
'no-answer',  
'canceled',  
'failed',  
'completed'\]
{% endapi-method-parameter %}

{% api-method-parameter name="RecordingUrl" type="string" required=false %}
Specify the URL of the recording.
{% endapi-method-parameter %}

{% api-method-parameter name="Duration" type="string" required=false %}
Specify the call duration \(sec\). 
{% endapi-method-parameter %}

{% api-method-parameter name="Direction" type="string" required=true %}
Specify the direction of the call. 'outgoing/incoming'
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
  "email": "user@example.com",
  "CallStatus": "completed",
  "RecordingUrl": "string",
  "Duration": "10",
  "Direction": "incoming"
}
```

