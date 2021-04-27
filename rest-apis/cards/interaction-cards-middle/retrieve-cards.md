---
description: Retrieve a list of all custom cards.
---

# List all Cards

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/view" path="" %}
{% api-method-summary %}
Get cards
{% endapi-method-summary %}

{% api-method-description %}
Retrieve a list of all custom cards. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="page" type="integer" required=false %}
Specify the page number e.g. 2 to return.
{% endapi-method-parameter %}

{% api-method-parameter name="limit" type="integer" required=false %}
The number of results e.g. 20 to return
{% endapi-method-parameter %}

{% api-method-parameter name="contact\_id" type="integer" required=true %}
Id of the contact.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "data": {
        "offset": 0,
        "count": 7,
        "data": [
            {
                "id": 18,
                "title": "Interaction Cards",
                "contactId": 96,
                "userId": 24,
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
                },
                "meta": {
                    "iconFont": "icon-ticket",
                    "iconImageUrl": "https://acquire.io/wp-content/themes/acquire/assets/images/common/acq-footer-black-logo.svg"
                },
                "dateCreated": "2020-10-16T06:50:04.000Z"
            },
            {
                "id": 17,
                "title": "Update Interaction Cards",
                "contactId": 96,
                "userId": 24,
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
                    "iconFont": "icon-ticket",
                    "iconImageUrl": "https://acquire.io/wp-content/themes/acquire/assets/images/common/acq-footer-black-logo.svg"
                },
                "dateCreated": "2020-10-14T11:57:20.000Z"
            },
            {
                "id": 16,
                "title": "Custom View added",
                "contactId": 96,
                "userId": 24,
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
                        "initialize_url": "https://0cd3f367b0ac.ngrok.io/mix2-initialize"
                    }
                },
                "meta": {
                    "iconFont": "icon-ticket",
                    "iconImageUrl": "https://acquire.io/wp-content/themes/acquire/assets/images/common/acq-footer-black-logo.svg"
                },
                "dateCreated": "2020-10-14T11:36:36.000Z"
            },
            {
                "id": 15,
                "title": "this is new view",
                "contactId": 96,
                "userId": 24,
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
                        "initialize_url": "https://226069089919.ngrok.io/mix2-initialize"
                    }
                },
                "meta": {
                    "iconFont": "icon-ticket",
                    "iconImageUrl": "https://acquire.io/wp-content/themes/acquire/assets/images/common/acq-footer-black-logo.svg"
                },
                "dateCreated": "2020-10-14T11:35:10.000Z"
            },
            {
                "id": 13,
                "title": "this is new view",
                "contactId": 96,
                "userId": 24,
                "view": {
                    "type": "ui_block",
                    "config": {
                        "canvas": {
                            "content": {
                                "components": [
                                    {
                                        "text": "hello acquire",
                                        "type": "text",
                                        "style": "heading"
                                    },
                                    {
                                        "id": "my_input",
                                        "type": "input",
                                        "label": "my input box",
                                        "style": "paragraph",
                                        "value": "acquire"
                                    }
                                ]
                            }
                        }
                    }
                },
                "meta": {
                    "iconFont": "icon-ticket",
                    "iconImageUrl": "https://acquire.io/wp-content/themes/acquire/assets/images/common/acq-footer-black-logo.svg"
                },
                "dateCreated": "2020-09-17T05:28:44.000Z"
            },
            {
                "id": 12,
                "title": "this is canvas view",
                "contactId": 96,
                "userId": 24,
                "view": {
                    "type": "ui_block",
                    "config": {
                        "canvas": {
                            "content": {
                                "components": [
                                    {
                                        "text": "hello acquire",
                                        "type": "text",
                                        "style": "heading"
                                    },
                                    {
                                        "id": "my_input",
                                        "type": "input",
                                        "label": "my input box",
                                        "style": "paragraph",
                                        "value": "acquire"
                                    }
                                ]
                            }
                        }
                    }
                },
                "meta": {
                    "iconFont": "icon-ticket",
                    "iconImageUrl": "https://acquire.io/wp-content/themes/acquire/assets/images/common/acq-footer-black-logo.svg"
                },
                "dateCreated": "2020-09-17T05:09:42.000Z"
            },
            {
                "id": 11,
                "title": "thiTest view updated",
                "contactId": 96,
                "userId": 1,
                "view": {
                    "type": "ui_block",
                    "config": {
                        "canvas": {
                            "content": {
                                "components": [
                                    {
                                        "text": "hello acquire",
                                        "type": "text",
                                        "style": "heading"
                                    },
                                    {
                                        "id": "my_input",
                                        "type": "input",
                                        "label": "my input",
                                        "style": "paragraph",
                                        "value": "acquire"
                                    }
                                ]
                            }
                        }
                    }
                },
                "meta": {
                    "iconFont": "icon-ticket",
                    "iconImageUrl": "https://acquire.io/wp-content/themes/acquire/assets/images/common/acq-footer-black-logo.svg"
                },
                "dateCreated": "2020-09-17T05:05:35.000Z"
            }
        ]
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

