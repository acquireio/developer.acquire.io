# Update

Acquire Agent Update API in you can do update your agents details. This API in you can not update Email address.

#### **How to get id** 

if you create own dashboard then first use agents **list** API and get **`id`** for update API parameter.

| Parameter | Value |
| :--- | :--- |
| Path | https://app.acquire.io/account/agents/update |
| Method | POST |
| Authorization | Bearer **`[YOUR_API_AUTH_TOKEN]`** |
| Content-type | application/x-www-form-urlencoded |

#### **Body \(urlencoded\)**

| Parameter | Value |
| :--- | :--- |
| id |  5128  \( user**`id`**\) |
| role | 1/2 \(**`Administrator`** = 1 AND **`Operator`** = 2\) |
| name | david Klok |
| email | devidklok@acquire.io |
| password | 123456789 |
| status | active/disable |

#### Response JSON

```javascript
{
    "success": true,
    "error": null,
    "data": "Agent updated successfully"
}
```

