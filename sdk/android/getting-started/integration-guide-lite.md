# Integration Guide \(Lite\)

## **Steps to integrate Acquire android-sdk-lite are as follows :**

**Step 1 :**

Add the SDK to your project by including the following snippets in the **`build.gradle`** file:

Project level **`build.gradle`**:

```javascript
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

Module **`build.gradle`**:

```javascript
dependencies {
    implementation 'io.acquire:lite-beta:1.+'
}
```

If you have added any of this dependency already then try to match the version.

**Step 2 :**

Initialize Acquire in the onCreate\(\) method of an Activity/Application where you plan to use the SDK. Use the initialization details provided by the Acquire Support admin and an Application instance:

```javascript
class XYZApp : Application() {
     override fun onCreate() {
     super.onCreate()
     AcquireApp.init(this, accountID)
   }
}
```

 To get the Demo app clone project from GitHub: [SDKs Guide](https://github.com/acquireio/android-sdk)

To know more about initialization options [click here](). 

To handle chat events manually [click here](../acquire-apis.md#chat-apis). 

To customize our chat widget [click here]().

