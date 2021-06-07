---
description: Retrieve and manipulate details for users (also known as agents).
---

# Users

These endpoints can be used to retrieve, create, update, and delete account users and their details.  

### Attributes 

<table>
  <thead>
    <tr>
      <th style="text-align:left">ATTRIBUTE</th>
      <th style="text-align:left">TYPE</th>
      <th style="text-align:left">DESCRIPTION</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">count</td>
      <td style="text-align:left">Integer</td>
      <td style="text-align:left">Represents the number of records exists</td>
    </tr>
    <tr>
      <td style="text-align:left">data</td>
      <td style="text-align:left">JSON object</td>
      <td style="text-align:left">
        <p>Information about the user</p>
        <p>which contains the details as firstname,</p>
        <p>lastname,id,type,status,</p>
        <p>name,email,phone,photo,language</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">roles</td>
      <td style="text-align:left">JSON Array Object</td>
      <td style="text-align:left">
        <p>Specify the User roles</p>
        <p>which has the properties id,rolename,</p>
        <p>permissions,permissionType</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">departments</td>
      <td style="text-align:left">JSON Array Object</td>
      <td style="text-align:left">
        <p>Specify the departments to</p>
        <p>which the User belongs to and</p>
        <p>the department properties</p>
      </td>
    </tr>
  </tbody>
</table>

### **Permissions**

To request this endpoint you will need a valid API Key with the account access permissions enabled.

### **Relations between Users and other entities**

A user can be a part of many departments and have multiple roles.

