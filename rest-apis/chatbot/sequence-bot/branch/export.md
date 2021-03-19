---
description: API to export the sequence
---

# Export

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/bot/lead/export" path="" %}
{% api-method-summary %}
Export
{% endapi-method-summary %}

{% api-method-description %}
API to export the sequence
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
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
  "data": [
    {
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
      "dateUpdated": "2021-03-19T04:44:45.000Z",
      "leadBranchs": [
        {
          "id": 926,
          "title": "Welcome Branch",
          "visibleOrder": 1,
          "position": {
            "x": 22,
            "y": 30
          },
          "isParent": "yes",
          "leadEdges": [
            {
              "id": 3996,
              "type": "auto_followup",
              "typeVal": null,
              "followupFalsefallback": "Welcome to Acquire! Please let me know what you looking for today?\n",
              "followupFalsefallbackJson": {
                "blocks": [
                  {
                    "key": "bh4it",
                    "data": {},
                    "text": "Welcome to Acquire! Please let me know what you looking for today?",
                    "type": "unstyled",
                    "depth": 0,
                    "entityRanges": [],
                    "inlineStyleRanges": []
                  }
                ],
                "entityMap": {}
              },
              "visibleOrder": 1,
              "leadEdgeActions": [],
              "leadEdgeBubbles": []
            },
            {
              "id": 4002,
              "type": "auto_followup",
              "typeVal": null,
              "followupFalsefallback": "Hello From Bot!\n",
              "followupFalsefallbackJson": {
                "blocks": [
                  {
                    "key": "e4brl",
                    "data": {},
                    "text": "Hello From Bot!",
                    "type": "unstyled",
                    "depth": 0,
                    "entityRanges": [],
                    "inlineStyleRanges": []
                  }
                ],
                "entityMap": {}
              },
              "visibleOrder": 2,
              "leadEdgeActions": [],
              "leadEdgeBubbles": []
            }
          ]
        }
      ]
    }
  ]
}

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Body\(raw\)

```text
{
  "leadIds": [
    138
  ]
}

```

