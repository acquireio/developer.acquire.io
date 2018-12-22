# Get Recent Article

**Knowledge Base Get Recent Article**

Knowledge Base Get Recent Article API in you get currently added article details. This API Body in account\_id,limit and offset parameter send.

| Parameter | Type |
| :--- | :--- |
| **`Path`** | https://app.acquire.io/chatbot/api/get-recent-articles |
| **`Method`** | POST |
| **`Content-type`** | application/x-www-form-urlencoded |

####  **Body\(urlencoded\)**

| Parameter | Type |
| :--- | :--- |
| **`account_id`** | \[YOUR\_ACCOUNT\_ID\] |
| **`limit`** | 2 |
| **`offset`** | 0 |

####  **Response JSON Format**

```javascript
{
    "success": true,
    "error": null,
    "data": [
        {
            "article_id": [ARTICLE_ID],
            "desc_id": 1336,
            "question": "do you support co browsing?",
            "chatbot_category_id": null,
            "account_id": 15,
            "category": [
                {
                    "id": 22,
                    "title": "Support with Chat (Dashboard)"
                }
            ]
        },
        {
            "article_id": [ARTICLE_ID],
            "desc_id": 680,
            "question": "Email Campaign",
            "chatbot_category_id": "24",
            "account_id": 15,
            "category": [
                {
                    "id": 24,
                    "title": "How to setup campaign"
                }
            ]
        }
    ]
}

```



