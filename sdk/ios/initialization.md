# Initialization

## Initialize AcquireSupport SDK

**Step 1: Get your Acquire Account ID**

You can find your `accountID` as shown in image below :

![Get Acquire Account ID](https://gblobscdn.gitbook.com/assets%2F-LMa9C05MmCnAr03_v9O%2F-MSgJ2mo03pc0Tx2-JgU%2F-MSgMvdRYwCkFXSrlxUd%2FNew_AccountID.png?alt=media&token=336cc5fb-a565-4696-afde-ca6649f2142d)

**Step 2: Verify your users**

Make sure your users are who they claim to be with identity verification. Enforce identity verification to prevent other from pretend to be \(third party\) for entertainment or fraud logged-in users. Generate an `HMAC with SHA256` whenever a user logs into your app. Most web frameworks will have a method or library to help you do this.

You'll need your app’s secret key and the email of the currently logged-in user.

#### Secret Key

![User Authentication](https://gblobscdn.gitbook.com/assets%2F-LMa9C05MmCnAr03_v9O%2F-MSgJ2mo03pc0Tx2-JgU%2F-MSgN4xzhLsRp7Kd-JpY%2FNew_SecretKey.png?alt=media&token=4a1f50ab-b260-4ec3-8406-9b67aea77cdb)

For example, in Ruby on Rails we can generate our HMAC using a method called `OpenSSL::HMAC.hexdigest`, where the first parameter is the name of a hash function \(we use `SHA256`\), the second is `YOUR_SECRET_KEY`, and the third is your `USER_EMAIL`.

> Keep your secret key safe! Never commit it directly to your repository, client-side code, or anywhere a third party can find it.

To set up identity verification, you'll need to generate an HMAC on your server for each logged-in user and set in acquireIOSupport SDK.

#### setVisitorHash

If your visitor is identified \(i.e., visitor has already logged in your app and you have a email address of visitor\), call the following method before setAccount: an identified user.

```text
AcquireIO.support.setVisitorHash(<_Nonnull_Generated_HMAC_of_email>)
```

| Parameter | Type | Description |
| :--- | :--- | :--- |
| \_Nonnull\_Generated\_HMAC\_of\_email | String | A HMAC digest of the visitor email. |

> `setVisitorHash()` must be called **before setAccount:** takes place and must pass same email in `setVisitorDetails()`.

#### setVisitorIdentityFields

To set visitor identity for SDK, use `setVisitorIdentityFields` which takes identity parameters such as “email” and its value as an argument.

```text
AcquireIO.support.setVisitorIdentityFields(["email":"xyz@abc.com"])
```

| Parameter | Type | Description |
| :--- | :--- | :--- |
| fields | \[String: Any\] | identified parameter as key and its value |

> `setVisitorIdentityFields()` must be called before **setAccount:** takes place and must pass same email as passed in `setVisitorDetails()`.

### startSession

You must call this method to start a session with Acquire server. After calling `startSession()`, the `AcquireIODelegate` the delegate will receive either `didChangeConnectionStatus:` or `onError:`

```text
AcquireIO.support.startSession()
```

> **setAccount:** should be called first before calling above method

**Step 3: Setup Account**

To setup an account, call below method.

```text
AcquireIO.support.setAccount("your_acquire_account_id", domain: "optional_testing_domain_url", withOptions: config)
```

| Parameter | Type | Description |
| :--- | :--- | :--- |
| ACCOUNT\_ID | String | your account id from acquire dashboard from **Step 1** |
| domain | String \(Optional\) | your testing domain url. \(If not provided, default domain is Acquire Live Domain\) |
| configOptions | \[String : Any\] | config options. For more details on config options [Click here](https://developer.acquire.io/sdk/ios/theme-setting) |

#### showSupport

Calling this method will start a connection session with acquire server. After calling `showSupport()`, the `AcquireIODelegate` delegate will receive either `didChangeConnectionStatus:` or `onError:`

```text
AcquireIO.support.showSupport(<viewcontroller_instance>)
```

| Parameter | Type | Description |
| :--- | :--- | :--- |
| viewController | UIViewController | instance of viewcontroller on which support button should be displayed |

> **setAccount:** should be called first before calling above method

#### loadAcquireIOSupportFonts

To load SDK's **default** Fonts, following method must be called before _setAccount:_

```text
UIFont.loadAcquireIOSupportFonts
```

### User APIs

To customize visitor’s identification, you can call following sdk method to set the name, phone, email and fields of the app visitor. This is part of additional visitor configuration. Use this method before initialization of sdk otherwise it wont work.

```text
func setVisitorDetails(_ data: [String: Any])
```

| Parameter | Type | Description |
| :--- | :--- | :--- |
| data | \[String: Any\] | details of visitor e.g.\["name":"abc","phone":"xxxxxxxx","email":"abc@gmail.com"\] |

> Pass nil values for both name and email to clear out old existing values.

If this is provided through the api, user will not be prompted to re-enter this information again.

#### Logout visitor

If you have set visitor hash \(HMAC digest\) and visitor just logged out from account and need to manage user integrity with agent, call method `logoutVisitor()` to remove all acquire data from your app related to `visitorHash`. To `logout` from AcquireIOSupport, calling below method is mandatary:

```text
AcquireIO.support.logoutVisitor()
```

### Methods

#### getVisitorId

To fetch visitorID after acquire session Connected. Returns `string`

```text
let visitorID = AcquireIO.support.getVisitorID()
```

#### getAvailableAgentCount

To fetch total number of available agents. Returns `Int`.

```text
let agentsAvailableCount = AcquireIO.support.getAvailableAgentCount()
```

#### getOnlineAgentIDs

To fetch agentIDs of online agents. Returns `[NSNumber]`.

```text
let agentsIDs = AcquireIO.support.getOnlineAgentIDs()
```

#### dismissChatSupport

This optional method will dismiss the support view from the screen.

```text
AcquireIO.support.dismissChatSupport()
```

