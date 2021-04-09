---
description: >-
  A contact is someone who has initiated a conversation through any channel.
  Contacts can also belong to a company.
---

# Contact

The Contact API can be used to create, update, retrieve, and delete records in a Contact object. You can retrieve single contact and a list of all contacts. You can assign **Tags** & create **Custom Attributes** for a contact.

### Attributes 

| ATTRIBUTE | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| id | Integer | Specify the ID of the contact |
| clientType | String | Specify the platform: 'web', 'client',  or 'sdk'. |
| clientName | String | Specify the contact's browser name. |
| clientVersion | String | Specify the browser version. |
| clientOsName | String | Specify the operating system name. |
| clientOsVersion | String | Specify the operating system version. |
| clientDeviceType | String | Specify the device type: desktop, mobile, etc. |
| clientDeviceVendor | String | Specify the device vendor: Apple, Microsoft, etc. |
| clientDeviceModel | String | Specify the device model: iPhone, Android. |
| clientDetails | JSON Object | Specify the user info in details such as engine, CPU, WebKit, etc. |
| archive | String | Specify the visibility of the contact |
| company | JSON Array Object \(Entity Relations\) | Information about contact's company. |
| cases  | JSON Array Object \(Entity Relations\) | Specify the cases |
| tags | JSON Array Object \(Entity Relations\) | Specify the contact tags |
| visits | JSON Array Object \(Entity Relations\) | Specify the contact's visit history |
| timeline | JSON Array Object \(Entity Relations\) | Specify the contact's timeline details |
| fields | JSON object \(Entity Relations\) | Information about contact such as name, email, phone, & custom attributes |
| dateCreated | datetime | Contact creation timestamp |
| dateUpdated | datetime | Contact updated timestamp |

### **Permissions**

To request a contact's endpoint, you will need a valid API key with the contact access permissions.

### **Relations between contact and other entities**

Contacts are associated with a company, case, tags, and timeline.  
  


