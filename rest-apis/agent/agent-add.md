# Agent add

Agents add API in you can create a new agent in your dashboard. Body parameter in **`"role"`** two types available first **`Administrator`** and second **`Operator`**. if you agent role make Administrator then pass **`1`** else pass **`2`** for Operator.

| Parameter | Value |
| :--- | :--- |
| Path | [https://app.acquire.io/account/agents/add](%20https://app.acquire.io/account/agents/add
) |
| Method | POST |
| Authorization | Bearer **`[YOUR_API_AUTH_TOKEN]`** |
| Content-type | application/x-www-form-urlencoded |

#### **Body \(urlencoded\)**

| Parameter | Value |
| :--- | :--- |
| role | 1/2 \(**`Administrator`** = 1 AND **`Operator`** = 2\) |
| name | david |
| email | devidklok@acquire.io |
| password | 1234567 |
| status | active/disable |

#### Response JSON

```javascript
{
    "success": true,
    "error": null,
    "data": "Agent save successfully."
}
```

