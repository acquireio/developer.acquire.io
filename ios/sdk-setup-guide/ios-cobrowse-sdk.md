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

* Unzip the SDK & drag-drop `acquireIO.framework` files into your Xcode project.
* In `Build Phases`, verify that `AcquireIO.framework` is in the `Link Binary with Libraries` and the AcquireIO resources are in `Copy Bundle Resources`
* Add the following frameworks to `Link Binary with Libraries` -
  * `CoreFoundation`
  * `CoreGraphics`
  * `QuartzCore`
  * `UIKit`

## Methods

### Get Cobrowse Code

Get visitor cobrowse code, when acquire session ready to connect

If acquire support session not started then it will return -1, otherwise session code to start cobrowse session with agent.

{% hint style="info" %}
Available in SDK version 1.0.9 or later
{% endhint %}

**Sample code**

{% tabs %}
{% tab title="Objective C" %}
```objectivec
NSInteger code = [[AcquireIO support] getCobrowseCode];
```
{% endtab %}

{% tab title="Swift" %}
```swift
let code = AcquireIO.support().getCobrowseCode()
```
{% endtab %}
{% endtabs %}

### Add Mask on View

Adds a UIView to mask during the cobrowse session.

| Parameter | Type | Description |
| :--- | :--- | :--- |
| `view` | `id <UIView>` |  instance to mask _`required`_ |

Sample Code

{% tabs %}
{% tab title="Objective C" %}
```objectivec
//Mask UIImageView
[[AcquireIO support] addMaskedView:self.imageView];

//Mask UITextField
[[AcquireIO support] addMaskedView:self.textfield];

//Mask UITextView
[[AcquireIO support] addMaskedView:self.textview];
```
{% endtab %}

{% tab title="Swift" %}
```text
//Mask UIImageView
AcquireIO.support().addMaskedView(self.imageView);

//Mask UITextField
AcquireIO.support().addMaskedView(self.textfield);

//Mask UITextView
AcquireIO.support().addMaskedView(self.textview);
```
{% endtab %}
{% endtabs %}

### Remove Masked View

Remove a UIView from being masked during a cobrowse session.

**Sample Code**

{% tabs %}
{% tab title="Objective C" %}
```objectivec
[[AcquireIO support] removeMaskedView:self.yourMaskedView];
```
{% endtab %}

{% tab title="Swift" %}
```swift
AcquireIO.support().removeMaskedView(self.yourMaskedView);
```
{% endtab %}
{% endtabs %}

### Mask Keyboard

Masks the keyboard from being shown `(Default: NO)`

**Sample Code**

{% tabs %}
{% tab title="Objective C" %}
```objectivec
[[AcquireIO support] maskKeyboard:YES]
```
{% endtab %}

{% tab title="Swift" %}
```swift
AcquireIO.support().maskKeyboard(true)
```
{% endtab %}
{% endtabs %}

### Pause Sharing

Pause an active cobrowse session

**Sample Code**

{% tabs %}
{% tab title="Objective C" %}
```objectivec
[[AcquireIO support] pauseSharing];
```
{% endtab %}

{% tab title="Swift" %}
```swift
AcquireIO.support().pauseSharing()
```
{% endtab %}
{% endtabs %}

### Start Sharing

Start a cobrowse session with a agent. Note that for Visitor sessions already start sharing when agent start cobrowse session via code. You can Pause and start sharing again.

{% hint style="warning" %}
**init: no need to call first time. After pause then you can call this method**
{% endhint %}

**Sample Code**

{% tabs %}
{% tab title="Objective C" %}
```objectivec
[[AcquireIO support] startSharing];
```
{% endtab %}

{% tab title="Swift" %}
```swift
AcquireIO.support().startSharing()
```
{% endtab %}
{% endtabs %}

### End Sharing

End the cobrowse session. Calling endSharing initiates the process of ending the session.

**Parameter**

| **Parameter** | Type | Description |
| :--- | :--- | :--- |
| `showPrompt` | `boolean` | Pass bool value to show or not confirmation. |

**Sample Code**

{% tabs %}
{% tab title="Objective C" %}
```objectivec
[[AcquireIO support] endSharing:NO];
```
{% endtab %}

{% tab title="Swift" %}
```swift
AcquireIO.support().endSharing(false)
```
{% endtab %}
{% endtabs %}

### Remove Stop Sharing Button

After session is connected you can choose to show our stop button or not.

Add key `@"ShowDefaultStopButton"` for stop sharing button. Set Value `@YES` to hide the stop button.

Also check about how to add key in config dictionary, see this:

{% page-ref page="sdk-configuration-example.md" %}

## Example app

There is an example app provided [here](https://github.com/acquireio/acquireio-cobrowse-ios) for both Objective-C and Swift.

Next: How to configure Acquire SDK in App, See this:

{% page-ref page="sdk-configuration-example.md" %}



