---
description: >-
  Snooze allows the agent to remove the conversation from active view for a set
  time.
---

# Snooze

This API allows you to manage snooze for a specific day and time. That conversation will be snooze marked on the specified day and time. 

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
      <td style="text-align:left">Specify the ID of the Snooze</td>
    </tr>
    <tr>
      <td style="text-align:left">object</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">Specify the attribute key</td>
    </tr>
    <tr>
      <td style="text-align:left">key</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">Specify the attribute key</td>
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

To request a snooze endpoint, you will need a valid API Key with the Snooze permissions enabled.

