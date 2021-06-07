---
description: Any interaction with a contact creates a case in Acquire.
---

# Cases

The Case or Thread API can be used to send, retrieve, update, and delete messages \(Chat, Email, VOIP\) from a conversation.

### Attributes 

| ATTRIBUTE | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| id | Integer | Specify the ID of the case. |
| title | String | Specify the case title. |
| description | String | Specify the case description. |
| channel | String | Specify the case channel. |
| status | String | Specify the case status such as active, close, etc. |
| threadId | Integer | Specify the case threading id or parent id. |
| closingState | String | Specify the operating system version. |
| dateQueue | datetime | Specify the case queue date. |
| datePending | datetime | Specify the case pending date. |
| dateActive | datetime | Specify the case active date. |
| dateClosed | datetime | Specify the case close date. |
| userId | Integer | Specify the third-party initiated app id of the case. |
| waitTime | String | Specify the case wait time. |
| contact | JSON Array Object \(Entity Relations\) | Specify the case contact. |
| feedbacks | JSON Array Object \(Entity Relations\) | Specify the case feedbacks. |
| messages | JSON Array Object \(Entity Relations\) | Specify the case messages. |
| users | JSON Array Object \(Entity Relations\) | Specify the case users. |
| timeline | JSON Array Object \(Entity Relations\) | Specify the contact's time details |
| fields | JSON object \(Entity Relations\) | Information about case fields. |
| dateCreated | datetime | Case creation timestamp |
| dateUpdated | datetime | Case updated timestamp |

### **Permissions**

To request a case endpoint, you will need a valid API key with case access permissions.

### **Relations between case and other entities**

Cases are associated with message, contact, feedbacks, and timeline. 

