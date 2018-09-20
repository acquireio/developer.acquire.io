# Acquire Chat Start

### Start chat module directly

Start chat module directly by calling **`startSupportChat();`**

**Method name :** **`startSupportChat()`**:

This method is used to open chat. To use this method **AcquireApp** instance is needed. So use this method after successful initialization.

**Another Method :** **`startSupportChat(AQR_BaseActivity aqrBaseActivity, CallType callType)`**:

* **@param** **`aqrBaseActivity`** - Your Activity which is extended to AQR\_BaseActivity
* **@param** **`callType`** - TEXT, AUDIO, VIDEO

Use this method to start direct Audio/Video calls. By this method , Audio/Video chat request will be visible to the agent and on answer to that chat will start Audio/Video call as soon as chat is connected.

#### **Set session listener:**

**Register your activity by calling `setSessionListner(sessionListner);`**

**Note :** Set the listener manually by calling this method : **`AcquireApp.getInstance().setSessionListner(this);`** to get callbacks to anywhere you require.  For session events usage see here :  [https://developers.acquire.io/custom-callback-events](https://developers.acquire.io/custom-callback-events)

