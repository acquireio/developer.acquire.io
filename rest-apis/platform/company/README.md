# Company

Companies constitute the organization to which customers belong. When you have conversations with several people from counterpart companies, it is better to group them in an organization. The Company API can be used to create, update, retrieves, and delete records in a company object. Ensure that the **relations** parameter with the value **contacts** is required to obtain contact information.

| ATTRIBUTE | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| id | Integer | ID of the company |
| fields | JSON object \(Entity Relations\) | Information of company such as company name, website, industry, description, source, revenue, city, state, country, address, employees, foundation |
| contacts | JSON Array Object \(Entity Relations\) | Information of company contacts |
| dateCreated | datetime | Company creation timestamp |
| dateUpdated | datetime | Company updated timestamp |

**Permissions**

To request a company endpoint you will need a valid API key with the company access permissions.

**Relations between companies and other entities**

Companies belong one-to-many relations with customers.

#### PARAMS <a id="params"></a>

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

