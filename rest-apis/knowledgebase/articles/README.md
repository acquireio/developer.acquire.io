---
description: Articles are pages in a Knowledge Base.
---

# Articles

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
      <td style="text-align:left">Specify the article Id</td>
    </tr>
    <tr>
      <td style="text-align:left">groupId</td>
      <td style="text-align:left">JSON Object</td>
      <td style="text-align:left">
        <p>Specify the Id of the groups</p>
        <p>to which the article belongs to</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">title</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">Specify the title of the article</td>
    </tr>
    <tr>
      <td style="text-align:left">description</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">Specify the description of the article</td>
    </tr>
    <tr>
      <td style="text-align:left">content</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">Specify the html content of the article</td>
    </tr>
    <tr>
      <td style="text-align:left">jsonContent</td>
      <td style="text-align:left">JSON Object</td>
      <td style="text-align:left">
        <p>Specify the json content of the article</p>
        <p>which has block and entity map</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">articleSlug</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">Specify the key of the article</td>
    </tr>
    <tr>
      <td style="text-align:left">featuresImage</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">Specify the image url of the article</td>
    </tr>
    <tr>
      <td style="text-align:left">updatedBy</td>
      <td style="text-align:left">JSON Object</td>
      <td style="text-align:left">Specify the array of users who updated the article</td>
    </tr>
    <tr>
      <td style="text-align:left">tags</td>
      <td style="text-align:left">JSON Array</td>
      <td style="text-align:left">Specify the tags related to the article</td>
    </tr>
    <tr>
      <td style="text-align:left">dateCreated</td>
      <td style="text-align:left">datetime</td>
      <td style="text-align:left">Specify the date on which article created</td>
    </tr>
    <tr>
      <td style="text-align:left">dateUpdated</td>
      <td style="text-align:left">datetime</td>
      <td style="text-align:left">Specify the date on which article updated</td>
    </tr>
    <tr>
      <td style="text-align:left">status</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">Specify the status of the article</td>
    </tr>
    <tr>
      <td style="text-align:left">createdBy</td>
      <td style="text-align:left">Integer</td>
      <td style="text-align:left">Specify the userId of the person who created the article</td>
    </tr>
  </tbody>
</table>

### **Permissions**

To request this endpoint you will need a valid API Key with the knowledge-base access permissions enabled.

