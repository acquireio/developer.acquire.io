# Webhook Format

Each webhook is an HTTP POST request made to the URL that you provide in the web app. The request's POST body contains webhook information in JSON format.

Each webhook contains the following properties:

**Data** - Data contains webhook data related to webhook trigger in JSON format

**Event** - Determine the event associated with the webhook

When your server receives a webhook from Acquire, it should respond with HTTP 200 response. Otherwise, Acquire will retry sending the webhook to your service for 5 more times unless it receives the correct HTTP 200 response.

Note: Acquire webhooks are sent with Content-Type: application/JSON header, so please make sure that your service can handle such requests.

All selected events you get on your web and webhook data method using **POST** \(**REQUEST**\) or data type **JSON** format.

 **Example Webhook**

```javascript
{
        "id":58624,
        "message":{
            "type":"message",
            "msg":"Hii",
            "user":{
                "id":15416,
                "type":"agent",
                "name":"Jaisaram",
                "photo":null
            },
        },
        "event":"CHAT_ON_MESSAGE"
    }
```

 **Example Integrations**

Here are some ideas for using Acquire webhooks:

Read additional information about your visitors from your database and send it back to the Acquire app, display a warning message on your internal status board when your website visitors start queuing before the chat, save each chat transcript in the external system.

