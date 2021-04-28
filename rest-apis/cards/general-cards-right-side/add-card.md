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
Config object. The configuration of your card.
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

### Attributes 

<table>
  <thead>
    <tr>
      <th style="text-align:left">ATTRIBUTE</th>
      <th style="text-align:left">TYPE</th>
      <th style="text-align:left">DESCRIPTION</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">type</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">Specify the type of card. <b><br />block</b> | <b>action</b> | <b>tab</b> | <b>script_tags</b> | <b>style</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">config</td>
      <td style="text-align:left">JSON object</td>
      <td style="text-align:left">Specify the card configuration. Value for config is a JSON object according
        to type.</td>
    </tr>
    <tr>
      <td style="text-align:left">displayScope</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">
        <p>Specify the card display scope.</p>
        <p><b>home</b>(For frontend widget home app list) |
          <br /><b>contact_action</b> | <b>case_action</b> | <b>message_action</b> |
          <br /><b>picker</b> | <b>main</b> (for other)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">area</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

