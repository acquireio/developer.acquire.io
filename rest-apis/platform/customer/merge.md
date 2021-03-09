# Merge

Using this API you can merge two customers \(contacts\). The contact ID in the endpoint URL **\(primary\_contact\_id\)** is included in the primary and the contact ID **\(secondary\_contact\_ids\)** in the request body will indicate the contact to be merged. Secondary \(selected\) contact information such as conversation, chats, notes, views, etc. will be merged into primary contact.  
**primary\_contact\_id:** will be placed in the path parameter within the endpoint.  
**secordary\_contact\_id:** will be placed in the request body.  


| `NOTE:` | Merged contact cannot be revert. |
| :--- | :--- |


### PARAMETERS

| ATTRIBUTE | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| primary\_contact\_id | Integer | ID of the source contact |
| secondary\_contact\_ids | Array of integers | IDs of the secondary contacts |

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/contact/merge/{{contactId}}" path="" %}
{% api-method-summary %}
Merge Customer
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
Bearer \*\*\*\*\*\*\*\*\*\*YOUR\_API\_KEY\*\*\*\*\*\*\*\*\*\*\*\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="mergeId" type="string" required=true %}
 78 \(Customer ID that the customer has to merge\).
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "data": {
        "id": 83,
        "message": "#78 contact timeline's merged with #83 successfully."
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

