---
description: Make sure your users are who they claim to be with identity verification.
---

# Verify your users

Enforce identity verification to prevent other from pretend to be \(third party\) for entertainment or fraud logged-in users.

Generate an HMAC with SHA256 whenever a user logs into your app. Most web frameworks will have a method or library to help you do this. You'll need your app’s secret key and the email of the currently logged-in user.

**Secret Key**  
&lt;YOUR\_SECRET\_KEY&gt;

For example, in Ruby on Rails we can generate our HMAC using a method called `OpenSSL::HMAC.hexdigest`, where the first parameter is the name of a hash function \(we use SHA256\), the second is your secret key, and the third is your user’s email.

```cpp
OpenSSL::HMAC.hexdigest(
  'sha256', # hash function
  '<YOUR_SECRET_KEY>', # secret key (keep safe!)
  current_user.email # user's email address
)
```

{% hint style="info" %}
Keep your secret key safe! Never commit it directly to your repository, client-side code, or anywhere a third party can find it.
{% endhint %}

To set up identity verification, you'll need to generate an HMAC on your server for each logged-in user and set in acquireIO SDK.

{% hint style="info" %}
This must be called before `setAccount:` takes place and must pass same email in `setVisitor:`.
{% endhint %}

```objectivec
[[AcquireIO support] setVisitorHash:<_Nonnull String your_hmac_of_email>];
```

First, you need to add email id in set visitor method in SDK for uniquely identify your users. Note that if you set only visitor hash and email is not set then acquire can't identify visitor. So you need both method to verify visitor hash.

```objectivec
[[AcquireIO support] setVisitor:<Nullable String Name> phone:<Nullable String Phone Number> andEmail:<Nullable String Email>];
```

### **Logout visitor**

If you have set visitor hash \(HMAC digest\) and visitor just logged out from account and need to manage user integrity with agent, call method logoutVisitor to remove all acquire data from your app related to visitorHash. This must call method to logout from acquireIO support:

```objectivec
[[AcquireIO support] logoutVisitor];
```

