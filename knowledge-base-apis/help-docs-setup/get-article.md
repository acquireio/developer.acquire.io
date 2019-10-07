# Get Article

**Knowledge Base Get Article**

Knowledge Base Get Article API in you get a single article details using article\_id and account\_id

| Parameter | Type |
| :--- | :--- |
| **`Path`** | https://app.acquire.io/chatbot/api/get-article |
| **`Method`** | POST |
| **`Content-type`** | application/x-www-form-urlencoded |

####  **Body\(urlencoded\)**

| Parameter | Type |
| :--- | :--- |
| **`account_id`** |  \[YOUR\_ACCOUNT\_ID\] |
| **`article_id / url_slug`** |  \[ARTICLE\_ID\] / \[ARTICLE\_SLUG\] |

####  **Response JSON Format**

```javascript
{
    "success": true,
    "error": null,
    "data": {
        "article_id": [ARTICLE_ID],
        "desc_id": 695,
        "question": "General setting",
        "answer": "<p>Here under the general settings, you could explore your way with how chat widget behaves :</p>
					<h6><strong>Chat Routing</strong></h6>
					<p>Here chat routing is working under the “Assigned” mode, so it will assign the incoming chat to the specific agent automatically.</p>
					<p><img src=\"https://media.acquire.io/knowledgebase/kb-img-15247182689431.png\" class=\"fr-fic fr-dii\"></p>
					<p>This could also be changed to Broadcast, here the chat will be broadcasted to number of agents fixed and if no one is able 
					to answer the chat for specific amount of time, it will be broadcasted to next slot of available agents.</p>",
        "chatbot_category_id": "28",
        "account_id": 15,
        "uid": "[YOUR_ACCOUNT_ID]",
        "category": [
            {
                "id": 28,
                "title": "Settings "
            }
        ]
    }
}

```



