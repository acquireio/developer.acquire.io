# Get FAQ Categories

#### **Knowledge Base faq-categories**

Knowledge Base in added your all faq-categories data available in this API. if you want to get faq-categories data and setup help docs use this API.

| Parameter | Type |
| :--- | :--- |
| **`Path`** | https://app.acquire.io/chatbot/api/faq-categories |
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
    "data": [
        {
            "id": 19,
            "account_id": 15,
            "category": "Getting started",
            "desc": "Just a few clicks and couple of minutes is all that it takes to configure Acquire Live Chat solution on your website.\n",
            "visible_order": 1,
            "uid": "[YOUR_ACCOUNT_ID]"
        },
        {
            "id": 21,
            "account_id": 15,
            "category": "Configure Acquire",
            "desc": "After signup, you need to place few lines of widget code to your website. For the Mobile app, you need to integrate our Mobile SDK. ",
            "visible_order": 3,
            "uid": "[YOUR_ACCOUNT_ID]"
        },
    ]
}
```



