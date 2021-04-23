---
description: Create a general card.
---

# Create general card

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/ui-component" path="" %}
{% api-method-summary %}
Create general card
{% endapi-method-summary %}

{% api-method-description %}
Create a general Custom Card.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="type" type="string" required=true %}
"tab"
{% endapi-method-parameter %}

{% api-method-parameter name="config" type="object" required=true %}
Config objet. The configuration of your card.
{% endapi-method-parameter %}

{% api-method-parameter name="displayScope" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="area" type="string" required=true %}

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
        "data": {
            "type": "tab",
            "config": {
                "label": "mix sample",
                "canvas": {
                    "content_url": true
                },
                "action_key": "test-json",
                "action_type": "initialize_tab",
                "iconImageUrl": "./assets/app-store/acquire_saml.svg",
                "initialize_url": "https://0ff32dabc277.ngrok.io/mix2-initialize"
            },
            "displayScope": "contact_action",
            "area": "backend",
            "userId": 98,
            "dateCreated": "2021-04-06T10:41:08.898Z",
            "order": 0,
            "id": 573
        },
        "message": "UI component created successfully."
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
    "type": "tab",
    "config": {
        "label": "mix sample",
        "canvas": {
            "content_url": true
        },
        "action_key": "test-json",
        "action_type": "initialize_tab",
        "iconImageUrl": "./assets/app-store/acquire_saml.svg",
        "initialize_url": "https://0ff32dabc277.ngrok.io/mix2-initialize"
    },
    "displayScope": "contact_action",
    "area": "backend"
}
```

