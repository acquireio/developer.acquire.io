---
description: Perform bulk actions on bots
---

# Bulk Action

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/bot/lead/bulk" path="" %}
{% api-method-summary %}
Bulk Action on bots
{% endapi-method-summary %}

{% api-method-description %}
Perform bulk action on bots. Store the sequence IDs in an array set to `"recordIds"`. Set your desired action to `"actionType"`.   
  
Available actions:   
  
`"delete"` - Deletes the sequences. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="recordIds" type="array" required=true %}
Array of integers. An array of sequence IDs. 
{% endapi-method-parameter %}

{% api-method-parameter name="actionType" type="string" required=true %}
The bulk action you want performed. 
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
    "message": "Sequences deleted successfully.",
    "lessEventsNotice": true
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
  "actionType": "delete",
  "recordIds": [
    137
  ]
}

```

