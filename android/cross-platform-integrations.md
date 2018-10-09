# Cross Platform Integrations

### phoneGap , cordova 

For cross platform tools like phoneGap , cordova , IONIC , etc…

You need to be more careful while adding our sdk.

Because these tools do changes in files like Android Manifest at compile time.

So Be sure that your final AndroidManifest.xml includes basic elements of our sdk.

#### **Service and Activities:**

If not included these below lines then add it manually on your AndroidManifest.xml.

#### **1. Service:**

```javascript
<service
		android:name="com.acquireio.socket.SocketBackgroundService"
		android:exported="true" />
```

 **2. Activities:**

```javascript
<activity   android:name="com.acquireio.sdk.activities.AQR_ChatListActivity"
		android:launchMode="singleInstance"
		android:screenOrientation="portrait" />
	<activity  android:name="com.acquireio.sdk.activities.AQR_ChatActivity"
		android:launchMode="singleInstance"
		android:screenOrientation="portrait" />
```

Further if you are facing any difficulty then please contact us.

### React Native

For React-Native also you can use our native andrtoid sdk.

You can also check our [demo app](https://github.com/acquireio/acquireReactProject) built upon react-native platform to get an idea how to configure our android native sdk on to your react native project.

{% hint style="info" %}
 **Note:** Our provided all android APIs will work from native android only.
{% endhint %}



