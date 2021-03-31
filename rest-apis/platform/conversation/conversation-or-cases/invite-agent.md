# Invite Agent

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/messenger/agent/invite-agent" path="" %}
{% api-method-summary %}
Invite an agent 
{% endapi-method-summary %}

{% api-method-description %}
Invite agents or departments to the chat. The **caseId** must be passed in the body of the request. The agent IDs or department IDs **\(agentId \| department\)** must be passed to the body as a JSON array. You can add as many agents as you'd like and invite a department. Agents or departments will receive an in-app notification, which they can accept to access the conversion.   
  
**agentId** - An agent's ID. To find agent IDs, log in to Acquire and go to `Settings > Users and Roles` or send a GET request to Agent List.  
  
**department -** A department's ID. Send a GET request to Department List to find department IDs.   
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

**Body \(raw\)**

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

