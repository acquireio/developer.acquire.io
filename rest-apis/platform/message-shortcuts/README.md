---
description: >-
  Shortcuts are predefined chat messages that can be used by agents during
  conversations.
---

# Message Shortcuts

This API allows you to manage message shortcuts, and provides a faster way to type your message. The message shortcut API can be used to create,  retrieve, update, and delete shortcuts.

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
      <td style="text-align:left">id</td>
      <td style="text-align:left">Integer</td>
      <td style="text-align:left">Specify the ID of the shortcut</td>
    </tr>
    <tr>
      <td style="text-align:left">shortcut_name</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">Specify the name of the shortcut</td>
    </tr>
    <tr>
      <td style="text-align:left">message</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">Specify the content of the shortcut</td>
    </tr>
    <tr>
      <td style="text-align:left">messageJson</td>
      <td style="text-align:left">JSON Array Object</td>
      <td style="text-align:left">
        <p>Specify the JSON conversion of</p>
        <p>the Actual message</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">messageHtml</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">
        <p>Specify the HTML conversion of</p>
        <p>the actual message</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">department</td>
      <td style="text-align:left">JSON Array</td>
      <td style="text-align:left">Specify the departments that use the shortcut</td>
    </tr>
    <tr>
      <td style="text-align:left">groupName</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">Specify the group of shortcut</td>
    </tr>
  </tbody>
</table>

### Permissions

To request a message shortcuts endpoint, you will need a valid API Key with the Message Shortcuts permissions enabled.

