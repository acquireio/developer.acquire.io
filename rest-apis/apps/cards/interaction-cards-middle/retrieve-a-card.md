# Retrieve a card

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/view/{cardId}" path="" %}
{% api-method-summary %}
Get single card
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="cardId" type="string" required=true %}
Id of the card.
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
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

