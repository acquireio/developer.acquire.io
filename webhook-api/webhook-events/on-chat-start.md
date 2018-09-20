# On Chat Start

#### Webhook Events

In some cases, you may want to get some additional information when the particular event occurs. For example, when the chat starts, you may want to know the visitor's name and e-mail. To get this information, you can parse webhook data send to your server as described following.

#### On Chat Start

On chat start, you want to get data like visitor name, email and phone as provided in pre-chat survey, which can be used to keep record of visitor on website in the format you like. You can also use visitor info to communicate with your visitors after chat is over.

This data is send to your web server as **JSON** provided in the webhook with trigger **ON START** selected at Acquire dashboard.

#### **Example Webhook**

```javascript
{
  "data": {
    " id": 172,
    "details": {
        "name": "John",
        "email": "John@acquire.io",
        "phone": null,
        "remarks": "Test",
        "meta": "_by:agent"
    },
    "status": "pending",
    "date_created": "2017-09-20 10:17:08",
    "date_updated": "2017-09-20 10:17:08",
    "department_id": ""
    },
    "event": "CHAT_ON_START"
}
```

```text

```

