# Message

Acquire live chat dashboard gives your team leader an overview of agent activity at any given time.

Profile Message API in header parameter Authorization: Bearer \[YOUR\_API\_AUTH\_TOKEN\], Content-Type : application/x-www-form-urlencoded and body parameter in thread\_id, visitor\_id, last\_chat\_id and key send.

| Parameter | Value |
| :--- | :--- |
| **Path** | https://app.acquire.io/api/profile/lead/message |
| **Method** | POST |
| **Authorization** | Bearer **\[YOUR\_API\_AUTH\_TOKEN\]** |
| **Content-type** | application/x-www-form-urlencoded |
| **zone** | {"timezone":"Central/Alabama","offset":"-05:00"} |

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
    "data": {
        "messages": [
            {
                "id": 944199,
                "chat_id": 106241,
                "account_id": 10719,
                "sender_type": "agent",
                "sender_id": 15416,
                "type": "message",
                "message": "Hello",
                "date_created": "2018-07-23 13:45:50",
                "seen": "seen",
                "email_from": null,
                "from": null,
                "to": null,
                "subject": null,
                "body": null,
                "cm_type": null,
                "message_date": null,
                "first_name": "Devid Klok",
                "last_name": "",
                "photo": "pp15337107338831.png",
                "vd_name": "John Deo",
                "vd_id": 61793,
                "bot_name": null,
                "bot_icon": null,
                "parent_bot_name": null,
                "parent_bot_icon": null,
                "offline_chat": 0,
                "user": {
                    "id": null,
                    "type": "agent",
                    "name": "Devid Klok",
                    "photo": "pp15337107338831.png"
                },
                "missed_chat": 0
            },
            {
                "id": 944201,
                "chat_id": 106241,
                "account_id": 10719,
                "sender_type": "visitor",
                "sender_id": 61793,
                "type": "message",
                "message": "Hello",
                "date_created": "2018-07-23 13:45:56",
                "seen": "seen",
                "email_from": null,
                "from": null,
                "to": null,
                "subject": null,
                "body": null,
                "cm_type": null,
                "message_date": null,
                "first_name": null,
                "last_name": null,
                "photo": null,
                "vd_name": "John Deo",
                "vd_id": 61793,
                "bot_name": null,
                "bot_icon": null,
                "parent_bot_name": null,
                "parent_bot_icon": null,
                "offline_chat": 0,
                "user": {
                    "id": null,
                    "type": "visitor",
                    "name": "John Deo",
                    "photo": null
                },
                "missed_chat": 0
            }
        ],
        "co_browse": [],
        "recording": [
            "Welcome"
        ],
        "query_seen": 0
    }
}
```

