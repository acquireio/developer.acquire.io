# On Chat Accept

On chat accept, you want to get chat status, chat wait time, and visitor details which you can use to keep a repository of chat at your server.

This trigger send **JSON** data to your web server, as show following.

 **Example Webhook**

```javascript
{
        "id":"32654",
        "status":"active",
        "chat_wait_time":"null",
        "user":{
            "id":"agent-12345",
            "status":"active",
            "type":"agent",
            "virtual":false,
            "owner":true,
            "photo":null,
            "state":"online",
            "id_real":15416,
            "name":"John Deo"
        },
        "event":"CHAT_ON_ACCEPT"
    }
```



