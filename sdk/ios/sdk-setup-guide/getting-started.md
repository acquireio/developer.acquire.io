# Getting Started

For more detail, you can also check out our [generated iOS docs ](https://devtools.acquire.io/sdk/ios/docs/html/index.html)or review the [app store](https://itunes.apple.com/us/app/acquire-support-sdk/id1445674477#?platform=iphone) and source code on [Github](https://github.com/acquireio/acquireio-ios)

### Requirements

* iOS 8.2+
* XCode 10+

### Build variants

We are providing two types of build variants :

1. **Core** - Fully featured including Audio/Video calling. [See Integration](integration-guide-core.md)
2. **Lite** - All features excluding Audio/Video Calling. [See Integration](integration-guide-lite.md)

The main difference of these two build variants is the size.

* Our **Core** version is of **35.2 MB** because of webRTC's archived libraries for all ABIs included.
* Our **Lite** version is only **13 MB.** 

{% hint style="info" %}
So if you don't require calling feature, you can use **lite** version to reduce the app size.
{% endhint %}

You can use our native SDK in your project using [Cocoapods](integration-guide-core.md) or [Manual](manual-setup-ios.md).



