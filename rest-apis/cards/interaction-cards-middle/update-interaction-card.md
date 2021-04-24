---
description: Update an interaction card.
---

# Update Interaction Card

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/crm/view/{{cardId}}" path="" %}
{% api-method-summary %}
Update card
{% endapi-method-summary %}

{% api-method-description %}
Update an interaction card. The cardId must be passed in to the endpoint as a path parameter. A view object must be passed in to the body. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="cardId" type="integer" required=true %}
ID of the card
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="title" type="string" required=false %}
Title for the card.
{% endapi-method-parameter %}

{% api-method-parameter name="view" type="object" required=true %}
View object. The card configuration.
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
            "id": 17,
            "view": {
                "type": "ui_block",
                "config": {
                    "label": "mix sample",
                    "canvas": {
                        "content_url": true
                    },
                    "action_key": "test-json",
                    "action_type": "initialize_tab",
                    "iconImageUrl": "./assets/app-store/acquire_saml.svg",
                    "initialize_url": "https://0cd3f367b0ac.ngrok.io/mix1-initialize"
                }
            },
            "meta": {
                "iconImageUrl": "https://acquire.io/wp-content/themes/acquire/assets/images/common/acq-footer-black-logo.svg",
                "iconFont": "icon-ticket"
            },
            "title": "Update Interaction Cards",
            "userId": null,
            "dateCreated": null
        },
        "message": "View updated successfully."
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
    "title": "Update Interaction Cards",
    "meta": {
        "iconImageUrl": "https://acquire.io/wp-content/themes/acquire/assets/images/common/acq-footer-black-logo.svg",
        "iconFont": "icon-ticket"
    },
    "contact_id": "96",
    "view": {
        "type": "ui_block",
        "config": {
        "label": "mix sample",
        "canvas": {
            "content_url": true
        },
        "action_key": "test-json",
        "action_type": "initialize_tab",
        "iconImageUrl": "./assets/app-store/acquire_saml.svg",
        "initialize_url": "https://0cd3f367b0ac.ngrok.io/mix1-initialize"
    }
    }
}
```

