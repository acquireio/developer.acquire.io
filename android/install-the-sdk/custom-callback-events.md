# Custom CallBack Events

### Custom CallBack Events

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
12. **`onTagChange(JSONObject tagJsonObject);`** executed whenever tag is changed from agent.

