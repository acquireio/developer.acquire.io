# Co browsing

Acquire live chat dashboard gives your team leader an overview of agent activity at any given time.

#### **Co browsing**

![](../../.gitbook/assets/image%20%281%29.png)

| Parameter | Value |
| :--- | :--- |
| **Path** | https://app.acquire.io/api/analytics/general/chat-statistics |
| **Method** | POST |
| **Authorization** | Bearer \[YOUR\_API\_AUTH\_TOKEN\] |
| **Content-type** | application/x-www-form-urlencoded |

**Body**

| Parameter | Value |
| :--- | :--- |
| **timezone** | Europe/London |
| **date\_start** | 2018-08-25 00:00:00 |
| **date\_end** | 2018-09-3 23:59:59 |
| **filter\_type** | today |

**Response JSON**

```javascript
{
    "success": true,
    "error": null,
    "data": {
        "chat_date": [
            "12 AM",
            "01 AM",
            "02 AM",
            "03 AM",
            "04 AM",
            "05 AM",
            "06 AM",
            "07 AM",
            "08 AM",
            "09 AM",
            "10 AM",
            "11 AM",
            "12 PM",
            "01 PM",
            "02 PM",
            "03 PM",
            "04 PM",
            "05 PM",
            "06 PM",
            "07 PM",
            "08 PM",
            "09 PM",
            "10 PM",
            "11 PM"
        ],
        "total_session": [
            0,
            0,
            1,
            0,
            0,
            0,
            1,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0
        ],
        "page_visited": [
            0,
            0,
            1,
            0,
            0,
            0,
            1,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0
        ],
        "average_time": [
            0,
            0,
            10.41,
            0,
            0,
            0,
            0.51,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0
        ],
        "total_time": [
            0,
            0,
            641,
            0,
            0,
            0,
            51,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0
        ]
    }
}
```

