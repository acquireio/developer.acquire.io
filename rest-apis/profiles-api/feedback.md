# Feedback

Acquire live chat dashboard gives your team leader an overview of agent activity at any given time.

Profiles Feedback API in header parameter Content-Type : application/x-www-form-urlencoded send.

| Parameter | Value |
| :--- | :--- |
| **Path** | https://app.acquire.io/api/profile/lead/feedback |
| **Method** | POST |
| **Authorization** | Bearer **\[YOUR\_API\_AUTH\_TOKEN\]** |
| **Content-type** | application/x-www-form-urlencoded |
| **zone** | {"timezone":"Mountain/Arizona","offset":"-06:00"} |

#### Body

| Parameter | Value |
| :--- | :--- |
|  visitor\_id | 56501 |

#### **Response JSON**

```javascript

{
    "success": true,
    "error": null,
    "data": [
        {
            "id": 214554,
            "account_id": 457412,
            "date_created": "2019-01-17 12:07:58",
            "date_updated": "2019-01-17 12:08:26",
            "feedback_rating": null,
            "feedback_message": null,
            "chat_date_created": null,
            "chat_date_updated": null,
            "user_id": 3518121,
            "agents": "Devid",
            "feedback": []
        }
    ]
}
```

