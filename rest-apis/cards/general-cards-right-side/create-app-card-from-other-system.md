---
description: Create a UI component card.
---

# Create app card - from other system

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/ui-component" path="" %}
{% api-method-summary %}
 Create card
{% endapi-method-summary %}

{% api-method-description %}
Create a UI component Custom Card.
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

{% endapi-method-parameter %}

{% api-method-parameter name="config" type="object" required=true %}
The configuration of your card. 
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
                "label": "test stripe",
                "canvas": {
                    "content_url": true
                },
                "action_key": "test-form",
                "action_type": "initialize_tab",
                "iconImageUrl": "./assets/app-store/acquire_saml.svg",
                "initialize_url": "https://9adfb9433cf4.ngrok.io/initialize",
                "submit_url": "https://9adfb9433cf4.ngrok.io/submit",
                "configure_url": "https://9adfb9433cf4.ngrok.io/configure"
            },
            "displayScope": "contact_action",
            "area": "backend",
            "userId": 98,
            "dateCreated": "2021-04-06T10:46:20.418Z",
            "order": 0,
            "id": 574
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
        "label": "test stripe",
        "canvas": {
            "content_url": true
        },
        "action_key": "test-form",
        "action_type": "initialize_tab",
        "iconImageUrl": "./assets/app-store/acquire_saml.svg",
        "initialize_url": "https://9adfb9433cf4.ngrok.io/initialize",
        "submit_url": "https://9adfb9433cf4.ngrok.io/submit",
         "configure_url": "https://9adfb9433cf4.ngrok.io/configure"
    },
    "displayScope": "contact_action",
    "area": "backend"
}
```

