# Delete contact

{% api-method method="delete" host="https://{{account\_id}}.acquire.io/api/v1/crm/objects/contact/{{contactId}}" path="" %}
{% api-method-summary %}
Delete contact
{% endapi-method-summary %}

{% api-method-description %}
 Delete a customer. The **contactId** must be passed in to the endpoint as a path parameter. **Warning**: This action cannot be undone.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="contactId" type="integer" required=true %}
The contact's ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "data": {
    "deleted": 1
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



