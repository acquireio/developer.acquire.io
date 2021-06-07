---
description: Retrieve and manipulate information for departments.
---

# Departments

Department endpoints allow you to get department related information and make updates to departments.

### Attributes 

| ATTRIBUTE | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| count | Integer | Represents the number of records that exist |
| data | JSON object | Information about the department such as id, name, status and users |
| users | JSON Array Object | Specify user details such as firstname, lastname, id, type, status, name, email, phone, photo, language |

### **Permissions**

To request a department endpoint, you will need a valid API Key with the department access permissions enabled.

### **Relations between Department and other entities**

A department may have many users.

