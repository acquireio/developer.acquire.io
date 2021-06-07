---
description: >-
  Block Visitor contains a particular contact gets blocked until a certain
  period of time or for some reason.
---

# Block Visitor

Block Visitor contains a particular contact gets blocked until a certain period of time or for some reason.

### Attributes 

| ATTRIBUTE | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| count | Integer | Represents the number of records exists |
| data | JSON object | Information which contains the blocked contact details such as id,dataCreated,blockTill, blockedBy and the user blocked details. |
| users | JSON Array Object | Specify the User details which includes firstname,lastname,id,type,status,name,email,phone,photo,language |

## **Permissions**

To request a block visitor endpoint you will need a valid API Key with the block contacts access permissions enabled.

