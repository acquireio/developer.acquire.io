---
description: learn how to add acquire core SDK with Cocoapods.
---

# Integration Guide \(Core\)

## Initial setup

The steps below use [CocoaPods](https://cocoapods.org/) to integrate the AcquireIO SDK.

For more detail, you can also check out our [generated iOS docs ](https://devtools.acquire.io/sdk/ios/docs/html/index.html)or review the [app store](https://itunes.apple.com/us/app/acquire-support-sdk/id1445674477#?platform=iphone) and source code on [Github](https://github.com/acquireio/acquireio-ios).

## Integration using Cocoapods

```objectivec
pod 'AcquireIO'            # For normal version
```

And run `pod install` or `pod update` to refresh your [cocoapods](https://cocoapods.org/) dependencies.

For issues installing CocoaPods, see [their website](https://cocoapods.org/) for help.

{% hint style="info" %}
**Explanation**: The AcquireIO SDK uses background mode `Audio` for when you are video/voice call to agent/visitor. If you have not enable then background voice will not work. When the `UIBackgroundModes` key contains the `audio` value, the system’s media frameworks automatically prevent the corresponding app from being suspended when it moves to the background. Go to `Project/Targets -> Capabilities -> Background Modes -> Audio, AirPlay (Check)`
{% endhint %}

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

