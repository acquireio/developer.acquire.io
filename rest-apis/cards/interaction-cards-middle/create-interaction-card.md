---
description: Create an Interaction Custom Card.
---

# Create Interaction Card

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/view" path="" %}
{% api-method-summary %}
Create a Card
{% endapi-method-summary %}

{% api-method-description %}
Create an Interaction Custom Card. A contact\_id with the contact's ID and a view object must be passed in to the body. See the body example for more information. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="view" type="object" required=true %}
View object. The card configuration.
{% endapi-method-parameter %}

{% api-method-parameter name="contact\_id" type="integer" required=true %}
Contact ID.
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
            "title": "this is canvas view",
            "contactId": 96,
            "view": {
                "type": "ui_block",
                "config": {
                    "canvas": {
                        "content": {
                            "components": [
                                {
                                    "type": "text",
                                    "text": "hello acquire",
                                    "style": "heading"
                                },
                                {
                                    "type": "input",
                                    "label": "my input box",
                                    "style": "paragraph",
                                    "id": "my_input",
                                    "value": "acquire"
                                }
                            ]
                        }
                    }
                }
            },
            "meta": {
                "iconImageUrl": "https://acquire.io/wp-content/themes/acquire/assets/images/common/acq-footer-black-logo.svg",
                "iconFont": "icon-ticket"
            },
            "userId": 24,
            "dateCreated": "2020-09-16T13:04:38.268Z",
            "id": 10
        },
        "message": "View added successfully."
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
    "title": "Interaction Cards",
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
        "initialize_url": "https://0ff32dabc277.ngrok.io/mix1-initialize"
    }
}
```

