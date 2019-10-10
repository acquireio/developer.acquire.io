# Get Side List

#### **Knowledge Base Side List**

Knowledge Base Side List API in all Category and Category under article data in article id ,chatbot\_category\_id, type, publish\_on, slug and article\_title available. You can use this and make own help docs side list.

| Parameter | Type |
| :--- | :--- |
| **`Path`** | https://app.acquire.io/chatbot/api/side-list |
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
                "article_id": 961093,
                "chatbot_category_id": 19,
                "type": "live",
                "publish_on": "knowledge_base",
                "slug": "admin-overview",
                "article_title": "Admin Tabs",
                "about": ""
            },
            {
                "article_id": 2070,
                "chatbot_category_id": 19,
                "type": "live",
                "publish_on": "knowledge_base",
                "slug": "how-to-sign-up",
                "article_title": "Create your Acquire Account",
                "about": "Sign up and get started with Acquire in a few clicks."
            },
        ],
    }
}

```



