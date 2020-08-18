# Cobrowse APIs

Acquire has this feature called Co-browsing which is unique in its sense, as it allows an agent to browse the session with the customer so that he/she can get the desired product/services on their website to purchase.

To use Cobrowse in your own app, you'll need to add our Native SDKs. We've made this as simple as possible, with just a few lines of code.

Once the Native SDKs are added to your app, everything else is done through our web dashboard in any browser - no plugins or installs needed.

### Features <a id="features"></a>

{% hint style="success" %}
 With Co-Browse any Agent can not only see his customer's screen but also he can access device with mouse and for text input, an Agent can type on customer device using his hardware keyboard. Isn't it fantastic!
{% endhint %}

{% hint style="success" %}
 Even more he can add overlays or highlight on the customer's device in real time.
{% endhint %}

{% hint style="info" %}
Note : Any Activity which extends to **AQR\_BaseActivity** will become supported for co-browse.
{% endhint %}



{% embed url="https://www.youtube.com/watch?v=sptkhM5n3Vc" %}

If you want to customize cobrowse settings then you can use our CobrowseBuilder class.

### CobrowseBuilder class provides following options :

1. **`setMAX_UPDATE_TIME(long MAX_UPDATE_TIME)`** :

```javascript
/**
 * Default Value - 1000L
 *
 * @param MAX_UPDATE_TIME - set the time of sending frames when screen is idle
 */
```

 2. **`setMIN_UPDATE_TIME(long MIN_UPDATE_TIME)`** :

```javascript
/**
 * Default Value - 400L
 *
 * @param MIN_UPDATE_TIME - This is the minimum interval for sending screenshots
 */
```

 3. **`setBITMAP_QUALITY (int BITMAP_QUALITY)`** :

```javascript
/**
 * Default is quality is set to 10
 *
 * @param BITMAP_QUALITY - Set Screen shot quality ranges from 1-100
 */
```

 4. **`setCoBrowseCODE(String coBrowseCODE)`** :

```javascript
/**
 * By default this is the automated random number
 * @param coBrowseCODE - Pass any Alpha-numeric value in form of String
 */
```

 5. **`setHideStopButton(boolean hideStopButton)`** :

![](../.gitbook/assets/android-cobrowse.PNG)

```javascript
/**
 * After session is connected you can choose to show our stop button or not
 * @param hideStopButton - Pass true to hide the stop button.
 */
```

 6. **`setConfirmStop(boolean enable)`** :

![](../.gitbook/assets/android-cobrowse-1.PNG)

```javascript
/**
 * You can enable/disable our confirmation dialog
 * @param enable - Pass true to show prompt on end session call
 */
```

#### e.g.

```javascript
CoBrowse cobrowse = new CoBrowse.CobrowseBuilder().setConfirmStop(false).setBITMAP_QUALITY(10).build();
```

 And then pass it to **initCobrowse** method :

```javascript
AcquireApp.initCobrowse(Application, [Your Account Id],cobrowse);
```

After initialization you can use both events callbacks :

* **OnSessionEvents** And
* **OnCoBrowseEvent**

**To get full understanding of all delegates** [**click here**](acquire-delegates.md)**.**

### **Useful methods to control the UI while co browsing.** 

#### Add mask to user's private data

![](../.gitbook/assets/android-cobrowse-2.PNG)

#### Set masking view color

![](../.gitbook/assets/android-cobrowse-3.PNG)

#### Set mouse icon which appears on user screen 

![](../.gitbook/assets/android-cobrowse-4.PNG)

