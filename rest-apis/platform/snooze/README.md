---
description: >-
  Snooze allows the agent to remove the conversation from active view for a set
  time.
---

# Snooze

This API allows you to manage snooze for a specific day and time. That conversation will be snooze marked on the specified day and time. 

### Attributes 

| ATTRIBUTE | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| id | Integer | Specify the ID of the Snooze |
| objectType | String | Specify the snooze set for 'contact' or 'case'. |
| contactId | Integer | Specify the Snooze for a contact. |
| scheduleDate | datetime | Specify the timestamp of the Snooze. |
| objectId | Integer | Specify the case or contact id. |
| userId | Integer | Specify the user id. |
| message | String | Specify the snooze message. |
| users | JSON Array Object | Specify the owner of the Snooze. |

### Permissions

To request a snooze endpoint, you will need a valid API Key with the Snooze permissions enabled.

