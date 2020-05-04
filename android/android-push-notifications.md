# Android Push Notifications

Below, we’ll show you how to send push notifications and/or push messages to your customers, with Firebase Cloud Messaging \(FCM\) in Acquire.

### Step 1. Enable Google services for your app

If you already have a Firebase project with notifications enabled you can skip to the next step. Otherwise go to the FCM Console page and create a new project following these steps:

Give the project a name and click **‘Create Project’**.

Once your project is set up, scroll down and select **‘Get started’** on the **‘Notifications’** card.

Enter your app’s package name and click **‘Add App’**.

### Step 2. Setup client to receive push <a id="step-2--setup-client-to-receive-push"></a>

Your google-services.json should automatically download. You’ll need to move that into the same directory as your application level build.gradle.

In your apps build.gradle you will need to add the following lines to your dependencies:

```javascript
dependencies {
  implementation 'com.google.firebase:firebase-core:17.4.0'
  implementation 'com.google.firebase:firebase-messaging:20.1.6'
}
```

At the bottom of your build.gradle you must add:

apply plugin: 'com.google.gms.google-services'

It is important that this is at the very end of the file.

Call below sdk method to pass the Firebase token :

```text
AcquireApp.setFireBaseToken([Firebase token]);
```

### Step 3. Add your Server key to Acquire for Android settings <a id="step-3--add-your-server-key-to-acquire-for-android-settings"></a>

Finally, click the settings cog and select ‘Project settings’, then **‘Cloud Messaging’** and copy your Server key.

Open your Acquire app’s settings and select **‘Push notifications’** under **App Settings** . Then find the ‘FCM Server key’ section. Here you'll be able to paste and save your Server API key.

### Step 4. Setting your FCM icon <a id="step-4--setting-your-fcm-icon"></a>

If you want to add a custom icon for your notifications, just add an image named chat\_icon\_aqr\_white.png to each of your supported densities. Please note that vector drawables cannot be used here. For example:

```javascript
/res/drawable-xxhdpi/chat_icon_aqr_white.png 
/res/drawable-xhdpi/chat_icon_aqr_white.png 
/res/drawable-hdpi/chat_icon_aqr_white.png 
/res/drawable-mdpi/chat_icon_aqr_white.png
```



Notifications icon design guidelines

We recommend following these [material design guidelines](https://material.io/design/platform-guidance/android-notifications.html) for producing this icon.

### Troubleshooting tips <a id="troubleshooting-tips"></a>

If you’re having trouble getting FCM to work in your app, here's a list of things you should check:

* Enter your FCM Server key here -&gt; [https://app.acquire.io/setting/push-notifications](https://app.acquire.io/setting/push-notifications) .
* Check that the notifications are not disabled for your app on your test device. **Settings &gt; Sound & Notification &gt; App** notifications. This may differ depending on the Android version.
* Did you specify the correct Push Server API key?
* Make sure you added your google-services.json file in the correct directory.
* And as always, you can contact us via Acquire. We're always here to help

