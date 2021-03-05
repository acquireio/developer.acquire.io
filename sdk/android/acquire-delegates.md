# Acquire Delegates

### Session Delegates 

#### To set session listener call sdk method :

```java
AcquireApp.setSessionListener(this);
```

1. **`onSessionConnected()`** Invokes on socket connection is established. One can open chat module after this event.
2. **`onSessionDisconnected(Reason: String)`** Invokes on socket connection is closed and chat is no longer available. ‘Reason’ will give the reason for the disconnection of the socket.
3. **`onAgentAvailable()`** Invokes on agent becomes available to chat.
4. **`onCallConnected()`** Invokes on direct Video/Audio call is connected to the agent.
5. **`onCallDIsconnected()`** Invokes on direct Video/Audio call is disconnected.
6. **`onTriggerEvent(eventName: String?)`** Invokes on custom trigger event has been set and clicked.
7. **`onChatClosed()`** Invokes on chat is closed by the agent.
8. **`noAgentAvailable();`** Invokes on all Agents become unavailable.
9. **`onWaitDialogAppear();`**Invokes on Audio/Video call is requested by the user \(visitor\).
10. **`onWaitDialogDisappear();`** Invokes on agent answer the call request.

