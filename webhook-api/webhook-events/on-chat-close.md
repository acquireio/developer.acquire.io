# On Chat Close

On chat close, you want to know the chat duration and wait time for chat, which you can use to estimate the chat seats you needed with changing demands to your business to serve your customer better and more quickly.

This trigger will send this data to your server as JSON.

**Example Webhook**

```javascript
{
	"id":"104111",
	"thread_id":"-1",
	"account_id":"10111",
	"session_id":"61111",
	"room_id":"9395a......",
	"visitor_id":"61111",
	"type":"text",
	"comments":"[]",
	"chat_notes":"{}",
	"chat_wait_time":"2",
	"chat_duration":"25",
	"status":"active",
	"translate_to":"en",
	"account_translate_language":"",
	"translate_form_show":"false",
	"date_created":"2018-07-23 05:17:40",
	"date_updated":"2018-07-23 05:17:40",
	"department_id":"",
	"past_comment":"[]",
	"past_chat":"[]",
	"translation_mode":"false",
	"users":"{
		"agent":{
			"name":"John Deo",
			"email":"johndeo@acquire.io",
			"photo":null,
			"role":"Administrator",
			"clients":{
				"agent-15111-web-1":{
					"name":"web",
					"online":true
					}
				}
			},
		"visitor":{
			"name":"David Klok",
			"email":"",
			"phone":"",
			"remarks":"",
			"meta":"_by:app",
			"fields":{},
			"tags":{},
			"custom_fields":[]
		}
	}",
	"by":"agent-15111",
	"ahead_chats":"0",
	"ahead_time":"0",
	"date_picked":"2018-07-23 05:17:42",
	"event":"CHAT_ON_CLOSE"
}
```

