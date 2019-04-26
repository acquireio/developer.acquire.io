# Profile Add Update

Profile Add Update API header parameter in Content-Type application/x-www-form-urlencoded and body in Form data send.

| Parameter | Value |
| :--- | :--- |
| **Path** | https://app.acquire.io/api/profile/lead/add-update |
| **Method** | POST |
| **Authorization** | Bearer **\[YOUR\_API\_AUTH\_TOKEN\]** |
| **Content-type** | application/x-www-form-urlencoded |

**Body**\(Formdata\)

| Parameter | Value |
| :--- | :--- |
| **name** | NewCusomer |
| **email** | email@email.com |
| **phone** | 9876543210 |
| **remarks** | No remarsk |
| **tags** | 73,74 |
| **address** | San Francisco, California, United States |
| **chat\_id** | 1002 |
| **visitor\_id** | 186 |
| **\[extra\_field\]\[text-1526537305797\]text-1526537305797** | Acquire |
| **\[extra\_field\]\[select-1526537321619\]select-1526537321619** | option-2 |
| **\[extra\_field\]\[textarea-1531911230782\]textarea-1531911230782** | No description |

**Response JSON Format**

```javascript

{
    "success": true,
    "error": null,
    "data": "New Record Successfully Added"
}
```

