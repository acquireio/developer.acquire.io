# Acquire SDK APIs

### SDK APIs:

### Initiate Support Chat

Start chat module directly by calling **`startSupportChat()`**

```java
AcquireApp.startSupportChat()
```

This method is used to open chat. To use this method **AcquireApp** instance is needed. So use this method after successful initialization.

**Alternate Method :** **`startDirectSupportChat(callType: CallType)`**

```java
AcquireApp.startDirectSupportChat(CallType.VIDEO)
```

* **@param** **`callType`** - TEXT, AUDIO, VIDEO

Use this method to start direct Audio/Video call request to the agent. By this method, Audio/Video chat request will be visible to the agent and on the answer to that chat will start Audio/Video call as soon as the chat is connected.

### Get Visitor ID

Get Visitor ID using this method 

```text
AcquireApp.getVisitorId()
```

### Logout Visitor

Logout will clear the current session and also gives a callback when the process is finished. After logout one has to initialize the SDK again to create a new session. 

```text
AcquireApp.logOut { }
```



