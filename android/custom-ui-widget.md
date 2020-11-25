# Custom UI/widget

### Change color of UI

**How it works**

Go to [https://app.acquire.io/widget/theme](https://app.acquire.io/widget/theme) - :

![](../.gitbook/assets/theme_change%20%282%29.png)

{% hint style="info" %}
Whole Chat module will change according to this Background color.

If not provided then it will use default primary colors of your app.
{% endhint %}

### Chat and call customization

To remove minimize video call option call below method. Use this method after successful initialization of AcquireApp.

```text
AcquireApp.removeMinimizeButton()
```

When require only agent can cut the call, call below method to remove endCall button from video and audio call.

```text
AcquireApp.removeDisconnectButton()
```

