---
description: Access your cobrowse analytics.
---

# Cobrowse

{% api-method method="get" host="https://app.acquire.io/api/analytics/general/raw-co-browse" path="" %}
{% api-method-summary %}
Get Cobrowse Data
{% endapi-method-summary %}

{% api-method-description %}
Access your cobrowse analytics. Only a month's worth of data may be accessed at a time.  
  
The body parameters should be in x-www-form-urlencoded format in key-value pairs.  
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Bearer Token" type="string" required=true %}
Your API Key
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="end\_date" type="string" required=true %}
End date in YYYY-MM-DD HH:MM:SS \(e.x. 2021-06-01 23:59:59\)
{% endapi-method-parameter %}

{% api-method-parameter name="start\_date" type="string" required=true %}
Start date in YYYY-MM-DD HH:MM:SS format \(e.x. 2021-05-01 00:00:00\)
{% endapi-method-parameter %}

{% api-method-parameter name="timezone" type="string" required=true %}
Your timezone
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
The response body shows the success status, error messages, and data array. 
{% endapi-method-response-example-description %}

```
{
    "success": true,
    "error": null,
    "data": [
        {
            "chat_id": 17200436,
            "date_created": "2021-05-06 11:46:24",
            "agent_id": 1,
            "agent_name": "Acquire",
            "total_time": "01 hours 01 minutes 45 seconds ",
            "page_visited": "https://sample.acquire.io"
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

