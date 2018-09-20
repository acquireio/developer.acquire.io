# On Chat Message

On chat message, you want to get chat message, session details and visitor details which you can use to keep a repository of chat at your server.

This trigger send **JSON** data to your web server, as show following.

**Example Webhook**

```javascript
{
	"id":"104111",
	"thread_id":"-1",
	"account_id":"10111",
	"session_id":"61111",
	"room_id":"9395ad5a....",
	"visitor_id":"61111",
	"message":"{
		"type":"message",
		"msg":"sadsdd",
		"user":{
			"id":15111,
			"name":"John",
			"type":"agent",
			"photo":null,
			"state":"online"
			}
	}",
	"recording":"[]",
	"chat_wait_time":"null",
	"chat_duration":"null",
	"translate_to":"en",
	"account_translate_language":"",
	"translate_form_show":"false",
	"date_created":"2018-07-23 05:17:40",
	"date_updated":"2018-07-23 05:17:40",
	"date_picked":"2018-07-23 05:17:42",
	"event":"CHAT_ON_MESSAGE"
}
```

