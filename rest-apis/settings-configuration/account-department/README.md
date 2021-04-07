---
description: >-
  Department endpoint enable us to get the department related information and
  make some updates to the account departments.
---

# Account - Department

Department endpoint enable us to get the department related information and make some updates to the account departments.

### Attributes 

| ATTRIBUTE | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| count | Integer | Represents the number of records exists |
| data | JSON object | Information about the department which contains the details as id,name,status and users. |
| users | JSON Array Object | Specify the User details which includes firstname,lastname,id,type,status,name,email,phone,photo,language |

### **Permissions**

To request a department endpoint you will need a valid API Key with the department access permissions enabled.

### **Relations between Department and other entities**

A department may have many users.

