# User Verification

 Make sure your users are who they claim to be with identity verification. Enforce identity verification to prevent other from pretend to be \(third party\) for entertainment or fraud logged-in users.

 Generate an **HMAC** with **SHA256** whenever a user logs into your app. Most web frameworks will have a method or library to help you do this. You'll need your app’s secret key and the email of the currently logged-in user.

#### **Secret Key**

 _\[YOUR\_SECRET\_KEY\]_

 Then, choose the server-side language or framework you are using:

{% tabs %}
{% tab title="PHP" %}
Your code to generate an HMAC for your app is:

```javascript
hash_hmac(
  'sha256', // hash function
  $user->email, // user's id
  '' // secret key (keep safe!)
);
```
{% endtab %}

{% tab title="Rails" %}
 Your code to generate an HMAC for your app is:

```javascript
OpenSSL::HMAC.hexdigest(
  'sha256', # hash function
  '', # secret key (keep safe!)
  current_user.email # user's email
)
```
{% endtab %}

{% tab title="Python" %}
 Your code to generate an HMAC for your app is:

```javascript
import hmac
import hashlib

hmac.new(
  '', # secret key (keep safe!)
  request.user.email, # user's email
  digestmod=hashlib.sha256 # hash function
).hexdigest()
```
{% endtab %}

{% tab title="Other" %}
 For example, in Ruby on Rails we can generate our **HMAC** using a method called `OpenSSL::HMAC.hexdigest()`, where the first parameter is the name of a hash function \(we use **SHA256**\), the second is your secret key, and the third is your user’s user\_email.

```javascript
OpenSSL::HMAC.hexdigest(
  'sha256', # hash function
  '', # secret key (keep safe!)
  current_user.email # user's email
)
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
 **Note:** Keep your secret key safe! Never commit it directly to your repository, client-side code, or anywhere a third party can find it.
{% endhint %}



### Visitor Authentication

For visitor authentication you  can use this run following code asap you load acquire init.js script or before that, and add a new attribute **`user_hash`** and assign the **HMAC** code along with user's email or any other details to cofing object.

_To get HMAC code, login acquire dashboard and open this:_ [_https://app.acquire.io/widget/customize_](https://app.acquire.io/widget/customize) _and Chat widget code in Choose Visitor authentication._

{% hint style="info" %}
**Important :** Use **HMAC** only Server side not use client side and Keep your secret key safe! Never commit it directly to your repository.
{% endhint %}

```javascript
<script type="text/javascript">
	window.acquire=window.acquire||[];
	acquire.push({
		user_hash:'INSERT_HMAC_VALUE_HERE',
		userDetails:{
			email:'customer@example.com', //EMAIL
		}
	});
</script>
```

###  **Logout visitor**

If you have set visitor hash \(**HMAC digest**\) and visitor just logged out from account and need to manage user integrity with agent, call method `logoutVisitor()` to remove all acquire data from your app related to visitorHash. This must call method to logout from acquireIO support:

```javascript
acquireIO.logoutVisitor()
```

Once you've called logout visitor, it will destroy current user's session and start again guest user's session as it was before.

in case you've already started acquire widget and guest visitor is already started its session, that case you can still use above code or also following function to make user login back.

```javascript
acquireIO.loginVisitor('USER_HASH',{email:'user@example.com'})
```

