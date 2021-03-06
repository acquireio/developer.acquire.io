---
description: Learn how to use Cobrowse feature using our native SDK.
---

# iOS Cobrowse

Acquire has this feature called Co-browsing which is unique in its sense, as it allows an agent to browse the session with the customer so that he/she can get the desired product/services on their website to purchase.

To use Cobrowse in your own app, you'll need to add our Native SDKs. We've made this as simple as possible, with just a few lines of code.

Once the Native SDKs are added to your app, everything else is done through our web dashboard in any browser - no plugins or installs needed.

{% hint style="info" %}
Even more he can add overlays or highlight on the customer's device in real time.
{% endhint %}

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

Show prompt message for end confirmation, see:

![End sharing prompt message for user](../.gitbook/assets/screen-shot-2018-09-24-at-1.11.07-pm.png)

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

![ShowDefaultStopButton](../.gitbook/assets/showdefaultstopbutton.png)

Add key `@"ShowDefaultStopButton"` for stop sharing button. Set Value `@NO` to hide the stop button.

Also check about how to add key in config dictionary, see this:

{% page-ref page="sdk-configuration-example.md" %}

## Example app

If you want a sample app for cobrowse\_only SDK version , you can download the sample app with integrated our SDK from Github. Example app provided [here](https://github.com/acquireio/acquireio-cobrowse-ios) for both Objective-C.

Next: How to configure Acquire SDK in App, See this:

{% page-ref page="sdk-configuration-example.md" %}



