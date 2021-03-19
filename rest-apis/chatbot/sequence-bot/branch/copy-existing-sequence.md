---
description: API to create copy of the existing sequence
---

# Copy Existing Sequence

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/bot/lead/clone/{id}" path="" %}
{% api-method-summary %}
Copy Existing Sequence
{% endapi-method-summary %}

{% api-method-description %}
API to create copy of the existing sequence
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="number" required=true %}
Sequence id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

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
    "lead": {
      "title": "Sales Sequence 06 : Copy 01",
      "description": "A sequence designed to generate leads.",
      "status": "draft",
      "greeting": "active",
      "askFeedback": "disabled",
      "identifier": "salesSequence",
      "identifierCount": 7,
      "isCloned": "yes",
      "clonedCount": 1,
      "createdBy": 1,
      "updatedBy": 1,
      "dateCreated": "2021-02-24T12:10:32.000Z",
      "dateUpdated": "2021-03-19T04:50:20.166Z",
      "id": 140,
      "isImported": "no"
    }
  }
}

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

