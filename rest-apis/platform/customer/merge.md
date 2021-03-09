# Merge

Using this API you can merge two customers \(contacts\). The contact ID in the endpoint URL **\(primary\_contact\_id\)** is included in the primary and the contact ID **\(secondary\_contact\_ids\)** in the request body will indicate the contact to be merged. Secondary \(selected\) contact information such as conversation, chats, notes, views, etc. will be merged into primary contact.  
**primary\_contact\_id:** will be placed in the path parameter within the endpoint.  
**secordary\_contact\_id:** will be placed in the request body.  


| `NOTE:` | Merged contact cannot be revert. |
| :--- | :--- |


### PARAMETERS

| ATTRIBUTE | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| primary\_contact\_id | Integer | ID of the source contact |
| secondary\_contact\_ids | Array of integers | IDs of the secondary contacts |

