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
    implementation 'com.acquireio:core:3.+'
    implementation "org.jetbrains.kotlin:kotlin-stdlib:1.5.20"
    implementation 'androidx.appcompat:appcompat:1.3.0'
    implementation 'com.google.android.material:material:1.3.0'
    implementation 'androidx.core:core-ktx:1.5.0'
    implementation 'androidx.constraintlayout:constraintlayout:2.0.4'
    implementation "org.jetbrains.kotlinx:kotlinx-coroutines-core:1.4.2"
    implementation "org.jetbrains.kotlinx:kotlinx-coroutines-android:1.4.2"
    implementation 'com.squareup.okhttp3:okhttp:4.9.0'
    api('io.socket:socket.io-client:1.0.1') {
        exclude group: 'org.json', module: 'json'
    }
    implementation 'com.google.code.gson:gson:2.8.6'
    implementation 'com.beust:klaxon:5.0.1'
    implementation 'androidx.lifecycle:lifecycle-extensions:2.2.0'
    implementation "androidx.fragment:fragment-ktx:1.3.5"
    implementation "androidx.room:room-runtime:$room_version"
    kapt "androidx.room:room-compiler:$room_version"
    implementation "androidx.room:room-ktx:$room_version"
    implementation 'org.greenrobot:eventbus:3.2.0'
    implementation 'org.webrtc:google-webrtc:1.0.32006'
    implementation 'com.squareup.picasso:picasso:2.71828'
    api 'androidx.emoji:emoji-appcompat:1.1.0'
    api 'pl.droidsonroids.gif:android-gif-drawable:1.2.20'
    api 'androidx.browser:browser:1.3.0'
}
```

{% hint style="info" %}
If you have added any of this dependency already then try to match the version.
{% endhint %}

**Step 2 :**

Initialize Acquire in the **`onCreate()`** method of an Activity where you plan to use the SDK, or an Application subclass. Use the initialization details provided by the Acquire Support admin and an Application instance:

```javascript
class XYZApp : Application() {
    override fun onCreate() {
        super.onCreate()
        AcquireApp.init(this, “put your account id here”)
    }
}
```

To know more about initialization options [click here](start-using-acquire.md#initialize-acquire-sdk). 

To handle chat events manually [click here](../acquire-apis.md#chat-apis). 

To customize our chat widget [click here](../custom-ui-widget.md#customize-chat-widget).

 To reduce apk size \(e.g. for release version\).

{% hint style="info" %}
Use **apk split feature of android** 

\*\*\*\*[**https://developer.android.com/studio/build/configure-apk-splits**](https://developer.android.com/studio/build/configure-apk-splits)\*\*\*\*

for reference see below screenshot -&gt;
{% endhint %}

![](../../.gitbook/assets/image%20%283%29.png)

