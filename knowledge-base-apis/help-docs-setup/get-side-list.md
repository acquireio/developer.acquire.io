# Get Side List

#### **Knowledge Base Side List**

Knowledge Base Side List API in all Category and Category under article data in article id ,chatbot\_category\_id, type, publish\_on, slug and article\_title available. You can use this and make own help docs side list.

| Parameter | Type |
| :--- | :--- |
| **`Path`** | [https://app.acquire.io/chatbot/api/side-list](https://app.acquire.io/chatbot/api/side-list) |
| **`Method`** | POST |
| **`Content-type`** | application/x-www-form-urlencoded |

####  **Body\(urlencoded\)**

| Parameter | Type |
| :--- | :--- |
|  **`account_id`** |  \[YOUR\_ACCOUNT\_ID\] |

####  **Response JSON Format**

```javascript
{
    "success": true,
    "error": null,
    "data": {
        "Getting started": [
            {
                "article_id": [ARTICLE_ID],
                "chatbot_category_id": 19,
                "type": "live",
                "publish_on": "knowledge_base",
                "slug": "how-to-sign-up",
                "article_title": "How to sign up"
            },
        ],
        "Configure Acquire": [],
        "How to setup campaign": [
            {
                "article_id": [ARTICLE_ID],
                "chatbot_category_id": 24,
                "type": "live",
                "publish_on": "knowledge_base",
                "slug": "email-campaign",
                "article_title": "Email Campaign"
            }
        ],
    }
}

```



