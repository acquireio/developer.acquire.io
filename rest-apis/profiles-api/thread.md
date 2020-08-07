# Thread

Acquire live chat dashboard gives your team leader an overview of agent activity at any given time.

Profiles Thread API body parameter in add **lead\_id**, **per\_page**, **chatid** and **visitor\_id**

#### **Profiles Thread**

| Parameter | Value |
| :--- | :--- |
| **Path** | https://app.acquire.io/api/profile/message/thread |
| **Method** | POST |
| **Authorization** | Bearer **\[YOUR\_API\_AUTH\_TOKEN\]** |
| **Content-type** | application/x-www-form-urlencoded |
| **zone** | {"timezone":"Pacific/California","offset":"-08:00"} |

#### **Body \(Urlencode\)**

| Parameter | Value |
| :--- | :--- |
| **lead\_id** | 0 |
| **limit** | 20 |
| **chatid** | 197849 |
| **visitor\_id** | 86602 |
| **page** | 1 |

**Response JSON**

```javascript

{
    "success": true,
    "error": null,
    "data": {
        "messages": [
            {
                "chat_id": 1876,
                "thread_id": 445,
                "visitor_id": 565,
                "thread_status": "open",
                "chat_updated": null,
                "chat_created": null,
                "count_chat": 1,
                "chat_ids": "1876",
                "users": "agent-3518",
                "user_id": "3518",
                "agents": "John",
                "agent_imgs": [
                    "pp15402084341544301.png"
                ],
                "recording_available": null,
                "chat_duration": 36,
                "chat_wait_time": 2,
                "feedback_rating": 4,
                "rating": [
                    "4"
                ],
                "rating_time": [
                    "2018-09-20 05:33:30"
                ],
                "feedback_message": "",
                "message": "",
                "message_date": null,
                "unseen_count": 0,
                "cobrowse_recording": "no",
                "offline_chat": 0,
                "recording_available_ids": null,
                "cobrowse_recording_ids": null,
                "encrypt_key": []
            },
            {
                "chat_id": 2142,
                "thread_id": 446,
                "visitor_id": 565,
                "thread_status": "open",
                "chat_updated": null,
                "chat_created": null,
                "count_chat": 5,
                "chat_ids": "1877,2139,2140,2141,2142",
                "users": "agent-3518",
                "user_id": "3518",
                "agents": "John",
                "agent_imgs": [
                    "pp154020815443331101.png"
                ],
                "recording_available": null,
                "chat_duration": 0,
                "chat_wait_time": 126,
                "feedback_rating": null,
                "rating": [
                    "4"
                ],
                "rating_time": [
                    "2018-09-20 05:34:51",
                    "2019-01-16 13:01:47",
                    "2019-01-16 13:02:16",
                    "2019-01-16 13:04:41",
                    "2019-01-17 09:09:23"
                ],
                "feedback_message": null,
                "message": "",
                "message_date": null,
                "unseen_count": 0,
                "cobrowse_recording": "no",
                "offline_chat": 0,
                "recording_available_ids": null,
                "cobrowse_recording_ids": null,
                "encrypt_key": []
            },
            {
                "chat_id": 2146,
                "thread_id": 616,
                "visitor_id": 565,
                "thread_status": "open",
                "chat_updated": null,
                "chat_created": null,
                "count_chat": 3,
                "chat_ids": "2143,2145,2146",
                "users": "agent-3518",
                "user_id": "3518",
                "agents": "John",
                "agent_imgs": [
                    "pp1540208154437632301.png"
                ],
                "recording_available": null,
                "chat_duration": 7132,
                "chat_wait_time": 9,
                "feedback_rating": null,
                "rating": null,
                "rating_time": [
                    "2019-01-17 10:06:24",
                    "2019-01-17 12:07:58",
                    "2019-01-18 09:05:26"
                ],
                "feedback_message": null,
                "message": "",
                "message_date": null,
                "unseen_count": 0,
                "cobrowse_recording": "no",
                "offline_chat": 0,
                "recording_available_ids": null,
                "cobrowse_recording_ids": null,
                "encrypt_key": []
            }
        ],
        "overall_threads_time": 0.042,
        "activity": []
    }
}
```

