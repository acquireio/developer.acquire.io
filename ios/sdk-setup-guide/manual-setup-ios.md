---
description: Setting up the SDK manually
---

# Manual Setup iOS

You can install our SDK manually using the steps below for iOS.

First, [Download AcquireIO iOS SDK.](https://devtools.acquire.io/sdk/ios/2.0.0/acquireIO.zip)

{% hint style="info" %}
Supports iOS 8.2 and above.
{% endhint %}

Unzip the SDK & Drop the `.framework` package into the "Embedded Binaries" list in your targets &gt; general tab. This will add the .framework to "Linked Frameworks and Libraries" as well.

![Add AcquireIO.framework to your project](../../.gitbook/assets/manual-add.png)

Add the following frameworks to `Link Binary with Libraries` -

* `CoreFoundation`
* `CoreGraphics`
* `QuartzCore`
* `UIKit`



Go to Project/Targets -&gt; \[Project Name\] -&gt; Build Settings.  
Search `"ALWAYS_EMBED_SWIFT_STANDARD_LIBRARIES"`

![](../../.gitbook/assets/swift-enable.png)

Search `"Enable bitcode"` to `NO`

![Disable bitcode](../../.gitbook/assets/bitcode-no.png)

{% embed url="https://www.youtube.com/watch?v=45bhaS4iUq4" caption="" %}

