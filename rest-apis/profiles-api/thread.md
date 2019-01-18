# Thread

Acquire live chat dashboard gives your team leader an overview of agent activity at any given time.

Profiles Thread API body parameter in add **lead\_id**, **per\_page**, **chatid** and **visitor\_id**

#### **Profiles Thread**

| Parameter | Value |
| :--- | :--- |
| **Path** | https://app.acquire.io/api/profile/message/thread |
| **Method** | POST |
| **Authorization** | Bearer **\[YOUR\_API\_AUTH\_TOKEN\]** |
| **Content-type** | application/json |

#### **Body \(form-data\)**

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
                "chat_id": 197849,
                "thread_id": 40544,
                "visitor_id": 86602,
                "thread_status": "open",
                "chat_updated": null,
                "chat_created": null,
                "chat_duration": 36,
                "chat_wait_time": 3,
                "count_chat": 1,
                "users": null,
                "user_id": null,
                "agents": null,
                "agent_imgs": null,
                "recording_available": null,
                "feedback_rating": null,
                "feedback_message": null,
                "message": "",
                "message_date": null,
                "unseen_count": 0,
                "co_browse": 0,
                "offline_chat": 1,
                "encrypt_key": []
            },
            {
                "chat_id": 197858,
                "thread_id": 40545,
                "visitor_id": 86602,
                "thread_status": "open",
                "chat_updated": null,
                "chat_created": null,
                "chat_duration": 36,
                "chat_wait_time": 3,
                "count_chat": 3,
                "users": "agent-15416",
                "user_id": "15416",
                "agents": "David Klok",
                "agent_imgs": [
                    "pp15337107338831.png"
                ],
                "recording_available": null,
                "feedback_rating": null,
                "feedback_message": null,
                "message": "",
                "message_date": null,
                "unseen_count": 0,
                "co_browse": 3,
                "offline_chat": 0,
                "encrypt_key": []
            }
        ],
        "overall_threads_time": 0.155,
        "activity": []
    }
}
```

