# Merge contact

Use this endpoint to merge two or more contacts. The secondary contacts **\(mergeIds\)** will be merged onto the primary contact \(**primary\_contact\_id\)**. Merge data includes conversation, chats, notes, views, etc. The primary contact ID in the endpoint URL **\(primary\_contact\_id\)** is required. Place the secondary\_contact\_ids  in the request body.

**Contact Ids** can be found by going to the Acquire platform and hovering over a contact's name in `Contact List` or by using the endpoint Get All Contacts.

If a secondary merge's contact details different from the primary contact details, both contact details will be preserved on the primary contact. For example, if a secondary merge contact has an email that differs from their primary email, both emails will be preserved on the primary contact after the merge.

{% hint style="danger" %}
Warning: merges cannot be reverted.
{% endhint %}

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api/v1/crm/contact/merge/{{contactId}}" path="" %}
{% api-method-summary %}
Merge Contact
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="contactId" type="integer" required=true %}
The ID of a contact. 
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="mergeId" type="integer" required=true %}
 The ID of the contact you want to merge.
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

| ATTRIBUTE | TYPE | DESCRIPTION |
| :--- | :--- | :--- |
| mergeId | Array of integers | IDs of the secondary contacts |

## Body\(raw\)

```text
{
  "mergeId": [
    11
  ]
}
```

