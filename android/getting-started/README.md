# Getting Started

To know about our **android SDK** , check out our app on Google [play store](https://play.google.com/store/apps/details?id=com.acquire.sdk.app). Its source code is also available on [github](https://github.com/acquireio/acquireio-android).

### Requirements

* Android Studio 2.2+
* Gradle 2.14.1.+
* Android SDK 7.1.+
* Android device running Android 5.0 or newer \(To get fully functioning sdk\)

### Build variants

We are providing two types of build variants :

1. **Core** - Fully featured including Audio/Video calling. [See Integration](https://developer.acquire.io/android/getting-started/integration-guide#steps-to-integrate-acquire-android-sdk-are-as-follows)
2. **Lite** - All features excluding Audio/Video Calling. [See Integration](integration-guide-lite.md#steps-to-integrate-acquire-android-sdk-lite-are-as-follows)

The main difference of these two build variants is the size.

* Our **Core** version is of **18 MB** because of webRTC's archived libraries for all ABIs included.
* If you split apk using [apk splitting feature](https://developer.android.com/studio/build/configure-apk-splits) of android then it consumes around **8 to 10 MB.**
* Our **Lite** version is only **2~3 MB.** 

{% hint style="info" %}
So if you don't require Video calling feature, you can use **lite** version to reduce the apk size.
{% endhint %}

* [Integration Guide \(Core\)](integration-guide.md#steps-to-integrate-acquire-android-sdk-core-are-as-follows)
* [Integration Guide \(Lite\)](integration-guide-lite.md#steps-to-integrate-acquire-android-sdk-lite-are-as-follows)
* [Start using Acquire](start-using-acquire.md#initialize-acquire-sdk)
* [Permissions needed by Acquire SDK](start-using-acquire.md#permissions-description)
* [Acquire Delegates](../acquire-delegates.md)

