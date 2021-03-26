# React Native

Acquire SDK can be easily integrated into React Native.

You can refer [react-native-doc](https://reactnative.dev/docs/native-modules-android) to use Native components. 

Acquire SDK is the same as any other third party native library 

You will need to add

```text
allprojects {
...
    repositories {
   // Add this lines
        maven {
                url "https://android-sdk.acquire.io/artifactory/libs-release/"
        }
    }
...
}
```

this maven URL to your **project** level gradle.

And add this to your app **Module's** build.gradle

```text
dependencies {
    implementation 'io.acquire:core-twilio-beta:1.+'
}
```

{% hint style="danger" %}
If you want to use the lite version then use the below configuration.
{% endhint %}

```text
dependencies {
    implementation 'io.acquire:lite-beta:1.+'
}
```

Register Acquire SDK in the **onCreate\(\)** method of an Activity/Application where you plan to use the SDK. Use the initialization details provided by the Acquire Support admin and an Application instance:

```text
class XYZApp : Application() {
     override fun onCreate() {
     super.onCreate()
    AcquireApp.registerApp(this)
   }
}
```

Initialize Acquire SDK with **accountID** by using this method. 

{% hint style="warning" %}
This method will connect to the Acquire server in the background.
{% endhint %}

```javascript
AcquireApp.init(accountID)
```

**Permissions**   
We include the **INTERNET** permission by default as we need it to make network requests:

```text
<uses-permission android:name="android.permission.INTERNET"/>
```

Needed below permissions to make audio/video calls.

```text
<uses-permission android:name="android.permission.CAMERA" />
<uses-permission android:name="android.permission.RECORD_AUDIO" />
```

Needed below permissions for attachments to share from the app.

```text
<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
```

{% hint style="success" %}
All the above **permissions** need to be mentioned in your **AndroidManifest** file.
{% endhint %}

You can download our demo react native [source code](https://drive.google.com/file/d/1Ga7vgi5Zg2BKSIDfc9FG-np8j5IqEFRR/view?usp=sharing).

To know more about initialization options [click here](acquire-apis.md). 

To get session events [click here](acquire-delegates.md). 

