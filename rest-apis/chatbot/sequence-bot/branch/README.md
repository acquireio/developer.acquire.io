---
description: A branch is a single node of a Sequence bot.
---

# Branch

The Branch endpoints allow you to create, retrieve, update, and delete branches of a Sequence. 

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
      <td style="text-align:left">Specify the ID of the Branch.</td>
    </tr>
    <tr>
      <td style="text-align:left">title</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">Specify the title of the Branch.</td>
    </tr>
    <tr>
      <td style="text-align:left">visibleOrder</td>
      <td style="text-align:left">Integer</td>
      <td style="text-align:left">
        <p>The order in which the branch will execute on the</p>
        <p>widget side (as a lead can have multiple branches)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">isParent</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">Specify the parent branch or not.</td>
    </tr>
    <tr>
      <td style="text-align:left">leadEdges</td>
      <td style="text-align:left">JSON Array Object
        <br />(Entity Relations)</td>
      <td style="text-align:left">
        <p>A branch will have multiple edges,</p>
        <p>these edges can be &quot;bubble&quot;, &quot;action&quot; or</p>
        <p>&quot;text message&quot;</p>
      </td>
    </tr>
  </tbody>
</table>

### Permissions

To request a Branch endpoint, you will need a valid API Key with Sequence chatbot access permissions enabled.

