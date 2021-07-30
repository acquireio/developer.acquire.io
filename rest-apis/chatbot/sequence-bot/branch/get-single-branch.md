---
description: Retrieve the details of a branch sequence.
---

# Get Single Branch

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/bot/lead/branch/{{id}}" path="" %}
{% api-method-summary %}
Get Single Branch
{% endapi-method-summary %}

{% api-method-description %}
Retrieve the details of a single branch. The bran
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
 The branch Id
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
    "branch": {
      "id": 926,
      "title": "Demo Branch",
      "visibleOrder": 8,
      "position": {
        "x": 22,
        "y": 30
      },
      "isParent": "no",
      "leadEdges": [
        {
          "id": 1628,
          "type": "auto_followup",
          "typeVal": null,
          "followupFalsefallback": "Hello from Bot!",
          "followupFalsefallbackJson": null,
          "visibleOrder": 0,
          "leadEdgeActions": [],
          "leadEdgeBubbles": []
        }
      ]
    }
  }
}

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}
