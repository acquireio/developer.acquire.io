---
description: >-
  To start using AcquireIO in your project, add one of the following lines to
  your Podfile according to the version which you wish to integrate.
---

# Getting Start iOS

## Integration using Cocoapods

```objectivec
pod 'AcquireIO'            # For normal version
```

And run `pod install` or `pod update` to refresh your [cocoapods](https://cocoapods.org/) dependencies.

## Manual Integration

### Get the latest SDK zip

Download the latest for the AcquireIO iOS SDK.

### [`Download SDK v2.0.0`](https://devtools.acquire.io/sdk/ios/2.0.0/acquireIO.zip)

The zip file `AcquireIO.framework` contains

{% embed url="https://www.youtube.com/watch?v=45bhaS4iUq4" %}

### Add the latest stable SDK

**Add the latest stable SDK release to your project**

* Unzip the SDK & drag-drop `acquireIO.framework` files into your Xcode project.
* In `Build Phases`, verify that `AcquireIO.framework` is in the `Link Binary with Libraries` and the AcquireIO resources are in `Copy Bundle Resources`
* Add the following frameworks to `Link Binary with Libraries` -
  * `CoreFoundation`
  * `CoreGraphics`
  * `QuartzCore`
  * `UIKit`

{% hint style="info" %}
**Explanation**: The AcquireIO SDK uses background mode `Audio` for when you are video/voice call to agent/visitor. If you have not enable then background voice will not work. When the `UIBackgroundModes` key contains the `audio` value, the system’s media frameworks automatically prevent the corresponding app from being suspended when it moves to the background. Go to `Project/Targets -> Capabilities -> Background Modes -> Audio, AirPlay (Check)`
{% endhint %}

For xcode 8 or later:

1. Go to Project/Targets -&gt; \[Project Name\] -&gt; Build Settings.
2. search `"ALWAYS_EMBED_SWIFT_STANDARD_LIBRARIES"`
3. click the right of Debug, and selected `'Other'`, input `"$(inherited)"`
4. do same with 'Release' and install your pod

In iOS 10, Before you access privacy-sensitive data like Camera, Microphone, and so on, you must ask for the authorization, or your app will crash when you access them.

Open the file in your project named `info.plist`, right click it, opening as Source Code, paste this code below to it. Or you can open `info.plist` as `Property List` by default, click the add button, Xcode will give you the suggest completions while typing Privacy - with the help of keyboard and

Remember to write your description why you ask for this authorization, between `<string>` and `</string>`, or your app will be rejected by apple:

```markup
<!-- Allow Camera -->
<key>NSCameraUsageDescription</key>
<string>$(PRODUCT_NAME) use camera for video chat</string>

<!-- Allow Microphone -->
<key>NSMicrophoneUsageDescription</key>
<string>$(PRODUCT_NAME) use microphone for voice chat</string>

<!-- Allow Photo Library -->
<key>NSPhotoLibraryUsageDescription</key>
<string>$(PRODUCT_NAME) send photo/video to agent</string>
```

