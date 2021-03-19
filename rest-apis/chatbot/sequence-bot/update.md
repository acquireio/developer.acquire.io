---
description: API to update specific sequence by it's ID
---

# Update

{% api-method method="put" host="https://{{account\_id}}.acquire.io/api/v1/bot/lead/{id}" path="" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
API to update specific sequence by it's ID
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="number" required=true %}
Specify ID of the sequence to be updated
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
API KEY
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
    "id": 139,
    "title": "Blank Lead",
    "description": "Description Changed",
    "status": "draft",
    "greeting": "active",
    "askFeedback": "disabled",
    "identifier": "blankSequence",
    "identifierCount": 1,
    "isImported": "no",
    "isCloned": "no",
    "clonedCount": 0,
    "createdBy": 1,
    "updatedBy": 1,
    "dateCreated": "2021-03-19T04:01:38.000Z",
    "dateUpdated": "2021-03-19T04:03:47.648Z"
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
  "title": "Blank Lead",
  "description": "Description Changed",
  "status": "draft",
  "greeting": "active",
  "askFeedback": "disabled"
}

```

