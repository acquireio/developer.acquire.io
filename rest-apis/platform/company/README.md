---
description: >-
  A company is an organization that a contact belongs to. Contacts from the same
  organization should be grouped in a company.
---

# Company

The Company API can be used to create, update, retrieve, and delete records in a company object. The **relations** parameter with a value **contacts** is required to obtain a company's contacts \(i.e., employees\).

### Attributes 

| ATTRIBUTE | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| id | Integer | ID of the company |
| fields | JSON object \(Entity Relations\) | Information about company such as company name, website, industry, description, source, revenue, city, state, country, address, employees, foundation |
| contacts | JSON Array Object \(Entity Relations\) | Information about company's contacts |
| dateCreated | datetime | Company creation timestamp |
| dateUpdated | datetime | Company updated timestamp |

### **Permissions**

To request a company endpoint you will need a valid API Key with the company access permissions enabled.

### **Relations between companies and other entities**

A company has many contacts. Contacts belong to a company. 

### Parameters

<table>
  <thead>
    <tr>
      <th style="text-align:left">Name</th>
      <th style="text-align:left">Data Type</th>
      <th style="text-align:left">Details</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Relations</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">
        <p>to get other objects with a company such as</p>
        <p>contacts or parent or companies</p>
      </td>
    </tr>
  </tbody>
</table>

