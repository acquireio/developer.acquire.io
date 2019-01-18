# Edit / Get-agent

Agent Edit API use for get a particular agent details and agent edit details. If you want to a agent details use this API and setup your dashboard easily.

#### **How to get id** 

if you create own dashboard then first use agents **list** API and get **`id`** for edit API parameter.

| Parameter | Value |
| :--- | :--- |
| Path | https://app.acquire.io/api/account/agents/edit |
| Method | POST |
| Authorization | Bearer **`[YOUR_API_AUTH_TOKEN]`** |
| Content-type | application/x-www-form-urlencoded |

#### **Body \(urlencoded\)**

| Parameter | Value |
| :--- | :--- |
| id |  5128  |

#### Response JSON

```javascript
{
    "success": true,
    "error": null,
    "data": {
        "id": 5128,
        "name": "david",
        "email": "devidklok@acquire.io",
        "status": "active",
        "allowed_ip": "",
        "userId": 3518,
        "accountId": 4574,
        "role": 1,
        "department": "",
        "role": "Administrator"
    }
}
```

