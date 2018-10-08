# Latest SDK Integration Guide

## **Now with v1.2 you can integrate our sdk with few clicks!!!**

#### **What’s New in 1.2 :**

1. Chat widget will be added throughout your app without any hassle.
2. Whole chat module integration with only few steps.
3. Chat widget customization and ability to turn it off whenever needed.

## **Steps to integrate Acquire sdk are as follows**

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
implementation 'com.android.support:appcompat-v7:28.0.0' // if not added already
implementation 'com.android.support:design:28.0.0' // if not added already
implementation 'com.android.support:support-emoji-appcompat:28.0.0' // if not added already
implementation ('io.socket:socket.io-client:1.0.0') {
   exclude group: 'org.json', module: 'json'
}
implementation 'com.acquireio:core:1.+' 
}
```

For more info : [click here](https://developer.acquire.io/android/install-the-sdk/integration-sdk)

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

For more info about init method [click here](https://developer.acquire.io/android/install-the-sdk/initialization). 

To handle events manually [click here](https://developer.acquire.io/android/install-the-sdk/acquire-chat-start). 

To remove widget call our SDK  method **`removeFAB();`** 

To Customize our widget click here.

