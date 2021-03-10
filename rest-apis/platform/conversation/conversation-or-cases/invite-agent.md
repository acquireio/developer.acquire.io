# Invite Agent

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/messenger/agent/invite-agent" path="" %}
{% api-method-summary %}
Invite an agent 
{% endapi-method-summary %}

{% api-method-description %}
This API will help to invite a new agent to the chat. You can add one or more agents, plus you can invite a department to this chat. Agents or departments will receive an invitation notification, which they can accept for access conversion. The agent or department IDs **\(department \| agentIds\)** must be passed to the json-array.  
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
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
    "1": {
      "userId": 1,
      "online": true,
      "sent": true
    },
    "11": {
      "userId": 11,
      "online": false,
      "sent": false
    },
    "26": {
      "userId": 26,
      "online": false,
      "sent": false
    }
  
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

**Body\(row\)**

```text
{
    "caseId": 22,
    "department": [
    2,
    3,
    4
  ],
    "agentIds": [
        1,
        11,
        26
    ]
}
```

