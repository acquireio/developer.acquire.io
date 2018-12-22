# Get Suggestion

#### **Knowledge Base Get Suggestion API**

Knowledge Base Get Suggestion API in you can show data records searching by user question related article.

| Parameter | Type |
| :--- | :--- |
| **`Path`** | https://app.acquire.io/chatbot/api/get-suggestion |
| **`Method`** | POST |
| **`Content-type`** | application/x-www-form-urlencoded |

####  **Body\(urlencoded\)**

| Parameter | Type |
| :--- | :--- |
| **`account_id`** | \[YOUR\_ACCOUNT\_ID\] |
|  **`search_txt`** | how operating hours can be setup |
|  **`rec_no`** | 2 |

####  **Response JSON Format**

```javascript
{
    "success": true,
    "error": null,
    "data": [
        {
            "article_id": [ARTICLE_ID],
            "question": "Voip (how to buy number, top up, setup, charges)",
            "slug": "voip-how-to-buy-number-top-up-setup-charges",
            "answer": "<p>1. To Call a customer via VoIP you need to click on the people tab and then green call icon......</p>"
        },
        {
            "article_id": [ARTICLE_ID],
            "question": "how chat shortcut works?",
            "slug": "setup-shortcut",
            "answer": "<p>Shortcuts are used during a chat to increase the productivity of agents by filling in the frequently used clauses and sentences...........</p>"
        }
    ]
}

```

