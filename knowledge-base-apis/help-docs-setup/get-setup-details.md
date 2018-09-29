# Get Setup Details

#### **Knowledge Base Setup**

Acquire Knowledge Base Setup api in your help docs setup in required data available. This data use and you make your own help docs easily.

| Parameter | Type |
| :--- | :--- |
| **`Path`** | [https://app.acquire.io/chatbot/api/kb-setup](https://app.acquire.io/chatbot/api/kb-setup) |
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
        "id": 2,
        "account_id": 15,
        "name": "Acquire Help Documentation",
        "tagline": "We are encouraging people to deliver outstanding solutions with great experiences.",
        "top_button": "Try For Free",
        "app_login_url": "https://app.acquire.io/",
        "default_help_url": "acquire",
        "custom_help_url": "https://docs.acquire.io",
        "homepage_link": "https://acquire.io",
        "track_id": "116388650-1",
        "custom_nav": "[{\"name\":\"Home\",\"url\":\"https://acquire.io/\"}]",
        "favicon_img": "https://media.acquire.io/knowledgebase-setup/kb15254774402851.png",
        "logo_img": "https://media.acquire.io/knowledgebase-setup/kb15254774489461.png",
        "header_img": "https://media.acquire.io/knowledgebase-setup/",
        "color_code": "#d5e3f9",
        "button_color": "#f8f8f9",
        "social_url": {
            "facebook": "",
            "twitter": "",
            "linkedin": "",
            "copyright": "Copyright © 2018, Acquire Inc.",
            "privacy_policy": "https://acquire.io/privacy-policy/",
            "term_condition": "https://acquire.io/terms-of-service/"
        },
        "uid": "[YOUR_ACCOUNT_ID]"
    }
}
```



