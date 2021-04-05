---
description: >-
  Field for collecting and mapping data such as name and email in Acquire. Can
  be synced from other systems.
---

# Custom Attributes

Manage custom fields associated with different objects. This API allows you to define custom fields for your account using Custom Attributes API.

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
      <td style="text-align:left">Specify the ID of the Custom Attributes</td>
    </tr>
    <tr>
      <td style="text-align:left">object</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">Specify the attribute key</td>
    </tr>
    <tr>
      <td style="text-align:left">key</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">Specify the color of the Tag</td>
    </tr>
    <tr>
      <td style="text-align:left">type</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">
        <p>Specify the origin like system-defined</p>
        <p>or custom generated.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">config</td>
      <td style="text-align:left">JSON Array Object</td>
      <td style="text-align:left">Specify the field details</td>
    </tr>
  </tbody>
</table>

### Permissions 

To request a custom attribute endpoint, you will need a valid API Key with the Custom Attribute permissions enabled.

