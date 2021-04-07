---
description: >-
  Account User contains the information of the available users in that
  particular account and it's details.
---

# Account - User / Agent

Account User contains the information of the available users in that particular account and it's details. 

### Attributes 

| ATTRIBUTE | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| count | Integer | Represents the number of records exists |
| data | JSON object | Information about the user which contains the details as firstname,lastname,id,type,status,name,email,phone,photo,language |
| roles | JSON Array Object | Specify the User roles which has the properties id,rolename,permissions,permissionType |
| departments | JSON Array Object | Specify the departments to which the User belongs to and the department properties |

### **Permissions**

To request a company endpoint you will need a valid API Key with the company access permissions enabled.

### **Relations between Users and other entities**

A user can be a part of many departments and has multiple roles.

