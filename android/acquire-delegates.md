# Acquire Delegates

### Session Delegates 

#### To set session listener call sdk method :

```java
AcquireApp.getInstance().setSessionListner(this);
```

1. **`onSessionConnected();`** executed when socket connection is established. One can open chat module after this event.
2. **`onSessionDisconnected(String reason);`** executed when socket connection is closed and chat is no longer available. ‘reason’ will give the reason for disconnection of the socket.
3. **`onAgentOnline();`** executed when agent becomes online. Use only if required.
4. **`onAgentOffline();`** executed when agent becomes offline. Use only if required.
5. **`onAgentAvailable();`** executed when agent is available to chat. Use only if required.
6. **`onCallConnected(CallType callType);`** executed when direct Video/Audio call is connected to the agent. Use only if required.
7. **`onCallDIsconnected(CallType callType);`** executed when direct Video/Audio call is disconnected. Use only if required.
8. **`callDisconnectWithReason(String reason);`** executed when direct Audio/Video call is disconnected automatically.
9. **`onTriggerEvent(String eventName);`** executed when a custom trigger event has been set and clicked.
10. **`onChatClosed();`** executed when agent closes the chat. Use only if required.
11. **`onChatWidgetClose();`**  executed when user closes the chat screen. Use only if required.
12. **`onTagChange(List list);`** executed whenever tag is changed from agent.
13. **`noAgentAvailable();`** executed when no agent is available.
14. **`onWaitDialogAppear();`**executed when visitor sends a call request.
15. **`onWaitDialogDisappear();`** executed when agent accepts call request.

### Co-Browse Event Delegates

#### To set co-browse event listener call sdk method :

```java
AcquireApp.getInstance().setCoBrowseSessionListner(this);
```

1.**`onCoBrowseConnect(String s)`** : Will be invoked when co browse session is connected and also you can get random id from its argument.

3.**`onAgentConnected()`** : This is invoked when agent start connection by entering same random id which user has got.  

4.**`onCoBrowseDisconnect(String name)`** : this method is invoked when co browsing session is disconnected. Also it will tell you who \(agent/user\) has disconnected the session.

5. **`onCoBrowseFailed()`** : will be invoked when socket connection fails to connect.

6.**`onCoBrowseError()`** : will be invoked when socket gives any error while running session.

