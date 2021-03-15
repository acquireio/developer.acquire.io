# Interrelated

### STATUS CODES

  
`200 OK` Successful request.  
`400 Bad Request` Returns JSON with the error message.  
`401 Unauthorized` Couldn’t authenticate your request.  
`403 Forbidden` Invalid Request.  
`404 Not Found` No such object.  
`500 Internal Server` Error Something went wrong.  
`503 Service Unavailable` Service is down for maintenance.

### CREATING REQUESTS

  
According to RESTful structure, Acquire implements the following HTTP verbs:  
  
`GET -` Read entity  
`POST -` Create new entity  
`PUT -` Modify existing entity  
`DELETE -` Remove entity  


#### PERMISSIONS <a id="permissions"></a>

To request any API endpoint you will need a valid API key with the access permissions.

## Errors <a id="errors"></a>

Errors are returned using standard HTTP error code.  


In general, the list of error codes:  


| Code | Explanation |
| :--- | :--- |
| 2xx | Success |
| 4xx | Bad request sent to the server |
| 5xx | Server-side error |

| Types | Code | Explanation |
| :--- | :--- | :--- |
| `ERROR_INVALID_INPUT` | 400 | Invalid request |
| `ERROR_RECORD_NOT_FOUND` | 400 | No credentials in the request body |
| `ERROR_DUPLICATE_RECORD_FOUND` | 400 | Already exists |
| `ERROR_UNAUTHORIZED` | 401 | Missing, an incorrectly formatted or invalid API Key |
| `ERROR_UNAUTHORIZED_ACCESS` | 403 | Invalid Request |
| `ERROR_SERVER_ERROR` | 500 | Internal server error |

## API Limit <a id="api-limit"></a>

There are no API consumption limits.

