---
description: >-
  We recommend installing the acquire.io SDK using Cocoapods. Add this to your
  Podfile:
---

# iOS Cobrowse SDK

## Setup

```objectivec
pod 'AcquireIO-Cobrowse'            # For normal version
```

And run `pod install` or `pod update` to refresh your [cocoapods](https://cocoapods.org/) dependencies.

## Manual Integration

### Get the latest SDK zip

Download the latest for the AcquireIO iOS SDK.

### [`Download SDK Latest`](https://developers.acquire.io/sdk/ios/1.0.9/cobrowse/acquireIO.zip)\`\`

The zip file `AcquireIO.framework` contains

| File | Description |
| :--- | :--- |
| `AcquireIO.h` | AcquireIO main API header file |
| `AcquireIOClient.h` | Support API methods header file |
| `AcquireIO-Swift.h` | AcquireIO swift library for use Socket connection |
| `AcquireIOTheme/` | Folder containing theme configuration to match the design of your app |

### Add the latest stable SDK

**Add the latest stable SDK release to your project**

\*\*\*\*

* Unzip the sdk & drag-drop `acquireIO.framework` files into your Xcode project.
* In `Build Phases`, verify that `AcquireIO.framework` is in the `Link Binary with Libraries` and the AcquireIO resources are in `Copy Bundle Resources`
* Add the following frameworks to `Link Binary with Libraries` -
  * `CoreFoundation`
  * `CoreGraphics`
  * `QuartzCore`
  * `UIKit`

### Example app

There is an example app provided [here](https://github.com/acquireio/acquireio-cobrowse-ios) for both Objective-C and Swift.

Next: [How to configure Acquire SDK in App](sdk-configuration-example.md)

