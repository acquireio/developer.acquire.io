---
description: API to get all the custom attributes available
---

# List of custom attributes

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/crm/objects/object-field" path="" %}
{% api-method-summary %}
List of Custom Attributes
{% endapi-method-summary %}

{% api-method-description %}
API to get a list of all available custom attributes
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="select" type="array" required=false %}
Array type with selected fields to be retrived Available values: id,object,key,type,config
{% endapi-method-parameter %}

{% api-method-parameter name="relations" type="array" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="where" type="array" required=false %}
Specify array of objects with rules as {FIELD\_NAME\|CONDITION\|VALUE}
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
    "page": 0,
    "offset": 0,
    "limit": 20,
    "count": 34,
    "data": [
      {
        "id": 34,
        "object": "case",
        "key": "title",
        "type": "text",
        "config": {
          "input": {
            "type": "text",
            "label": "title",
            "required": true,
            "placeholder": "",
            "validationType": "format",
            "validationFormat": "any",
            "requiredErrorMessage": "Please add an attribute name.",
            "validationErrorMessage": "Oops! Seems incorrect format that you entered."
          },
          "label": "title",
          "backend": {
            "list": false
          },
          "capture": [
            "api"
          ],
          "online_order": 33,
          "offline_order": 33
        },
        "system": "no"
      },
      {
        "id": 33,
        "object": "contact",
        "key": "completed",
        "type": "text",
        "config": {
          "input": {
            "type": "text",
            "label": "Completed",
            "required": true,
            "placeholder": "",
            "validationType": "format",
            "validationFormat": "any",
            "requiredErrorMessage": "Please add an attribute name.",
            "validationErrorMessage": "Oops! Seems incorrect format that you entered."
          },
          "label": "Completed",
          "backend": {
            "list": false
          },
          "capture": [
            "api"
          ],
          "online_order": 32,
          "offline_order": 32
        },
        "system": "no"
      },
      {
        "id": 32,
        "object": "contact",
        "key": "sadfcdsfcfs",
        "type": "text",
        "config": {
          "input": {
            "type": "department",
            "label": "saDfcdsfcfs",
            "required": true,
            "validationType": "format",
            "validationFormat": "any",
            "requiredErrorMessage": "Please add an attribute name.",
            "validationErrorMessage": "Oops! Seems incorrect format that you entered."
          },
          "label": "saDfcdsfcfs",
          "backend": {
            "list": false
          },
          "capture": [
            "api"
          ],
          "online_order": 31,
          "offline_order": 31
        },
        "system": "no"
      },
      {
        "id": 31,
        "object": "contact",
        "key": "hjk",
        "type": "text",
        "config": {
          "input": {
            "type": "department",
            "label": "hjk",
            "required": true,
            "validationType": "format",
            "validationFormat": "any",
            "requiredErrorMessage": "Please add an attribute name.",
            "validationErrorMessage": "Oops! Seems incorrect format that you entered."
          },
          "label": "hjk",
          "backend": {
            "list": false
          },
          "capture": [
            "api"
          ],
          "online_order": 30,
          "offline_order": 30
        },
        "system": "no"
      },
      {
        "id": 30,
        "object": "contact",
        "key": "ytuyy",
        "type": "text",
        "config": {
          "input": {
            "type": "department",
            "label": "ytuyy",
            "required": true,
            "validationType": "format",
            "validationFormat": "any",
            "requiredErrorMessage": "Please add an attribute name.",
            "validationErrorMessage": "Oops! Seems incorrect format that you entered."
          },
          "label": "ytuyy",
          "backend": {
            "list": false
          },
          "capture": [
            "api"
          ],
          "online_order": 29,
          "offline_order": 29
        },
        "system": "no"
      },
      {
        "id": 29,
        "object": "contact",
        "key": "checks",
        "type": "text",
        "config": {
          "input": {
            "type": "checkbox",
            "label": "checks",
            "options": [
              "1",
              "2",
              "3"
            ],
            "required": true,
            "validationType": "format",
            "validationFormat": "any",
            "requiredErrorMessage": "Please add an attribute name.",
            "validationErrorMessage": "Oops! Seems incorrect format that you entered."
          },
          "label": "checks",
          "backend": {
            "list": false
          },
          "capture": [
            "api"
          ],
          "online_order": 28,
          "offline_order": 28
        },
        "system": "no"
      },
      {
        "id": 28,
        "object": "contact",
        "key": "radios",
        "type": "text",
        "config": {
          "input": {
            "type": "radio",
            "label": "radios",
            "options": [
              "1",
              "2",
              "3"
            ],
            "required": true,
            "validationType": "format",
            "validationFormat": "any",
            "requiredErrorMessage": "Please add an attribute name.",
            "validationErrorMessage": "Oops! Seems incorrect format that you entered."
          },
          "label": "radios",
          "backend": {
            "list": false
          },
          "capture": [
            "api"
          ],
          "online_order": 27,
          "offline_order": 27
        },
        "system": "no"
      },
      {
        "id": 27,
        "object": "case",
        "key": "wishing_text",
        "type": "text",
        "config": {
          "input": {
            "type": "text",
            "label": "Wishing Text",
            "required": true,
            "placeholder": "",
            "validationType": "format",
            "validationFormat": "any",
            "requiredErrorMessage": "Please add an attribute name.",
            "validationErrorMessage": "Oops! Seems incorrect format that you entered."
          },
          "label": "Wishing Text",
          "backend": {
            "list": false
          },
          "capture": [
            "api"
          ],
          "online_order": 26,
          "offline_order": 26
        },
        "system": "no"
      },
      {
        "id": 26,
        "object": "case",
        "key": "wishing_radios",
        "type": "text",
        "config": {
          "input": {
            "type": "radio",
            "label": "Wishing Radios",
            "options": [
              "a",
              "b",
              "c"
            ],
            "required": true,
            "validationType": "format",
            "validationFormat": "any",
            "requiredErrorMessage": "Please add an attribute name.",
            "validationErrorMessage": "Oops! Seems incorrect format that you entered."
          },
          "label": "Wishing Radios",
          "backend": {
            "list": false
          },
          "capture": [
            "api"
          ],
          "online_order": 25,
          "offline_order": 25
        },
        "system": "no"
      },
      {
        "id": 25,
        "object": "case",
        "key": "wishig_checks",
        "type": "text",
        "config": {
          "input": {
            "type": "checkbox",
            "label": "Wishig Checks",
            "options": [
              "a",
              "b",
              "c"
            ],
            "required": true,
            "validationType": "format",
            "validationFormat": "any",
            "requiredErrorMessage": "Please add an attribute name.",
            "validationErrorMessage": "Oops! Seems incorrect format that you entered."
          },
          "label": "Wishig Checks",
          "backend": {
            "list": false
          },
          "capture": [
            "api"
          ],
          "online_order": 24,
          "offline_order": 24
        },
        "system": "no"
      },
      {
        "id": 24,
        "object": "case",
        "key": "remark",
        "type": "text",
        "config": {
          "input": {
            "type": "text",
            "label": "Remark",
            "required": false,
            "placeholder": "",
            "validationType": "format",
            "validationFormat": "any",
            "requiredErrorMessage": "Please add an attribute name.",
            "validationErrorMessage": "Oops! Look like you entered the wrong text."
          },
          "label": "Remark",
          "backend": {
            "list": false
          },
          "capture": [
            "api"
          ],
          "online_order": 23,
          "offline_order": 23
        },
        "system": "yes"
      },
      {
        "id": 23,
        "object": "company",
        "key": "foundation",
        "type": "text",
        "config": {
          "capture": [
            "api"
          ]
        },
        "system": "no"
      },
      {
        "id": 22,
        "object": "company",
        "key": "employees",
        "type": "text",
        "config": {
          "input": {
            "label": "Employees",
            "validationType": "format",
            "validationFormat": "any",
            "validationErrorMessage": "Oops! Look like you entered the wrong text."
          },
          "label": "Employees",
          "capture": [
            "api"
          ],
          "online_order": 22,
          "offline_order": 22
        },
        "system": "no"
      },
      {
        "id": 21,
        "object": "company",
        "key": "address",
        "type": "text",
        "config": {
          "capture": [
            "api"
          ],
          "online_order": 21,
          "offline_order": 21
        },
        "system": "no"
      },
      {
        "id": 20,
        "object": "company",
        "key": "countryId",
        "type": "text",
        "config": {
          "capture": [
            "api"
          ],
          "online_order": 20,
          "offline_order": 20
        },
        "system": "yes"
      },
      {
        "id": 19,
        "object": "company",
        "key": "state",
        "type": "text",
        "config": {
          "capture": [
            "api"
          ],
          "online_order": 19,
          "offline_order": 19
        },
        "system": "yes"
      },
      {
        "id": 18,
        "object": "company",
        "key": "city",
        "type": "text",
        "config": {
          "capture": [
            "api"
          ],
          "online_order": 18,
          "offline_order": 18
        },
        "system": "yes"
      },
      {
        "id": 17,
        "object": "company",
        "key": "revenue",
        "type": "text",
        "config": {
          "capture": [
            "api"
          ],
          "online_order": 17,
          "offline_order": 17
        },
        "system": "yes"
      },
      {
        "id": 16,
        "object": "company",
        "key": "source",
        "type": "text",
        "config": {
          "capture": [
            "api"
          ],
          "online_order": 16,
          "offline_order": 16
        },
        "system": "yes"
      },
      {
        "id": 15,
        "object": "company",
        "key": "description",
        "type": "text",
        "config": {
          "capture": [
            "api"
          ],
          "online_order": 15,
          "offline_order": 15
        },
        "system": "yes"
      }
    ]
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

