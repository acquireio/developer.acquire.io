---
description: >-
  Tags are used to label conversations. Agents may attach tags to cases and
  conversations.
---

# Tags

The tag endpoints allows you to create, update, retrieve, and delete Tags.

### Attributes 

| ATTRIBUTE | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| id | Integer | Specify the ID of the Tag |
| name | String | Specify the name of the Tag. |
| color | String | Specify the color of the Tag |
| userId | Integer | Specify the owner id of the Tag |
| type | String | Specify the type of tag for contact or case |
| user | JSON Array Object \(Entity Relations\) | Specify the owner details |
| dateCreated | datetime | Tag creation timestamp |

### Permissions

To request a tag endpoint, you will need a valid API Key with Tag permissions enabled.

