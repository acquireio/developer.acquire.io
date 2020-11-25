# Acquire Delegates

### Session Delegates 

#### To set session listener call sdk method :

```java
AcquireApp.getInstance().setSessionListner(this);
```

1. **`onSessionConnected()`** executed when socket connection is established. One can open chat module after this event.
2. **`onSessionDisconnected(String reason)`** executed when socket connection is closed and chat is no longer available. ‘reason’ will give the reason for disconnection of the socket.
3. **`onAgentAvailable()`** executed when agent is available to chat. Use only if required.
4. **`onCallConnected()`** executed when direct Video/Audio call is connected to the agent. Use only if required.
5. **`onCallDIsconnected()`** executed when direct Video/Audio call is disconnected. Use only if required.
6. **`onTriggerEvent(String eventName)`** executed when a custom trigger event has been set and clicked.
7. **`onChatClosed()`** executed when agent closes the chat. Use only if required.
8. **`noAgentAvailable();`** executed when no agent is available.
9. **`onWaitDialogAppear();`**executed when visitor sends a call request.
10. **`onWaitDialogDisappear();`** executed when agent accepts call request.

