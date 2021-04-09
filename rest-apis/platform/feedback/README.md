---
description: >-
  Feedback or rating functionality allows organizations to capture feedback from
  customers about their experience with an agent.
---

# Feedback

These endpoints allow you to retrieve, add and manage questions to collect feedback after a conversation.

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
      <td style="text-align:left">Specify the ID of the feedback.</td>
    </tr>
    <tr>
      <td style="text-align:left">question</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">Specify the question of feedback.</td>
    </tr>
    <tr>
      <td style="text-align:left">type</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">
        <p>Specify the type of feedback</p>
        <p>[&apos;Rating&apos;, &apos;Text&apos;, &apos;Radio&apos;, &apos;Checkbox&apos;]</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">config</td>
      <td style="text-align:left">JSON Array Object</td>
      <td style="text-align:left">Specify the feedback details.</td>
    </tr>
    <tr>
      <td style="text-align:left">departments</td>
      <td style="text-align:left">JSON Array Object (Entity Relations)</td>
      <td style="text-align:left">Specify the departments receiving the feedback.</td>
    </tr>
    <tr>
      <td style="text-align:left">channels</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">
        <p>Specify the feedback channels</p>
        <p>[&apos;Chat&apos;, &apos;SMS&apos;, &apos;Email&apos;].</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">dateCreated</td>
      <td style="text-align:left">datetime</td>
      <td style="text-align:left">Specify the timestamp of the feedback.</td>
    </tr>
    <tr>
      <td style="text-align:left">status</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">Specify the status of the feedback.</td>
    </tr>
  </tbody>
</table>

### Permissions

To request a feedback endpoint, you will need a valid API Key with the feedback permissions enabled.

