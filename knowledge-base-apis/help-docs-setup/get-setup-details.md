# Get Setup Details

#### **Knowledge Base Setup**

Acquire Knowledge Base Setup api in your help docs setup in required data available. This data use and you make your own help docs easily.

| Parameter | Type |
| :--- | :--- |
| **`Path`** | https://app.acquire.io/chatbot/api/kb-setup |
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
        "name": "Help Center",
        "tagline": "We encourage people to deliver outstanding solutions with great experiences.",
        "top_button": "Get Started Now",
        "app_login_url": "https://app.acquire.io/",
        "get_start_button": "",
        "default_help_url": "https://5d03c.lml.io",
        "custom_help_url": "https://docs.acquire.io",
        "homepage_link": "https://acquire.io",
        "track_id": "116388650-1",
        "custom_nav": "[{\"name\":\"Home\",\"url\":\"https://acquire.io/\"},{\"name\":\"API Reference\",\"url\":\"https://developer.acquire.io/\"},{\"name\":\"Blog\",\"url\":\"https://acquire.io/blog/\"}]",
        "favicon_img": "https://media.acquire.io/knowledgebase-setup/kb15365791379360.png",
        "logo_img": "https://media.acquire.io/knowledgebase-setup/kb15693244899830.png",
        "header_img": "https://media.acquire.io/knowledgebase-setup/kb15693208639251.png",
        "secondary_header_img": "https://media.acquire.io/knowledgebase-setup/default-second-banner-theme1-img.png",
        "color_code": "#d5e3f9",
        "button_color": "#1c59b8",
        "header_script": null,
        "social_url": {
            "facebook": "",
            "twitter": "",
            "linkedin": "",
            "copyright": "© Copyright 2019 Acquire™",
            "privacy_policy": "https://acquire.io/privacy-policy/",
            "term_condition": "https://acquire.io/terms-of-service/"
        },
        "theme_id": 1,
        "uid": "[AccountID]"
    }
}
```



