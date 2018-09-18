# SDK Configuration Example

### Swift Example

```swift
import AcquireIO

func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplicationLaunchOptionsKey: Any]?) -> Bool {
    ...
    let option: NSDictionary = []

    let config = AcquireIOConfig.config()
    config.setDict(option as! [AnyHashable : Any])

    AcquireIO.support().setAccount("<YOUR_ACCOUNT_UID>", withOptions: config)
    ...
    
    return true
}
```

#### Use in Controller {#use-in-controller}

```swift
import AcquireIO

//Call this method to open support view

AcquireIO.support().showSupport(self)
```

### Objective-C Example

```objectivec
#import <AcquireIO/AcquireIO.h>
    
- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions{
    ...
    //Required for init support

    NSDictionary *option = @{};

    AcquireIOConfig *config = [AcquireIOConfig config];
    [config setDict:option];

    [[AcquireIO support] setAccount:@"<YOUR_ACCOUNT_UID>" withOptions:config];
    ...

    return YES;
}
```

#### Use in Controller: {#use-in-controller-}

```objectivec
#import 
    
//Call this method to open support view

[[AcquireIO support] showSupport:self];
```

### Configuration Options Dictionary {#configuration-options-dictionary}

```objectivec
//Objective C
NSDictionary *options = @{@"OptionKey":Value};
```

```swift
//Swift 3.0
let options:NSDictionary = ["OptionKey" : Value]
```

{% hint style="info" %}
Note: These config options optional key.
{% endhint %}

* `UseDefaultTheme` - If you want to use default theme of SDK, even ThemeConfig.plist exist. Default value @NO.
* `ShowAvatar` - If you want to hide avatar image from chat list then use this method. Default value @NO.
* `ScreenShareBorder` - this is optional key. If you want to show red color border when screen share with agent, then use this method. Default value @YES.
* `ShowVideoButton` - Show video button in top tab list on visitor's main chat messages screen and its just hide button but video functionality will not affect by this option. Default value @YES.
* `ShowAudioButton` - Show audio button in top tab list on visitor's main chat messages screen and its just hide button but audio functionality will not affect by this option. Default value @YES.
* `WebSocketServer` - Initialize AcquireIO chat with custom server, Websocket server ip or url to connect support socket server, this is optional, if not set default AcquireIO socket server will connect. Default value AcquireIO server.
* `ShowLocalNotificationBackgroundState` - Show local notification when app is in background state.. Default value @YES.
* `ShowLocalNotificationInApp` - Show in-app notification when app state is active state.. Default value @YES.
* `ButtonImageName` - This is init key for initialize AcquireIO chat with system button bottom right Set image name should be put in main bundle of app. Image size 30x30 px, 60x60 px for @2x. Default value nil.

### Methods {#methods}

* `setAccount: withOptions:` - This is init method for initialize AcquireIO chat. When you calling setAccount method you must pass one accountUID parameter Option can be nil.
* `setVisitorIdentifier:` - Set an visitor identifier for your visitor, can be tracked by admin in remark.
* `setVisitor: phone: andEmail:` - Set the name, phone and email of the app visitor.
* `setVisitorExtraField: fields:` - Set the extra field format: {"l":"FIELD\_LABEL","n":"FIELD\_KEY","v":"FIELD\_VALUE"}.
* `showSupport:` - Show support view controller from current `viewcontroller`, will call after setAccount method done. This method must pass a valid viewController instance.
* `getUnreadCount` - Total unread count of message\(s\).
* `getAvailableAgentCount` - Total unread count of message\(s\).

### Protocol {#protocol}

```text
@Optional
```

* `changeAgentStatus: andStatus:` - When any agent status update. First parameter is agentID and second is status \(AgentStatus enum\).
* `updateUnreadCount` - When receive chat message count will be increase. First parameter is integer count of unread message\(s\).
* `changeConnectionStatus:` Callback when AcquireIO server connection state change. First parameter is status \(ConnectionStatus enum\). Please don't call method for open support view before \`ConnectionStatus\` is \`Connected\`. 
* `hideSupport` When hide acquireIO widget.
* `didReceiveTriggerEvent:` Invoke when you got any event from acquire io trigger.
* `didChangeCobrowseCode:` When change cobrowse code for session.
* `didCobrowseSessionStateChange:` State change for cobrowse session.
* `onCobrowseSessionRequestDecline` SDK ask you to allow cobrowse with agent but you decline. 
* `onCobrowseSessionRequestSucceeded` SDK ask you to allow cobrowse with agent but you accept. 
* `onAgentConnected` Call when connect to cobrowse session
* `onAgentEnded` Call when agent end cobrowse session
* `onSessionFailed` Session failed if any reason
* `onError:` Any error in session with reason.

{% hint style="warning" %}
Note:AcquireIO connection exchanging data asynchronously between app SDK and server. So if you are trying to open `supportViewController` on `ConnectionStatus` is `Connecting` status then it will show message "AcquireIO Error! Session not started yet.".
{% endhint %}
