---
description: Notes are texts that are linked to case and contact objects.
---

# Notes

Create, retrieve, update or delete notes for a particular contact or case.

## Attributes

<table>
  <thead>
    <tr>
      <th style="text-align:left">Attribute</th>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">id</td>
      <td style="text-align:left">Integer</td>
      <td style="text-align:left">Specifies ID of the note.</td>
    </tr>
    <tr>
      <td style="text-align:left">contactId</td>
      <td style="text-align:left">Integer</td>
      <td style="text-align:left">
        <p>Specifies the contactID of the note</p>
        <p>under which it was created.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">type</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">
        <p>Specifies the type of note and whether or not</p>
        <p>it&apos;s a separate note or a note message.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">title</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">Specifies the title of the note which was created.</td>
    </tr>
    <tr>
      <td style="text-align:left">description</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">Specifies the description of the note.</td>
    </tr>
    <tr>
      <td style="text-align:left">userId</td>
      <td style="text-align:left">Integer</td>
      <td style="text-align:left">Specifies the ID of the user who created the note.</td>
    </tr>
    <tr>
      <td style="text-align:left">dateCreated</td>
      <td style="text-align:left">Date</td>
      <td style="text-align:left">Specifies the date on which the note was created.</td>
    </tr>
    <tr>
      <td style="text-align:left">users</td>
      <td style="text-align:left">Object</td>
      <td style="text-align:left">
        <p>Specifies the details of the users</p>
        <p>involved in the notes.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">lastMessage</td>
      <td style="text-align:left">Object</td>
      <td style="text-align:left">Specifies the last, or most recent, message in the note section</td>
    </tr>
  </tbody>
</table>

## Permissions

To request a case endpoint, you will need a valid API key with note access permissions.

