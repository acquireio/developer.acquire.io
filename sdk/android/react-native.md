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

this maven URLto your **project** level gradle.

And add this to your app **Module's** build.gradle

```text
dependencies {
    implementation 'io.acquire:core-twilio-beta:1.+'
}
```

Initialize Acquire SDK in the onCreate\(\) method of an Activity/Application where you plan to use the SDK. Use the initialization details provided by the Acquire Support admin and an Application instance:

```text
class XYZApp : Application() {
     override fun onCreate() {
     super.onCreate()
     AcquireApp.init(this, accountID)
   }
}
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

