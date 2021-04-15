---
description: Add a new Sequence branch
---

# Add

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/bot/lead/branch" path="" %}
{% api-method-summary %}
Add
{% endapi-method-summary %}

{% api-method-description %}
Add a new Sequence branch. The Sequence ID must be passed into the body. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="y" type="string" required=false %}
The location that the branch will be placed on the y-axis
{% endapi-method-parameter %}

{% api-method-parameter name="x" type="string" required=false %}
The location that the branch will be placed on the x-axis
{% endapi-method-parameter %}

{% api-method-parameter name="position" type="object" required=false %}
position object
{% endapi-method-parameter %}

{% api-method-parameter name="title" type="string" required=false %}
The title of the branch
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="integer" required=true %}
The Sequence ID that the branch will be part of
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
    "message": {
      "lead": {
        "id": 138,
        "title": "Sales Sequence 06",
        "description": "A sequence designed to generate leads.",
        "status": "publish",
        "greeting": "active",
        "askFeedback": "disabled",
        "identifier": "salesSequence",
        "identifierCount": 7,
        "isImported": "no",
        "isCloned": "no",
        "clonedCount": 0,
        "createdBy": 1,
        "updatedBy": 1,
        "dateCreated": "2021-02-24T12:10:32.000Z",
        "dateUpdated": "2021-03-01T08:55:10.000Z"
      },
      "title": "New Branch",
      "visibleOrder": 8,
      "position": {
        "x": "22",
        "y": "30"
      },
      "id": 928,
      "isParent": "no"
    }
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
  "id": 138,
  "title": "New Branch",
  "position": {
    "x": "22",
    "y": "30"
  }
}

```



