---
description: Retrieve details for a specific sequence
---

# Get Single Sequence

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/bot/lead/{{id}}" path="" %}
{% api-method-summary %}
Get Single Sequence
{% endapi-method-summary %}

{% api-method-description %}
Retrieve details for a specific sequence. The sequence id must be passed in to the endpoint as a path parameter.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
Specify sequence ID
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
      "id": 137,
      "title": "Sales Sequence 05",
      "description": "A sequence designed to generate leads.",
      "status": "publish",
      "greeting": "active",
      "askFeedback": "disabled",
      "identifier": "salesSequence",
      "identifierCount": 6,
      "isImported": "no",
      "isCloned": "no",
      "clonedCount": 0,
      "createdBy": 1,
      "updatedBy": 1,
      "dateCreated": "2020-12-15T08:36:02.000Z",
      "dateUpdated": "2021-02-24T06:18:39.000Z",
      "leadBranchs": [
        {
          "id": 919,
          "title": "Welcome",
          "visibleOrder": 1,
          "position": {
            "x": 405,
            "y": 22
          },
          "isParent": "yes",
          "leadEdges": [
            {
              "id": 3968,
              "type": "auto_followup",
              "typeVal": null,
              "followupFalsefallback": "Welcome! Please let me know what you looking for?",
              "followupFalsefallbackJson": null,
              "visibleOrder": 1,
              "leadEdgeActions": [],
              "leadEdgeBubbles": []
            },
            {
              "id": 3969,
              "type": "bubble",
              "typeVal": null,
              "followupFalsefallback": null,
              "followupFalsefallbackJson": null,
              "visibleOrder": 2,
              "leadEdgeActions": [],
              "leadEdgeBubbles": [
                {
                  "id": 782,
                  "label": "Sales",
                  "nextBranchId": 918,
                  "wantToSave": "no",
                  "savedFieldKey": null
                },
                {
                  "id": 783,
                  "label": "Support",
                  "nextBranchId": 917,
                  "wantToSave": "no",
                  "savedFieldKey": null
                },
                {
                  "id": 784,
                  "label": "Just browsing",
                  "nextBranchId": 916,
                  "wantToSave": "no",
                  "savedFieldKey": null
                }
              ],
              "wantToSave": "no",
              "savedFieldKey": null
            }
          ]
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



