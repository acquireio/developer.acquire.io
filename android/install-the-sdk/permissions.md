# Permissions

### Permissions Description

We include the INTERNET permission by default as we need it to make network requests :

```java
<uses-permission android:name="android.permission.INTERNET"/>
```

 In the AndroidManifest.xml file.

### Run-time permissions

* To make Audio/Video calls camera and record audio permissions are needed so it will ask in marshmallow and above devices. Before marshmallow it is granted by default as mentioned in **AndroidManifest**.

```java
<uses-permission android:name="android.permission.CAMERA" /> 
<uses-permission android:name="android.permission.RECORD_AUDIO" />
```

 audio/video calls will not work if denied these permissions.

* To share attachments from device Read and Write External Storage permissions are needed so it will ask in marshmallow and above devices. Before marshmallow it is granted by default as mentioned in AndroidManifest.

```java
<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />
 <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE"/>
```



User will be unable to share attachment if these permissions are not granted.

**Notes:**

1. For release apk if you want to give support to arm-v7 ABI only then use "'**`com.acquireio.sdk:core-arm-v7a:1.+`**'" instead of "'**`com.acquireio.sdk:core:1.+`**'". to reduce apk size.
2. If you are using gradle Plugin version 3.0 then use implementation instead of compile.
3. You can get instance of sdk anywhere in your app. To get instance of the sdk anywhere in the app call the method **`AcquireApp.getInstance();`** This will return AcquireApp object only if sdk initialized before.
4. Use only AppCompat Theme when you want to use my sdk.

```text

```



