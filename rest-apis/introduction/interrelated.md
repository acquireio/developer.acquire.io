# Request Types, Permissions, Errors, & Limits

### CREATING REQUESTS

According to RESTful structure, Acquire implements the following HTTP verbs:  
  
`GET -` Read entity  
`POST -` Create new entity  
`PUT -` Modify existing entity  
`DELETE -` Remove entity

## PERMISSIONS

To request any API endpoint, you will need a valid API key with the related access permissions.

Learn more about obtaining an API key and access permissions in the [Authorization](https://developer.acquire.io/rest-apis/authorization) section. 

## Errors <a id="errors"></a>

Errors are returned using standard HTTP error codes.

In general, the list of error codes includes:  


| Code | Explanation |
| :--- | :--- |
| 2xx | Success |
| 4xx | Bad request sent to the server |
| 5xx | Server-side error |

### STATUS CODES

`200 OK` Successful request.  
`400 Bad Request` Returns JSON with the error message.  
`401 Unauthorized` Couldn’t authenticate your request.  
`403 Forbidden` Invalid request.  
`404 Not Found` No such object.  
`500 Internal Server Error` Something went wrong.  
`503 Service Unavailable` Service is down for maintenance.

| Types | Code | Explanation |
| :--- | :--- | :--- |
| `ERROR_INVALID_INPUT` | 400 | Invalid request |
| `ERROR_RECORD_NOT_FOUND` | 400 | No credentials in the request body |
| `ERROR_DUPLICATE_RECORD_FOUND` | 400 | Already exists |
| `ERROR_UNAUTHORIZED` | 401 | Missing, incorrect, or invalid API Key |
| `ERROR_UNAUTHORIZED_ACCESS` | 403 | Invalid request |
| `ERROR_SERVER_ERROR` | 500 | Internal server error |

## API Limit <a id="api-limit"></a>

There are no API consumption limits.

