---
description: API to reject case
---

# Case Reject

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/messenger/chat/reject" path="" %}
{% api-method-summary %}
Reject a case
{% endapi-method-summary %}

{% api-method-description %}
API to reject case
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
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
    "dateCreated": "2021-03-24T10:31:24.000Z",
    "dateUpdated": "2021-03-24T10:31:24.000Z",
    "id": 1681,
    "contactId": 597752,
    "closedBy": null,
    "visitId": 1368,
    "title": "#597752 has just started a chat",
    "description": "You're being transferred to one of our agents, they'll be with you shortly.|translate",
    "channel": "chat",
    "status": "pending",
    "closingState": "handled",
    "dateQueue": "2021-03-24T10:31:24.000Z",
    "datePending": "2021-03-24T10:31:24.000Z",
    "dateActive": null,
    "dateClosed": null,
    "queueId": 15,
    "queueOrder": 0,
    "meta": {
      "sessionId": "4645852264",
      "queueRecheck": "no"
    },
    "parentId": null,
    "userId": null,
    "waitTime": 0,
    "threadId": 1681,
    "users": [
      {
        "id": 3832,
        "caseId": 1681,
        "type": "user",
        "userId": 1,
        "role": "owner",
        "status": "rejected",
        "dateCreated": "2021-03-24T10:31:24.000Z",
        "dateLastAssigned": "2021-03-24T10:31:24.000Z",
        "closed": "no",
        "meta": null
      },
      {
        "id": 3831,
        "caseId": 1681,
        "type": "contact",
        "userId": 597752,
        "role": "owner",
        "status": "active",
        "dateCreated": "2021-03-24T10:31:24.000Z",
        "dateLastAssigned": "2021-03-24T10:31:24.000Z",
        "closed": "no",
        "meta": null
      }
    ]
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
  "caseId": 1681
}
```

