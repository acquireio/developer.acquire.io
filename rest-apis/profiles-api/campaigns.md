# Campaigns

Acquire live chat dashboard gives your team leader an overview of agent activity at any given time.

Acquire Campaigns API body parameter in add thread\_id, visitor\_id, last\_chat\_id and key

| Parameter | Value |
| :--- | :--- |
| **Path** | https://app.acquire.io/api/profile\_campaign/campaigns |
| **Method** | POST |
| **Authorization** | Bearer \[YOUR\_API\_AUTH\_TOKEN\] |
| **Content-type** | application/x-www-form-urlencoded |

**Body**

| Parameter | Value |
| :--- | :--- |
| **thread\_id** | -1 |
| **visitor\_id** | 61793 |
| **last\_chat\_id** | 106241 |
| **key** |  |

**Response JSON**

```javascript

{
    "success": true,
    "error": null,
    "data": [
        {
            "id": 1,
            "name": "Profiles",
            "config": null,
            "account_id": 0,
            "user_id": 0,
            "date_created": null,
            "date_updated": null,
            "is_primary": 1
        }
    ]
}
```

