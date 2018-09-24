# Tags

Acquire live chat dashboard gives your team leader an overview of agent activity at any given time.

Tagging a chat means that you can add certain labels or tag to a chat that would help you to define what it was all about. Tags helps you in bucketing the chat better, for example a agent can ‘tag’ a conversation as ‘support’ - meaning the customer required support.

Profiles Tags API header parameter in Authorization: Bearer YOUR\_API\_AUTH\_TOKEN, Content-Type application/x-www-form-urlencoded send.

| Parameter | Value |
| :--- | :--- |
| **Path** | https://app.acquire.io/profile/lead/tag-account |
| **Method** | POST |
| **Authorization** | Bearer YOUR\_API\_AUTH\_TOKEN |
| **Content-type** | application/x-www-form-urlencoded |

**Response JSON Format**

```javascript

{
    "success": true,
    "error": null,
    "data": [
        {
            "id": 168205,
            "name": "Ok"
        },
        {
            "id": 168206,
            "name": "New chat"
        },
        {
            "id": 168207,
            "name": "Test"
        },
        {
            "id": 168208,
            "name": "Important"
        }
    ]
}
```

