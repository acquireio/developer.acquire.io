# Acquire APIs

### SDK APIs:

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

Use this method to start direct Audio/Video call request to agent. By this method, Audio/Video chat request will be visible to the agent and on answer to that chat will start Audio/Video call as soon as chat is connected.

```text
getVisitorId()
```

Get Visitor ID using this method `AcquireApp.getVisitorId()`

```text
logout()
```

  
Logout will clear the current session and also gives a callback when the process is finished. After logout one has to initialize the SDK again to create a new session. `AcquireApp.logOut { }`  
  
  




