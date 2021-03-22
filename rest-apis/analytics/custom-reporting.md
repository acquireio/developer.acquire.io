# Custom Reporting

{% api-method method="delete" host="https://{{account\_id}}.acquire.io/api" path="/v1/analytics/custom-reporting/edit-custom-report" %}
{% api-method-summary %}
Delete Custom Chart
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter type="string" name="Authorization" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="chart\_id" type="string" required=true %}
Id of chart to delete
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
    "success": true,
    "data": {
      "title": "test chart",
      "config": [
        {
          "key": "id",
          "filters": [
            {
              "key": "id",
              "conditions": [
                {
                  "key": "is",
                  "searchValue": [
                    "1"
                  ]
                }
              ]
            }
          ],
          "joinType": "AND",
          "availableAggregation": [
            "group_by",
            "count",
            "list"
          ],
          "label": "Id"
        }
      ],
      "chartKey": "test-chart",
      "chartType": "table",
      "tenantId": "4wic4e",
      "id": 50,
      "data": [
        {
          "main_case_id": 1,
          "main_contact_id": 1,
          "id": 1
        }
      ],
      "totalCount": 1
    }
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api" path="/v1/analytics/custom-reporting/edit-custom-report" %}
{% api-method-summary %}
Create Custom Chart
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter type="string" name="Authorization" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Body\(raw\)

```text
{
  "title": "test chart",
  "config": [
    {
      "key": "id",
      "filters": [
        {
          "key": "id",
          "conditions": [
            {
              "key": "is",
              "searchValue": [
                "1"
              ]
            }
          ]
        }
      ]
    }
  ],
  "objectKey": "conversations",
  "chartType": "table"
}
```

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api" path="/v1/analytics/custom-reporting/edit-custom-report" %}
{% api-method-summary %}
Edit Custom Report
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter type="string" name="Authorization" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="reportKey" type="string" required=true %}
Key for report which you want to edit.
{% endapi-method-parameter %}

{% api-method-parameter name="description" type="string" required=false %}
Add description for report
{% endapi-method-parameter %}

{% api-method-parameter name="reportName" type="string" required=false %}
Name of report
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://{{account\_id}}.acquire.io/api" path="/v1/analytics/custom-reporting/generate-report" %}
{% api-method-summary %}
Create Custom Report
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter type="string" name="Authorization" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="objectKey" type="string" required=true %}
Selected object type. You can object key by calling Get Data Points API mentioned below.
{% endapi-method-parameter %}

{% api-method-parameter name="description" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="reportName" type="string" required=true %}
Name of report
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="delete" host="https://{{account\_id}}.acquire.io/api" path="/v1/analytics/custom-reporting/delete-custom-report" %}
{% api-method-summary %}
Delete Custom Report details
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="report\_key" type="string" required=true %}
Key of report which you want to delete.You can get report key by calling Get All Custom Reports API.
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
    "success": true
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api" path="/v1/analytics/custom-reporting/get-custom-report?report\_key=aloktestreport&offset=%2B00%3A00" %}
{% api-method-summary %}
Get Custom Report details
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter type="string" name="Authorization" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="report\_key" type="string" required=true %}
Key of report which you want to get data.You can get report key by calling Get All Custom Reports API.
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="offset" %}
This parameter is used for the timezone value and the default timezone will be "GMT". e.g. +05:30 for particular timezone. Default is +00:00
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
    "success": true,
    "customReport": {
      "reportName": "test report",
      "description": "test",
      "objectKey": "operator",
      "id": 37,
      "reportKey": "testreport"
    },
    "reportData": [
      {
        "id": 33,
        "title": "first table report",
        "chartKey": "first-table-report",
        "chartType": "table",
        "config": [
          {
            "key": "id",
            "label": "Operator Id",
            "filters": [],
            "dataType": "number",
            "joinType": "AND",
            "aggregation": "group_by",
            "aggregationLabel": "Operator Id",
            "availableAggregation": [
              "group_by",
              "count",
              "list"
            ]
          },
          {
            "key": "average_response_time",
            "label": "Average Response Time",
            "filters": [
              {
                "key": "average_response_time",
                "conditions": [
                  {
                    "key": "between",
                    "searchValue": [
                      "0",
                      "10"
                    ]
                  }
                ]
              }
            ],
            "customUi": {
              "duration": true
            },
            "dataType": "object",
            "joinType": "AND",
            "aggregation": "avg",
            "aggregationLabel": "Response Time",
            "availableAggregation": [
              "sum",
              "avg",
              "list"
            ]
          }
        ],
        "reportId": 37,
        "tenantId": "4wic4e",
        "data": [
          {
            "id": 56,
            "average_response_time": 9
          }
        ],
        "totalCount": 1
      },
      {
        "id": 34,
        "title": "report without aggregation",
        "chartKey": "report-without-aggregation",
        "chartType": "table",
        "config": [
          {
            "key": "id",
            "label": "Operator Id",
            "filters": [],
            "dataType": "number",
            "joinType": "AND",
            "aggregationLabel": "Operator Id",
            "availableAggregation": [
              "group_by",
              "count",
              "list"
            ]
          },
          {
            "key": "average_response_time",
            "label": "Average Response Time",
            "filters": [
              {
                "key": "average_response_time",
                "conditions": [
                  {
                    "key": "between",
                    "searchValue": [
                      "0",
                      "10"
                    ]
                  }
                ]
              }
            ],
            "customUi": {
              "duration": true
            },
            "dataType": "object",
            "joinType": "AND",
            "aggregationLabel": "Response Time",
            "availableAggregation": [
              "sum",
              "avg",
              "list"
            ]
          }
        ],
        "reportId": 37,
        "tenantId": "4wic4e",
        "data": [
          {
            "id": 56,
            "operator_id": 56,
            "average_response_time": 9
          }
        ],
        "totalCount": 1
      }
    ]
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api" path="/v1/analytics/custom-reporting/get-all-custom-report" %}
{% api-method-summary %}
Get All custom reports
{% endapi-method-summary %}

