# Integration Guide \(Core\)

## **Steps to integrate Acquire android-sdk-core are as follows :**

**Step 1 :**

Add the SDK to your project by including the following snippets in the **`build.gradle`** file:

Project level build.gradle :

```javascript
allprojects {
...
    repositories {
   // Add this lines 
        maven {
                url "https://android-sdk.acquire.io/artifactory/libs-release-local/"
        }
    }
...
}

```

Module build.gradle :

```javascript
dependencies {
implementation 'com.android.support:appcompat-v7:27.1.0' // if not added already
implementation 'com.android.support:design:27.1.0' // if not added already
implementation 'com.android.support:support-emoji-appcompat:27.1.0' // if not added already
implementation 'com.android.support:customtabs:27.1.0' // if want to give support for links
implementation ('io.socket:socket.io-client:1.0.0') {
   exclude group: 'org.json', module: 'json'
}
implementation 'pl.droidsonroids.gif:android-gif-drawable:1.2.+'
implementation 'com.amitshekhar.android:android-networking:1.0.2'
implementation 'com.acquireio:core:2.+'
}
```

**Step 2 :**

Initialize Acquire in the **`onCreate()`** method of an Activity where you plan to use the SDK, or an Application subclass. Use the initialization details provided by the Acquire Support admin and an Application instance:

```javascript
public class XYZApp extends Application {
@Override
public void onCreate() {
    super.onCreate();
    AcquireApp.init(this, “put your account id here”);
}
}
```

To know more about initialization options [click here](start-using-acquire.md#initialize-acquire-sdk). 

To handle chat events manually [click here](../acquire-apis.md#chat-apis). 

To customize our chat widget [click here](../custom-ui-widget.md#customize-chat-widget).

To enable our chat widget call **`setShowDefaultFAB(true);`**

To temporarily remove chat widget call**`removeFAB();`**whenever you need.

before initialization of sdk.

{% hint style="info" %}
 To reduce apk size \(e.g. for release version\).

Use **apk split feature of android** 

\*\*\*\*[**https://developer.android.com/studio/build/configure-apk-splits**](https://developer.android.com/studio/build/configure-apk-splits)\*\*\*\*

for reference see below screenshot -&gt;
{% endhint %}

![](../../.gitbook/assets/image%20%281%29.png)

