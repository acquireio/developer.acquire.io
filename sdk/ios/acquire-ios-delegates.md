# Acquire Delegates for iOS

## AcquireIOSupport iOS SDK Delegates

To add listeners provided by AcquireIOSupport SDK, add following line on your class where you want to listen to our SDK events

```text
AcquireIO.support.delegate = self
```

#### ConnectionStatusChange

This method will be called by SDK when connection status will change. The details of status that was updated during the connection will be available in the argument.

```text
func didChangeConnectionStatus(status: AcquireIOConnectionStatus)
```

AcquireIOConnectionStatus - Connection session status

```text
public enum AcquireIOConnectionStatus : Int {
    /// App support session connection status not connected.
    case notConnected = 0
    /// App support session connection status disconnected.
    case disconnected
    /// App support session connection status connecting.
    case connecting
    /// App support session connection status connected.
    case connected
    /// App support session connection status started.
    case sessionStarted
}
```

Once connection is established with Acquire server, the delegate will receive either didChangeConnectionStatus: or onError:.

#### onError

This function will provide connection related error i.e. invalid input data, expire data etc. To get more details about the error encountered while establishing connection, Implement below delegate method

```text
func onError(error: Error)
```

#### onCallSupportStatusChange

When status of Audio/Video call with Agent changes SDK will call below method. The details of call status that was updated during the connection will be available in the arguments along with the optional message string. To get the call connection status, use

```text
func onCallSupportStatusChange(_ status: AcquireIOCallSupportStatus, withMessage message: String?)
```

AcquireIOCallSupportStatus - Call status

```text
public enum AcquireIOCallSupportStatus : Int {
    case notConnected
    case disconnected
    case connecting
    case connected
}
```

#### onAgentConnected

This will be called when agent is connected.

```text
func onAgentConnected()
```

#### didChangeAgentStatus

This optional method will be called by SDK when Agent status changes. The details of agent `status` that was updated during the connection will be available in the argument along with `Agent ID`.

```text
func didChangeAgentStatus(agentID: String, andStatus status: AcquireIOAgentStatus)
```

AcquireIOAgentStatus - Status for the agent.

```text
public enum AcquireIOAgentStatus : Int {
    /// Online status for agent.
    case online = 0
    /// Offline status for agent.
    case offline
    /// Invisible status for agent.
    case invisible
}
```

#### didUserInteracted

This will be called when user interacts with events.

```text
func didUserInteracted(withEvent type: AcquireIOInteractionEventType, withData data: [String : Any]?)
```

Event Types available are listed below:

```text
public enum AcquireIOInteractionEventType : Int {
    case audioCallStarted = 0
    case videoCallStarted
    case audioCallAnswered
    case videoCallAnswered
    case callDeclined
    case callAutoDeclined
    case callerViewMinimize
    case callerViewMaximize
    case callerViewCameraSwitchToFront
    case callerViewCameraSwitchToBack
    case callSpeakerOn //10
    case callSpeakerOff
    case callMute
    case callUnmute
    case callVideoOn
    case callVideoOff
    case callDisconnected
    case conversationStart
    case conversationEnd
    case conversationFeedbackSubmit
}
```

> Note: For Lite version, only following events will be received

1. conversationStart
2. conversationEnd
3. conversationFeedbackSubmit

#### didReceiveTriggerEvent

This optional method will be called when fire rule matched for created Triggers from the agent panel. It will receive `eventName` as parameter

```text
func didReceiveTriggerEvent(_ eventName: String)
```

#### openAcquireSupport

This optional method will be called when support view controller is open.

```text
func didOpenAcquireSupport()
```

#### hideSupport

This optional method will be called when support view controller is dismissed.

```text
func hideSupport()
```



#### didReceiveNewMessage

This optional method will be called by SDK when a new message has been received. The details of the message received will be available in the argument.

```text
func didReceiveNewMessage(_ message: Any)
```