{% api-method-description %}
Get list of all custom reports with name, description and report key.Report key will be used to get details of custom report.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter type="string" name="Authorization" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
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
    "success": true,
    "customReport": [
      {
        "id": 35,
        "reportName": "Test_Report",
        "description": "test",
        "reportKey": "testreport"
      }
    ]
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api" path="/v1/analytics/custom-reporting/get-data-points" %}
{% api-method-summary %}
Get All Datapoints
{% endapi-method-summary %}

{% api-method-description %}
API will give you all available datapoints for available objects.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter type="string" name="Authorization" required=true %}
Bearer \*\*\*YOUR\_API\_KEY\*\*\*
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
    "objects": [
      {
        "objectName": "Conversations",
        "objectKey": "conversations",
        "dataSource": [
          {
            "label": "Id",
            "key": "id",
            "options": [],
            "filters": [
              {
                "label": "Id",
                "key": "id",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Is",
                    "key": "is",
                    "supportMultiple": false
                  },
                  {
                    "label": "In",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "number",
            "availableAggregation": [
              "group_by",
              "count",
              "list"
            ]
          },
          {
            "label": "Title",
            "key": "title",
            "options": [],
            "filters": [
              {
                "label": "Title",
                "key": "title",
                "dataType": "text",
                "options": [],
                "conditions": [
                  {
                    "label": "Is",
                    "key": "is",
                    "supportMultiple": false
                  },
                  {
                    "label": "Contains",
                    "key": "like",
                    "supportMultiple": false
                  },
                  {
                    "label": "One of",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "text",
            "customUi": {
              "isEmojiSupported": true
            },
            "availableAggregation": [
              "list"
            ]
          },
          {
            "label": "Description",
            "key": "description",
            "options": [],
            "filters": [
              {
                "label": "Description",
                "key": "description",
                "dataType": "text",
                "options": [],
                "conditions": [
                  {
                    "label": "Is",
                    "key": "is",
                    "supportMultiple": false
                  },
                  {
                    "label": "Contains",
                    "key": "like",
                    "supportMultiple": false
                  },
                  {
                    "label": "One of",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "text",
            "customUi": {
              "isEmojiSupported": true
            },
            "availableAggregation": [
              "list"
            ]
          },
          {
            "label": "Contact Name",
            "key": "contact_name",
            "options": [],
            "filters": [
              {
                "label": "Contact Name",
                "key": "name",
                "dataType": "text",
                "options": [],
                "conditions": [
                  {
                    "label": "Is",
                    "key": "is",
                    "supportMultiple": false
                  },
                  {
                    "label": "Contains",
                    "key": "like",
                    "supportMultiple": false
                  },
                  {
                    "label": "One of",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "text",
            "availableAggregation": [
              "group_by",
              "count",
              "list"
            ]
          },
          {
            "label": "Contact Email",
            "key": "contact_email",
            "options": [],
            "filters": [
              {
                "label": "Contact Email",
                "key": "email",
                "dataType": "text",
                "options": [],
                "conditions": [
                  {
                    "label": "Is",
                    "key": "is",
                    "supportMultiple": false
                  },
                  {
                    "label": "Contains",
                    "key": "like",
                    "supportMultiple": false
                  },
                  {
                    "label": "One of",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "object",
            "availableAggregation": [
              "group_by",
              "count",
              "list"
            ]
          },
          {
            "label": "Visit Id",
            "key": "visit_visit_id",
            "filters": [
              {
                "label": "Visit Id",
                "key": "id",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Is",
                    "key": "is",
                    "supportMultiple": false
                  },
                  {
                    "label": "In",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "group_by",
              "list"
            ]
          },
          {
            "label": "Visit Date",
            "key": "visit_date",
            "filters": [
              {
                "label": "Visit Date",
                "key": "date_created",
                "dataType": "datetime",
                "options": [],
                "conditions": [
                  {
                    "label": "Equals",
                    "key": "between",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "group_by",
              "list"
            ]
          },
          {
            "label": "Visit Source URL",
            "key": "visit_source",
            "filters": [
              {
                "label": "Source URL",
                "key": "source",
                "dataType": "text",
                "options": [],
                "conditions": [
                  {
                    "label": "Is",
                    "key": "is",
                    "supportMultiple": false
                  },
                  {
                    "label": "Contains",
                    "key": "like",
                    "supportMultiple": false
                  },
                  {
                    "label": "One of",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "group_by",
              "list"
            ]
          },
          {
            "label": "Site URL",
            "key": "site_url",
            "filters": [
              {
                "label": "Site URL",
                "key": "url",
                "dataType": "text",
                "options": [],
                "conditions": [
                  {
                    "label": "Is",
                    "key": "is",
                    "supportMultiple": false
                  },
                  {
                    "label": "Contains",
                    "key": "like",
                    "supportMultiple": false
                  },
                  {
                    "label": "One of",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "group_by",
              "list"
            ]
          },
          {
            "label": "Channel",
            "key": "channel",
            "options": [
              {
                "label": "Chat",
                "value": "chat"
              },
              {
                "label": "VoIP",
                "value": "voip"
              },
              {
                "label": "SMS",
                "value": "sms"
              },
              {
                "label": "Mail",
                "value": "mail"
              },
              {
                "label": "Private Form",
                "value": "private-form"
              }
            ],
            "filters": [
              {
                "label": "Channel",
                "key": "channel",
                "dataType": "text",
                "options": [
                  {
                    "label": "Chat",
                    "value": "chat"
                  },
                  {
                    "label": "VoIP",
                    "value": "voip"
                  },
                  {
                    "label": "SMS",
                    "value": "sms"
                  },
                  {
                    "label": "Mail",
                    "value": "mail"
                  },
                  {
                    "label": "Private Form",
                    "value": "private-form"
                  }
                ],
                "conditions": [
                  {
                    "label": "One of",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "text",
            "availableAggregation": [
              "group_by",
              "list"
            ]
          },
          {
            "label": "Status",
            "key": "status",
            "options": [
              {
                "label": "Pending",
                "value": "pending"
              },
              {
                "label": "Active",
                "value": "active"
              },
              {
                "label": "Closed",
                "value": "closed"
              }
            ],
            "filters": [
              {
                "label": "Status",
                "key": "status",
                "dataType": "text",
                "options": [
                  {
                    "label": "Pending",
                    "value": "pending"
                  },
                  {
                    "label": "Active",
                    "value": "active"
                  },
                  {
                    "label": "Closed",
                    "value": "closed"
                  }
                ],
                "conditions": [
                  {
                    "label": "One of",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "text",
            "availableAggregation": [
              "group_by",
              "list"
            ]
          },
          {
            "label": "Reopened",
            "key": "parent_id",
            "options": [
              {
                "label": "Yes",
                "value": "is"
              },
              {
                "label": "No",
                "value": "no"
              }
            ],
            "filters": [
              {
                "label": "Reopened",
                "key": "parent_id",
                "dataType": "text",
                "options": [
                  {
                    "label": "Yes",
                    "value": "is"
                  },
                  {
                    "label": "No",
                    "value": "no"
                  }
                ],
                "conditions": [
                  {
                    "label": "Is",
                    "key": "is",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "dataType": "text",
            "availableAggregation": [
              "group_by",
              "list"
            ]
          },
          {
            "label": "Case Created Date and time",
            "key": "date_created",
            "options": [],
            "filters": [
              {
                "label": "Case Created Date and time",
                "key": "date_created",
                "dataType": "datetime",
                "options": [],
                "conditions": [
                  {
                    "label": "Equals",
                    "key": "between",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "datetime",
            "availableAggregation": [
              "group_by",
              "list"
            ]
          },
          {
            "label": "Case Last Updated Date and time",
            "key": "date_updated",
            "options": [],
            "filters": [
              {
                "label": "Case Last Updated Date and time",
                "key": "date_updated",
                "dataType": "datetime",
                "options": [],
                "conditions": [
                  {
                    "label": "Equals",
                    "key": "between",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "datetime",
            "availableAggregation": [
              "group_by",
              "list"
            ]
          },
          {
            "label": "Case Pending Date and time",
            "key": "date_pending",
            "options": [],
            "filters": [
              {
                "label": "Case Pending Date and time",
                "key": "date_pending",
                "dataType": "datetime",
                "options": [],
                "conditions": [
                  {
                    "label": "Equals",
                    "key": "between",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "datetime",
            "availableAggregation": [
              "group_by",
              "list"
            ]
          },
          {
            "label": "Waiting time for case",
            "key": "wait_time",
            "options": [],
            "filters": [
              {
                "label": "Waiting time for case",
                "key": "wait_time",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "dataType": "number",
            "customUi": {
              "duration": true
            },
            "availableAggregation": [
              "sum",
              "list"
            ]
          },
          {
            "label": "Case Active Date and time",
            "key": "date_active",
            "options": [],
            "filters": [
              {
                "label": "Case Active Date and time",
                "key": "date_active",
                "dataType": "datetime",
                "options": [],
                "conditions": [
                  {
                    "label": "Equals",
                    "key": "between",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "datetime",
            "availableAggregation": [
              "group_by",
              "list"
            ]
          },
          {
            "label": "Case Closed Date and time",
            "key": "date_closed",
            "options": [],
            "filters": [
              {
                "label": "Case Closed Date and time",
                "key": "date_closed",
                "dataType": "datetime",
                "options": [],
                "conditions": [
                  {
                    "label": "Equals",
                    "key": "between",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "datetime",
            "availableAggregation": [
              "group_by",
              "list"
            ]
          },
          {
            "label": "Duration of Case",
            "key": "duration",
            "options": [],
            "filters": [
              {
                "label": "Duration of Case",
                "key": "duration",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "dataType": "number",
            "customUi": {
              "duration": true
            },
            "availableAggregation": [
              "sum",
              "list"
            ]
          },
          {
            "label": "Total Messages",
            "key": "total_messages",
            "filters": [
              {
                "label": "Total Messages",
                "key": "total",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "avg",
              "list"
            ],
            "aggregationLabel": "Messages"
          },
          {
            "label": "Total Sent Messages",
            "key": "total_sent_messages",
            "filters": [
              {
                "label": "Total Sent Messages",
                "key": "total_sent",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "avg",
              "list"
            ],
            "aggregationLabel": "Sent Messages"
          },
          {
            "label": "Total Received Messages",
            "key": "total_received_messages",
            "filters": [
              {
                "label": "Total Received Messages",
                "key": "total_received",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "avg",
              "list"
            ],
            "aggregationLabel": "Received Messages"
          },
          {
            "label": "Total Mails",
            "key": "totalEmails",
            "filters": [
              {
                "label": "Total Mails",
                "key": "totalEmails",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "avg",
              "list"
            ],
            "aggregationLabel": "Mails"
          },
          {
            "label": "Total Sent Mails",
            "key": "totalSentEmails",
            "filters": [
              {
                "label": "Total Sent Mails",
                "key": "totalSentEmails",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "avg",
              "list"
            ],
            "aggregationLabel": "Sent Mails"
          },
          {
            "label": "Total Received Mails",
            "key": "totalReceivedEmails",
            "filters": [
              {
                "label": "Total Received Mails",
                "key": "totalReceivedEmails",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "avg",
              "list"
            ],
            "aggregationLabel": "Received Mails"
          },
          {
            "label": "Total Read Mails",
            "key": "totalReadEmails",
            "filters": [
              {
                "label": "Total Read Mails",
                "key": "totalReadEmails",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "avg",
              "list"
            ],
            "aggregationLabel": "Read Mails"
          },
          {
            "label": "Total Unread Mails",
            "key": "totalUnreadEmails",
            "filters": [
              {
                "label": "Total Unread Mails",
                "key": "totalUnreadEmails",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "avg",
              "list"
            ],
            "aggregationLabel": "Unread Mails"
          },
          {
            "label": "Total Delivered Mails",
            "key": "totalDeliveredEmails",
            "filters": [
              {
                "label": "Total Delivered Mails",
                "key": "totalDeliveredEmails",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "avg",
              "list"
            ],
            "aggregationLabel": "Delivered Mails"
          },
          {
            "label": "Total Replied Mails",
            "key": "totalRepliedEmails",
            "filters": [
              {
                "label": "Total Replied Mails",
                "key": "totalRepliedEmails",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "avg",
              "list"
            ],
            "aggregationLabel": "Replied Mails"
          },
          {
            "label": "Total Bounced Mails",
            "key": "totalBouncedEmails",
            "filters": [
              {
                "label": "Total Bounced Mails",
                "key": "totalBouncedEmails",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "avg",
              "list"
            ],
            "aggregationLabel": "Bounced Mails"
          },
          {
            "label": "Agents Involved",
            "key": "user",
            "options": {},
            "filters": [
              {
                "label": "Agent",
                "key": "user_id",
                "dataType": "number",
                "options": [
                  {
                    "value": 1,
                    "label": "Kaushal Madani"
                  },
                  {
                    "value": 5,
                    "label": "Karan Panwar"
                  },
                  {
                    "value": 6,
                    "label": "Zalak "
                  },
                  {
                    "value": 10,
                    "label": "Test Developer of acquire"
                  },
                  {
                    "value": 11,
                    "label": "dharma"
                  },
                  {
                    "value": 22,
                    "label": "Dev User1"
                  },
                  {
                    "value": 23,
                    "label": "dev_user2@mail.com"
                  },
                  {
                    "value": 24,
                    "label": "dev_user3@mail.com"
                  },
                  {
                    "value": 25,
                    "label": "dev_user4@mail.com"
                  },
                  {
                    "value": 26,
                    "label": "dev_user5@mail.com"
                  },
                  {
                    "value": 27,
                    "label": "dev_user6@mail.com"
                  },
                  {
                    "value": 28,
                    "label": "dev_user7@mail.com"
                  },
                  {
                    "value": 29,
                    "label": "dev_user8@mail.com"
                  },
                  {
                    "value": 30,
                    "label": "dev_user9@mail.com"
                  },
                  {
                    "value": 33,
                    "label": "new test"
                  },
                  {
                    "value": 34,
                    "label": "Hiren Gohil"
                  },
                  {
                    "value": 35,
                    "label": "Test1"
                  },
                  {
                    "value": 36,
                    "label": "Test2"
                  },
                  {
                    "value": 37,
                    "label": "Test3"
                  },
                  {
                    "value": 38,
                    "label": "karan test"
                  },
                  {
                    "value": 56,
                    "label": "Ana 1"
                  },
                  {
                    "value": 64,
                    "label": "User from docs"
                  },
                  {
                    "value": 65,
                    "label": "UserFromAPI0"
                  },
                  {
                    "value": 66,
                    "label": "UserFromAPI1"
                  },
                  {
                    "value": 67,
                    "label": "UserFromAPI2"
                  }
                ],
                "conditions": [
                  {
                    "label": "In",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "object",
            "availableAggregation": [
              "group_by",
              "count",
              "list"
            ]
          },
          {
            "label": "Feedback",
            "key": "feedback",
            "options": [
              {
                "label": "Ratings",
                "value": "text"
              },
              {
                "label": "List Type",
                "value": "list"
              },
              {
                "label": "Multiple",
                "value": "multiple"
              },
              {
                "label": "Ratings",
                "value": "rating"
              },
              {
                "label": "Multiple Radio",
                "value": "multiple_radio"
              },
              {
                "label": "Multiple Checkbox",
                "value": "multiple_checkbox"
              }
            ],
            "filters": [
              {
                "label": "Feedback Type",
                "key": "type",
                "dataType": "text",
                "options": [
                  {
                    "label": "Ratings",
                    "value": "text"
                  },
                  {
                    "label": "List Type",
                    "value": "list"
                  },
                  {
                    "label": "Multiple",
                    "value": "multiple"
                  },
                  {
                    "label": "Ratings",
                    "value": "rating"
                  },
                  {
                    "label": "Multiple Radio",
                    "value": "multiple_radio"
                  },
                  {
                    "label": "Multiple Checkbox",
                    "value": "multiple_checkbox"
                  }
                ],
                "conditions": [
                  {
                    "label": "In",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "object",
            "availableAggregation": [
              "count",
              "list"
            ]
          },
          {
            "label": "Tags",
            "key": "tags",
            "options": {},
            "filters": [
              {
                "label": "Tags",
                "key": "tag_id",
                "dataType": "number",
                "options": [
                  {
                    "value": 1,
                    "label": "Tag1"
                  },
                  {
                    "value": 2,
                    "label": "Tag2"
                  },
                  {
                    "value": 3,
                    "label": "Tag3"
                  },
                  {
                    "value": 4,
                    "label": "private-form"
                  }
                ],
                "conditions": [
                  {
                    "label": "In",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "object",
            "customUi": {
              "type": "badge",
              "multipleValues": true,
              "separator": "|",
              "valueSeparator": ":"
            },
            "availableAggregation": [
              "count",
              "list"
            ]
          },
          {
            "label": "Notes",
            "key": "notes",
            "options": [],
            "filters": [],
            "dataType": "object",
            "customUi": {
              "isEmojiSupported": true
            },
            "availableAggregation": [
              "count",
              "list"
            ]
          },
          {
            "label": "Business Apps Involved In Case",
            "key": "business_apps",
            "options": {},
            "filters": [
              {
                "label": "Business App",
                "key": "app_id",
                "dataType": "text",
                "options": [
                  {
                    "value": "freshdesk",
                    "label": "Freshdesk"
                  },
                  {
                    "value": "freshservice",
                    "label": "Freshservice"
                  },
                  {
                    "value": "hubspot",
                    "label": "HubSpot"
                  },
                  {
                    "value": "infusionsoft",
                    "label": "Keap (Infusionsoft)"
                  },
                  {
                    "value": "leadsquared",
                    "label": "LeadSquared"
                  },
                  {
                    "value": "microsoft_dynamics_crm",
                    "label": "Microsoft Dynamics CRM"
                  },
                  {
                    "value": "salesforce",
                    "label": "Salesforce"
                  },
                  {
                    "value": "salesforce_sandbox",
                    "label": "Salesforce Sandbox"
                  },
                  {
                    "value": "salesloft",
                    "label": "SalesLoft"
                  },
                  {
                    "value": "sugarcrm",
                    "label": "Sugar CRM"
                  },
                  {
                    "value": "test_app2",
                    "label": "Test app22"
                  },
                  {
                    "value": "with_testing_data",
                    "label": "With Testing data"
                  },
                  {
                    "value": "zendesk",
                    "label": "Zendesk"
                  },
                  {
                    "value": "zoho_crm",
                    "label": "Zoho CRM"
                  },
                  {
                    "value": "zoho_desk",
                    "label": "Zoho Desk"
                  }
                ],
                "conditions": [
                  {
                    "label": "In",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "object",
            "availableAggregation": [
              "count",
              "list"
            ]
          },
          {
            "label": "Social Media Involved In Case",
            "key": "social_apps",
            "options": {},
            "filters": [
              {
                "label": "Social App",
                "key": "app_id",
                "dataType": "text",
                "options": [
                  {
                    "value": "apple_business_chat",
                    "label": "Apple business chat"
                  },
                  {
                    "value": "facebook",
                    "label": "Facebook"
                  },
                  {
                    "value": "line",
                    "label": "Line"
                  },
                  {
                    "value": "skype",
                    "label": "Skype"
                  },
                  {
                    "value": "slack",
                    "label": "Slack"
                  },
                  {
                    "value": "telegram",
                    "label": "Telegram"
                  },
                  {
                    "value": "twitter",
                    "label": "Twitter"
                  },
                  {
                    "value": "viber",
                    "label": "Viber"
                  },
                  {
                    "value": "wechat",
                    "label": "WeChat"
                  },
                  {
                    "value": "whatsapp",
                    "label": "WhatsApp"
                  }
                ],
                "conditions": [
                  {
                    "label": "In",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "object",
            "availableAggregation": [
              "count",
              "list"
            ]
          },
          {
            "label": "Departments Involved",
            "key": "department",
            "options": {},
            "filters": [
              {
                "label": "Department",
                "key": "department_id",
                "dataType": "number",
                "options": [
                  {
                    "value": 1,
                    "label": "Analytics12"
                  },
                  {
                    "value": 2,
                    "label": "Test"
                  },
                  {
                    "value": 3,
                    "label": "aaaa"
                  }
                ],
                "conditions": [
                  {
                    "label": "In",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "object",
            "availableAggregation": [
              "count",
              "list"
            ]
          },
          {
            "label": "Total Calls",
            "key": "totalCalls",
            "filters": [
              {
                "label": "Total Calls",
                "key": "totalCalls",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "avg",
              "list"
            ],
            "aggregationLabel": "Calls"
          },
          {
            "label": "Total Outgoing Calls",
            "key": "totalOutgoingCalls",
            "filters": [
              {
                "label": "Total Outgoing Calls",
                "key": "totalOutgoingCalls",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "avg",
              "list"
            ],
            "aggregationLabel": "Outgoing Calls"
          },
          {
            "label": "Total Incoming Calls",
            "key": "totalIncomingCalls",
            "filters": [
              {
                "label": "Total Incoming Calls",
                "key": "totalIncomingCalls",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "avg",
              "list"
            ],
            "aggregationLabel": "Incoming Calls"
          },
          {
            "label": "Total Missed Calls",
            "key": "totalMissedCalls",
            "filters": [
              {
                "label": "Total Missed Calls",
                "key": "totalMissedCalls",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "avg",
              "list"
            ],
            "aggregationLabel": "Missed Calls"
          },
          {
            "label": "Total Calls Duration",
            "key": "totalDuration",
            "filters": [
              {
                "label": "Total Calls Duration",
                "key": "totalDuration",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "avg",
              "list"
            ],
            "aggregationLabel": "Calls Duration"
          },
          {
            "label": "Total SMS",
            "key": "totalSms",
            "filters": [
              {
                "label": "Total SMS",
                "key": "totalSms",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "avg",
              "list"
            ],
            "aggregationLabel": "SMS"
          },
          {
            "label": "Total Outgoing SMS",
            "key": "totalOutgoingSms",
            "filters": [
              {
                "label": "Total Outgoing SMS",
                "key": "totalOutgoingSms",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "avg",
              "list"
            ],
            "aggregationLabel": "Outgoing SMS"
          },
          {
            "label": "Total Incoming SMS",
            "key": "totalIncomingSms",
            "filters": [
              {
                "label": "Total Incoming SMS",
                "key": "totalIncomingSms",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "avg",
              "list"
            ],
            "aggregationLabel": "Incoming SMS"
          },
          {
            "label": "Total Failed SMS",
            "key": "totalFailedSms",
            "filters": [
              {
                "label": "Total Failed SMS",
                "key": "totalFailedSms",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "avg",
              "list"
            ],
            "aggregationLabel": "Failed SMS"
          },
          {
            "label": "All Custom Attributes",
            "key": "custom_attributes",
            "options": [],
            "filters": [],
            "dataType": "object",
            "availableAggregation": [
              "list"
            ]
          },
          {
            "label": "my custom attribute",
            "key": "my_custom_attribute",
            "filters": [
              {
                "label": "my custom attribute",
                "key": "my_custom_attribute",
                "dataType": "text",
                "options": [],
                "conditions": [
                  {
                    "label": "In",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "list"
            ]
          }
        ]
      },
      {
        "objectName": "Operator",
        "objectKey": "operator",
        "dataSource": [
          {
            "label": "Operator Id",
            "key": "id",
            "options": [],
            "filters": [
              {
                "label": "Operator Id",
                "key": "id",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Is",
                    "key": "is",
                    "supportMultiple": false
                  },
                  {
                    "label": "In",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "number",
            "availableAggregation": [
              "group_by",
              "count",
              "list"
            ]
          },
          {
            "label": "Name",
            "key": "name",
            "options": [],
            "filters": [
              {
                "label": "Name",
                "key": "name",
                "dataType": "text",
                "options": [],
                "conditions": [
                  {
                    "label": "Is",
                    "key": "is",
                    "supportMultiple": false
                  },
                  {
                    "label": "Contains",
                    "key": "like",
                    "supportMultiple": false
                  },
                  {
                    "label": "One of",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "text",
            "availableAggregation": [
              "group_by",
              "count",
              "list"
            ]
          },
          {
            "label": "Email",
            "key": "email",
            "options": [],
            "filters": [
              {
                "label": "Email",
                "key": "email",
                "dataType": "text",
                "options": [],
                "conditions": [
                  {
                    "label": "Is",
                    "key": "is",
                    "supportMultiple": false
                  },
                  {
                    "label": "Contains",
                    "key": "like",
                    "supportMultiple": false
                  },
                  {
                    "label": "One of",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "text",
            "availableAggregation": [
              "group_by",
              "count",
              "list"
            ]
          },
          {
            "label": "Role",
            "key": "role",
            "options": {},
            "filters": [
              {
                "label": "Role",
                "key": "role_id",
                "dataType": "text",
                "options": [
                  {
                    "value": 1,
                    "label": "Administrator"
                  },
                  {
                    "value": 2,
                    "label": "Operator"
                  },
                  {
                    "value": 3,
                    "label": "User"
                  },
                  {
                    "value": 4,
                    "label": "new role"
                  }
                ],
                "conditions": [
                  {
                    "label": "In",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "object",
            "availableAggregation": [
              "group_by",
              "count",
              "list"
            ]
          },
          {
            "label": "Departments",
            "key": "departments",
            "options": {},
            "filters": [
              {
                "label": "Departments",
                "key": "department_id",
                "dataType": "text",
                "options": [
                  {
                    "value": 1,
                    "label": "Analytics12"
                  },
                  {
                    "value": 2,
                    "label": "Test"
                  },
                  {
                    "value": 3,
                    "label": "aaaa"
                  }
                ],
                "conditions": [
                  {
                    "label": "In",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "object",
            "availableAggregation": [
              "group_by",
              "count",
              "list"
            ]
          },
          {
            "label": "Average Response Time",
            "key": "average_response_time",
            "options": [],
            "filters": [
              {
                "label": "Average Response Time",
                "key": "average_response_time",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "dataType": "object",
            "customUi": {
              "duration": true
            },
            "availableAggregation": [
              "sum",
              "avg",
              "list"
            ],
            "aggregationLabel": "Response Time"
          },
          {
            "label": "Average Rating",
            "key": "rating",
            "options": [],
            "filters": [
              {
                "label": "Average Rating",
                "key": "rating",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "avg",
              "list"
            ],
            "aggregationLabel": "Rating"
          },
          {
            "label": "Total Case",
            "key": "total_case",
            "options": [],
            "filters": [
              {
                "label": "Total Case",
                "key": "total_case",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "dataType": "object",
            "availableAggregation": [
              "count",
              "list"
            ],
            "aggregationLabel": "Case"
          },
          {
            "label": "Total Chat",
            "key": "total_chat",
            "options": [],
            "filters": [
              {
                "label": "Total Chat",
                "key": "total_chat",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "dataType": "object",
            "availableAggregation": [
              "count",
              "list"
            ],
            "aggregationLabel": "Chat"
          },
          {
            "label": "Total Mails",
            "key": "totalEmails",
            "filters": [
              {
                "label": "Total Mails",
                "key": "totalEmails",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "list"
            ]
          },
          {
            "label": "Total Sent Mails",
            "key": "totalSentEmails",
            "filters": [
              {
                "label": "Total Sent Mails",
                "key": "totalSentEmails",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "list"
            ]
          },
          {
            "label": "Total Received Mails",
            "key": "totalReceivedEmails",
            "filters": [
              {
                "label": "Total Received Mails",
                "key": "totalReceivedEmails",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "list"
            ]
          },
          {
            "label": "Total of All Calls",
            "key": "total_all_calls",
            "options": [],
            "filters": [
              {
                "label": "Total of All Calls",
                "key": "total_all_calls",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "list"
            ],
            "aggregationLabel": "All Calls"
          },
          {
            "label": "Total Outgoing Calls",
            "key": "outgoing_calls",
            "options": [],
            "filters": [
              {
                "label": "Total Outgoing Calls",
                "key": "outgoing_calls",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "list"
            ],
            "aggregationLabel": "Outgoing Calls"
          },
          {
            "label": "Total Incoming Calls",
            "key": "incoming_calls",
            "options": [],
            "filters": [
              {
                "label": "Total Incoming Calls",
                "key": "incoming_calls",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "list"
            ],
            "aggregationLabel": "Incoming Calls"
          },
          {
            "label": "Total Missed Calls",
            "key": "missed_calls",
            "options": [],
            "filters": [
              {
                "label": "Total Missed Calls",
                "key": "missed_calls",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "list"
            ],
            "aggregationLabel": "Missed Calls"
          },
          {
            "label": "Total Calls Duration",
            "key": "call_duration",
            "options": [],
            "filters": [
              {
                "label": "Total Calls Duration",
                "key": "call_duration",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "dataType": "object",
            "customUi": {
              "duration": true
            },
            "availableAggregation": [
              "sum",
              "list"
            ],
            "aggregationLabel": "Calls Duration"
          },
          {
            "label": "Total of All SMS",
            "key": "total_all_sms",
            "options": [],
            "filters": [
              {
                "label": "Total of All SMS",
                "key": "total_all_sms",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "list"
            ],
            "aggregationLabel": "All SMS"
          },
          {
            "label": "SMS Sent",
            "key": "sms_sent",
            "options": [],
            "filters": [
              {
                "label": "SMS Sent",
                "key": "sms_sent",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "list"
            ],
            "aggregationLabel": "SMS Sent"
          },
          {
            "label": "SMS Received",
            "key": "sms_received",
            "options": [],
            "filters": [
              {
                "label": "SMS Received",
                "key": "sms_received",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "list"
            ],
            "aggregationLabel": "SMS Received"
          },
          {
            "label": "SMS Failed",
            "key": "sms_failed",
            "options": [],
            "filters": [
              {
                "label": "SMS Failed",
                "key": "sms_failed",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "dataType": "object",
            "availableAggregation": [
              "sum",
              "list"
            ],
            "aggregationLabel": "SMS Failed"
          }
        ]
      },
      {
        "objectName": "Contact",
        "objectKey": "contact",
        "dataSource": [
          {
            "label": "Contact Id",
            "key": "id",
            "options": [],
            "filters": [
              {
                "label": "Contact Id",
                "key": "id",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Is",
                    "key": "is",
                    "supportMultiple": false
                  },
                  {
                    "label": "In",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "number",
            "availableAggregation": [
              "list"
            ]
          },
          {
            "label": "Name",
            "key": "name",
            "options": [],
            "filters": [
              {
                "label": "Name",
                "key": "name",
                "dataType": "text",
                "options": [],
                "conditions": [
                  {
                    "label": "Is",
                    "key": "is",
                    "supportMultiple": false
                  },
                  {
                    "label": "Contains",
                    "key": "like",
                    "supportMultiple": false
                  },
                  {
                    "label": "One of",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "text",
            "availableAggregation": [
              "list"
            ]
          },
          {
            "label": "Email",
            "key": "email",
            "options": [],
            "filters": [
              {
                "label": "Email",
                "key": "email",
                "dataType": "text",
                "options": [],
                "conditions": [
                  {
                    "label": "Is",
                    "key": "is",
                    "supportMultiple": false
                  },
                  {
                    "label": "Contains",
                    "key": "like",
                    "supportMultiple": false
                  },
                  {
                    "label": "One of",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "text",
            "availableAggregation": [
              "list"
            ]
          },
          {
            "label": "Phone",
            "key": "phone",
            "options": [],
            "filters": [
              {
                "label": "Phone",
                "key": "phone",
                "dataType": "text",
                "options": [],
                "conditions": [
                  {
                    "label": "Is",
                    "key": "is",
                    "supportMultiple": false
                  },
                  {
                    "label": "In",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "text",
            "availableAggregation": [
              "list"
            ]
          },
          {
            "label": "City",
            "key": "city",
            "options": [],
            "filters": [
              {
                "label": "City",
                "key": "city",
                "dataType": "text",
                "options": [],
                "conditions": [
                  {
                    "label": "In",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "text",
            "availableAggregation": [
              "list"
            ]
          },
          {
            "label": "State",
            "key": "state",
            "options": [],
            "filters": [
              {
                "label": "State",
                "key": "state",
                "dataType": "text",
                "options": [],
                "conditions": [
                  {
                    "label": "In",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "text",
            "availableAggregation": [
              "list"
            ]
          },
          {
            "label": "Custom Attributes",
            "key": "custom_attributes",
            "options": [],
            "filters": [],
            "dataType": "object",
            "availableAggregation": [
              "list"
            ]
          },
          {
            "label": "Company",
            "key": "company",
            "options": [],
            "filters": [],
            "dataType": "object",
            "availableAggregation": [
              "list"
            ]
          },
          {
            "label": "Tags",
            "key": "tags",
            "options": {},
            "filters": [
              {
                "label": "Tags",
                "key": "tags",
                "dataType": "text",
                "options": [
                  {
                    "value": 1,
                    "label": "Tag1"
                  },
                  {
                    "value": 2,
                    "label": "Tag2"
                  },
                  {
                    "value": 3,
                    "label": "Tag3"
                  },
                  {
                    "value": 4,
                    "label": "private-form"
                  }
                ],
                "conditions": [
                  {
                    "label": "In",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "object",
            "customUi": {
              "type": "badge",
              "multipleValues": true,
              "separator": ",",
              "valueSeparator": ":"
            },
            "availableAggregation": [
              "list"
            ]
          },
          {
            "label": "IP",
            "key": "ip",
            "options": [],
            "filters": [
              {
                "label": "IP",
                "key": "ip",
                "dataType": "text",
                "options": [],
                "conditions": [
                  {
                    "label": "Is",
                    "key": "is",
                    "supportMultiple": false
                  },
                  {
                    "label": "In",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "text",
            "availableAggregation": [
              "list"
            ]
          },
          {
            "label": "Browser",
            "key": "client_name",
            "options": [],
            "filters": [
              {
                "label": "Browser",
                "key": "client_name",
                "dataType": "text",
                "options": [],
                "conditions": [
                  {
                    "label": "Is",
                    "key": "is",
                    "supportMultiple": false
                  },
                  {
                    "label": "Contains",
                    "key": "like",
                    "supportMultiple": false
                  },
                  {
                    "label": "One of",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "text",
            "availableAggregation": [
              "list"
            ]
          },
          {
            "label": "OS",
            "key": "client_os_name",
            "options": [],
            "filters": [
              {
                "label": "OS",
                "key": "client_os_name",
                "dataType": "text",
                "options": [],
                "conditions": [
                  {
                    "label": "Is",
                    "key": "is",
                    "supportMultiple": false
                  },
                  {
                    "label": "Contains",
                    "key": "like",
                    "supportMultiple": false
                  },
                  {
                    "label": "One of",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "text",
            "availableAggregation": [
              "list"
            ]
          },
          {
            "label": "Device",
            "key": "client_device_type",
            "options": [],
            "filters": [
              {
                "label": "Device",
                "key": "client_device_type",
                "dataType": "text",
                "options": [],
                "conditions": [
                  {
                    "label": "Is",
                    "key": "is",
                    "supportMultiple": false
                  },
                  {
                    "label": "Contains",
                    "key": "like",
                    "supportMultiple": false
                  },
                  {
                    "label": "One of",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "text",
            "availableAggregation": [
              "list"
            ]
          },
          {
            "label": "Contact Date",
            "key": "date_created",
            "options": [],
            "filters": [
              {
                "label": "Contact Date",
                "key": "date_created",
                "dataType": "datetime",
                "options": [],
                "conditions": [
                  {
                    "label": "Equals",
                    "key": "between",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "datetime",
            "availableAggregation": [
              "list"
            ]
          },
          {
            "label": "Last Contact Date",
            "key": "date_updated",
            "options": [],
            "filters": [
              {
                "label": "Last Contact Date",
                "key": "date_updated",
                "dataType": "datetime",
                "options": [],
                "conditions": [
                  {
                    "label": "Equals",
                    "key": "between",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "datetime",
            "availableAggregation": [
              "list"
            ]
          },
          {
            "label": "Total Cases",
            "key": "total_cases",
            "options": [],
            "filters": [
              {
                "label": "Total Cases",
                "key": "total_cases",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "dataType": "object",
            "availableAggregation": [
              "list"
            ]
          },
          {
            "label": "Total Visits",
            "key": "total_visits",
            "options": [],
            "filters": [
              {
                "label": "Total Visits",
                "key": "total_visits",
                "dataType": "number",
                "options": [],
                "conditions": [
                  {
                    "label": "Between",
                    "key": "between",
                    "supportMultiple": true
                  },
                  {
                    "label": "More Than",
                    "key": "greater_than",
                    "supportMultiple": false
                  },
                  {
                    "label": "Less Than",
                    "key": "less_than",
                    "supportMultiple": false
                  }
                ]
              }
            ],
            "dataType": "object",
            "availableAggregation": [
              "list"
            ]
          },
          {
            "label": "Notes",
            "key": "notes",
            "options": [],
            "filters": [],
            "dataType": "object",
            "customUi": {
              "isEmojiSupported": true
            },
            "availableAggregation": [
              "list"
            ]
          },
          {
            "label": "Business Apps Involved In Contact",
            "key": "business_apps",
            "options": {},
            "filters": [
              {
                "label": "Business App",
                "key": "app_id",
                "dataType": "text",
                "options": [
                  {
                    "value": "freshdesk",
                    "label": "Freshdesk"
                  },
                  {
                    "value": "freshservice",
                    "label": "Freshservice"
                  },
                  {
                    "value": "hubspot",
                    "label": "HubSpot"
                  },
                  {
                    "value": "infusionsoft",
                    "label": "Keap (Infusionsoft)"
                  },
                  {
                    "value": "leadsquared",
                    "label": "LeadSquared"
                  },
                  {
                    "value": "microsoft_dynamics_crm",
                    "label": "Microsoft Dynamics CRM"
                  },
                  {
                    "value": "salesforce",
                    "label": "Salesforce"
                  },
                  {
                    "value": "salesforce_sandbox",
                    "label": "Salesforce Sandbox"
                  },
                  {
                    "value": "salesloft",
                    "label": "SalesLoft"
                  },
                  {
                    "value": "sugarcrm",
                    "label": "Sugar CRM"
                  },
                  {
                    "value": "test_app2",
                    "label": "Test app22"
                  },
                  {
                    "value": "with_testing_data",
                    "label": "With Testing data"
                  },
                  {
                    "value": "zendesk",
                    "label": "Zendesk"
                  },
                  {
                    "value": "zoho_crm",
                    "label": "Zoho CRM"
                  },
                  {
                    "value": "zoho_desk",
                    "label": "Zoho Desk"
                  }
                ],
                "conditions": [
                  {
                    "label": "In",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "object",
            "availableAggregation": [
              "list"
            ]
          },
          {
            "label": "Social Media Apps Involved In Contact",
            "key": "social_apps",
            "options": {},
            "filters": [
              {
                "label": "Social App",
                "key": "app_id",
                "dataType": "text",
                "options": [
                  {
                    "value": "apple_business_chat",
                    "label": "Apple business chat"
                  },
                  {
                    "value": "facebook",
                    "label": "Facebook"
                  },
                  {
                    "value": "line",
                    "label": "Line"
                  },
                  {
                    "value": "skype",
                    "label": "Skype"
                  },
                  {
                    "value": "slack",
                    "label": "Slack"
                  },
                  {
                    "value": "telegram",
                    "label": "Telegram"
                  },
                  {
                    "value": "twitter",
                    "label": "Twitter"
                  },
                  {
                    "value": "viber",
                    "label": "Viber"
                  },
                  {
                    "value": "wechat",
                    "label": "WeChat"
                  },
                  {
                    "value": "whatsapp",
                    "label": "WhatsApp"
                  }
                ],
                "conditions": [
                  {
                    "label": "In",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "dataType": "object",
            "availableAggregation": [
              "list"
            ]
          },
          {
            "label": "Address",
            "key": "address",
            "filters": [
              {
                "label": "Address",
                "key": "address",
                "dataType": "text",
                "options": [],
                "conditions": [
                  {
                    "label": "In",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "list"
            ]
          },
          {
            "label": "Contact Dropdown",
            "key": "contact_dropdown",
            "filters": [
              {
                "label": "Contact Dropdown",
                "key": "contact_dropdown",
                "dataType": "text",
                "options": [
                  "First",
                  "Second",
                  "Contact Custom Dropdown Two ?><,./\":;'|}{[]\\+=_-)(*&^%$#@!"
                ],
                "conditions": [
                  {
                    "label": "In",
                    "key": "in",
                    "supportMultiple": true
                  }
                ]
              }
            ],
            "options": [],
            "dataType": "object",
            "availableAggregation": [
              "list"
            ]
          }
        ]
      }
    ]
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



