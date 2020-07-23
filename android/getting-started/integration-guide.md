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
    implementation 'com.acquireio:core:2.+'
    implementation 'com.google.android.material:material:1.1.0'
    implementation 'androidx.appcompat:appcompat:1.1.0'
    implementation 'androidx.emoji:emoji-appcompat:1.0.0'
    implementation 'pl.droidsonroids.gif:android-gif-drawable:1.2.19'
    implementation 'androidx.multidex:multidex:2.0.1'
    implementation 'androidx.browser:browser:1.2.0'
    implementation('io.socket:socket.io-client:1.0.0') {
        exclude group: 'org.json', module: 'json'
    }
    implementation 'com.squareup.picasso:picasso:2.71828'
    implementation 'com.amitshekhar.android:android-networking:1.0.2'
    implementation 'androidx.swiperefreshlayout:swiperefreshlayout:1.0.0'
    implementation 'androidx.lifecycle:lifecycle-extensions:2.2.0'
}
```

{% hint style="info" %}
To get the latest version at every build, use **2.+** instead of a specific number.
{% endhint %}

{% hint style="info" %}
If you have added any of this dependency already then try to match the version.
{% endhint %}

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

To enable our chat widget call**`setShowDefaultFAB(true);`**before initialization of sdk.

 To reduce apk size \(e.g. for release version\).

{% hint style="info" %}
Use **apk split feature of android** 

\*\*\*\*[**https://developer.android.com/studio/build/configure-apk-splits**](https://developer.android.com/studio/build/configure-apk-splits)\*\*\*\*

for reference see below screenshot -&gt;
{% endhint %}

To temporarily remove chat widget call**`removeFAB();`**whenever you need.

![](../../.gitbook/assets/image%20%283%29.png)

