# Get Categorized Articles

#### **Knowledge Base** Get Categorized Articles **API**

Knowledge Base Get Categorized Articles API in you can show data records searching by Category Title and manage easily Categorised  Articles.

| Parameter | Type |
| :--- | :--- |
| **`Path`** | https://app.acquire.io/chatbot/api/categorized-articles |
| **`Method`** | POST |
| **`Content-type`** | application/x-www-form-urlencoded |

####  **Body\(urlencoded\)**

| Parameter | Type |
| :--- | :--- |
| **`account_id`** | \[YOUR\_ACCOUNT\_ID\] |
| **`cat_title`** | \[Category Title\] |

####  **Response JSON Format**

```javascript
{
    "success": true,
    "error": null,
    "data": {
        "Integrations": {
            "id": 617,
            "account_id": 15,
            "category": "Integrations",
            "desc": "A list of all Third-Party Integrations that Acquire supports and a guide on to set them up for success. ",
            "visible_order": 10,
            "uid": "5d03c",
            "articles": [
                {
                    "article_id": 964446,
                    "chatbot_category_id": 617,
                    "type": "live",
                    "publish_on": "knowledge_base",
                    "slug": "calendly",
                    "article_title": "Calendly",
                    "about": ""
                },
                {
                    "article_id": 966010,
                    "chatbot_category_id": 617,
                    "type": "live",
                    "publish_on": "knowledge_base",
                    "slug": "google-tag-manager",
                    "article_title": "Google Tag Manager",
                    "about": "Configure tags via web-based user interface with the help of Google Tag Manager."
                },
            ]
        }
    }
}
```

