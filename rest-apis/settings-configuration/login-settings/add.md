---
description: API to add a new setting
---

# Add

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/account/account-setting" path="" %}
{% api-method-summary %}
Add
{% endapi-method-summary %}

{% api-method-description %}
API to add a new setting
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {api\_key}
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{"data":
{
    "crm.special_holidays":[
        {
            "id":233,
            "holiday_name":"Holi",
            "date":"Monday 29 Mar 2021",
            "start_hour":"0",
            "start_time":"00:00",
            "end_hour":"24",
            "end_time":"24:00",
            "time":"full"
        }
    ]
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
  "module": "crm",
  "settings": {
    "special_holidays":[
      {
        "date": "Monday 29 Mar 2021"
        "end_hour": "24"
        "end_time": "24:00"
        "holiday_name": "Holi"
        "start_hour": "0"
        "start_time": "00:00"
        "time": "full"
      }
    ]
  }
}
```

