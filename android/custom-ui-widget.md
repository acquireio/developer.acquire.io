# Custom UI/widget

### Change color of UI

**How it works**

Go to [https://app.acquire.io/widget/theme](https://app.acquire.io/widget/theme) - :

![](../.gitbook/assets/theme_change%20%282%29.png)

{% hint style="info" %}
Whole Chat module will change according to this Background color.

If not provided then it will use default primary colors of your app.
{% endhint %}

### Customize chat widget

Use our**`SupportFABBuilder`** class to customize our **chat widget** as per your requirement.

**e.g.**

```javascript
AcquireApp.supportFAB = new SupportFAB.SupportFABBuilder()
       .setFabIconPosition(SupportFAB.FAB_POSITION.BOTTOM_RIGHT)
       .setFABAnimation(true).setFabSize(0).setFabIconColor(Color.WHITE).build();

```

{% hint style="info" %}
Call this code snippet before initialization of acquire SDK.
{% endhint %}

 Here is the list of methods to customize chat widget:

```javascript
setFabSize(int fabSize);
/**
* Set FAB icon Size - By Default set to FAB_SIZE_NORMAL
*
* @param fabSize- Pass the size of the FAB icon 0 for Normal and 1- for mini
*/
```

```javascript
setFabIconPosition(FAB_POSITION fabIconPosition);
/**
* Set the FAB Position
*
* @param fabIconPosition - Pass the FAB icon position Start, Top ,End , Bottom
*/
```

```javascript
setFabText(String fabText);
/**
* Set FAB text
*
* @param fabText - Pass the Desired String value
* @note - text will override icon
*/
```

```javascript
setFabTextColor(int fabTextColor)
/**
* Set the FAB Text color value  - By default set to white
*
* @param fabTextColor - Pass the FAB Text color value
*/

```

```javascript
setFabElevation(int fabElevation); 
/**
* Set FAB Elevation - By default set to 0
*
* @param fabElevation- Pass the integer value
*/
```

```javascript
setFabColor(int fabColor);
/**
* Set FAB color - By default it is primary ascent color
*
* @param fabColor - FAB color integer value
*/
```

```javascript
setFabIcon(int fabIcon);
/**
* Set FAB icon
*
* @param fabIcon - Desired icon resource id
*/
```

```javascript
setFabIconColor(int fabIconColor);
/**
* Set FAB icon color
*
* @param fabIconColor - pass integer value of color
*/
```

```javascript
setFabTextAllCaps(boolean allCaps);
/**
* You can enable/disable our textAllCaps
*
* @param allCaps - Pass true to capitalize all characters of FAB text
*/
```

```javascript
setFABAnimation(boolean fabAnimation);
/**
* You can enable/disable our fabAnimation - By Default set to true
*
* @param fabAnimation - Pass true to animate FAB
*/
```

```javascript
setMargins(int left, int top, int right, int bottom);
/**
* Set appropriate margin to chat widget
*
* @param left - Pass the int value for left side margin
* @param top - Pass the int value for top side margin
* @param right - Pass the int value for right side margin
* @param bottom - Pass the int value for bottom side margin
*/
```



