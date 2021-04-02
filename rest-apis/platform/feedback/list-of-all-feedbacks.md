# List of all feedback

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/feedback" path="" %}
{% api-method-summary %}
All Feedbacks
{% endapi-method-summary %}

{% api-method-description %}
Retrieve a list of all feedback questions. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="order" type="object" required=false %}
Object type where you can mention field name followed by value. eg: {"id":"DESC"}
{% endapi-method-parameter %}

{% api-method-parameter name="where" type="object" required=false %}
Object type where you can specify field name followed by a value. eg: {"search":"How"}
{% endapi-method-parameter %}

{% api-method-parameter name="select" type="array" required=false %}
An array of strings which includes the fields in return Eg: "id","type" etc.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "data": {
    "count": 1,
    "departmentList": {
      "list": [
        {
          "id": 6,
          "name": "eswweew "
        },
        {
          "id": 7,
          "name": "fdhfthnfgg"
        },
        {
          "id": 8,
          "name": "Youpps"
        },
        {
          "id": 9,
          "name": "robust"
        },
        {
          "id": 10,
          "name": "qwe"
        },
        {
          "id": 11,
          "name": "moi"
        },
        {
          "id": 12,
          "name": "roi"
        },
        {
          "id": 13,
          "name": "eoi"
        }
      ],
      "success": "true"
    },
    "data": [
      {
        "id": 36,
        "question": "How satisfied?",
        "type": "rating",
        "config": {
          "values": [
            {
              "icon": "settings/feedback-5.svg",
              "label": "DISLIKE",
              "value": "5"
            }
          ],
          "required": true,
          "rating_type": "star",
          "error_message": "Invalid Input"
        },
        "departments": [],
        "channels": [
          "email"
        ],
        "dateCreated": "2021-03-17T04:27:48.000Z",
        "status": "active"
      }
    ]
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



