---
description: API to get list of all numbers available
---

# Get All Numbers

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/voip/get-all-numbers" path="" %}
{% api-method-summary %}
Get All Numbers
{% endapi-method-summary %}

{% api-method-description %}
API to get list of all numbers available
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
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
    "count": 1,
    "data": [
      {
        "id": 3,
        "name": "+12513188609",
        "number": "+12513188609",
        "type": "Local",
        "location": "AL",
        "sid": "PN204c8c83b85106d0c4fe9b2ed33a5ab7",
        "status": "active",
        "twiml_app": "5mkg3t-app",
        "app_sid": "APc048a0b7bfaccaf44ca25381252ae07a",
        "webhook_url": "https://5mkg3t.uat.env.acquire.io/api/v1/voip/call",
        "meta": {
          "type": "Local",
          "number": "+12513188609",
          "feature": [
            "Call",
            "SMS"
          ],
          "location": "AL",
          "countryCode": "US|usa",
          "countryName": "United States",
          "addressRequirements": "none"
        },
        "config": null,
        "ivr": []
      }
    ],
    "isOtherTwilioAccount": false,
    "twilioAccountStatus": "Full"
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

