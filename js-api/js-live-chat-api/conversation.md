# Conversation

## Conversation Start Event

When conversation has started with visitor, initiated by operator or visitor. Handler callback function will get data parameter with conversation data object.

#### Sample Code

```javascript
<script>
	window.acquire = window.acquire || [];
	window.acquire.push(function(app){
		app.on('conversation-start', (function(data){
			console.log('conversation started');
			console.log('conversation data =>', data);
		}));
	});
</script>
```



## Conversation End Event

When conversation has closed by operator. Handler callback function will get parameter with ended conversation id.

#### Sample Code

```javascript
<script>
   window.acquire = window.acquire || [];
   window.acquire.push(function(app){
      app.on('conversation-end', (function(conversation_id){
         console.log('conversation has been closed');
         console.log('conversation id =>', conversation_id);
      }));
   });
</script>
```



