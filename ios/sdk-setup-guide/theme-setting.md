# Theme Setting

{% hint style="info" %}
**Using UIAppearance**

UIAppearance customizations are applied to AcquireIO SDK by default. However if there is a conflicting property, then the value in AcquireIOConfig.plist will take precedence.

For example: If the app uses UIAppearance to change the color of Navigation Bar title and also specifies a color for the same property in the AcquireIOConfig.plist file, then the value in plist will be used. In order to use the UIAppearance value, the app must leave the corresponding entry in the plist blank.

if you don't want to use AcquireIOConfig.plist properties to SDK the use init method attribute option to '`UseDefaultTheme`' to `@YES`.
{% endhint %}

### Introduction {#introduction}

Head over to Theming if you want to customize your SDK integration's typeface, colors or fonts. It is done via simple key-value pairs in a plist file.

### Theme Setting {#theme-setting}

To skin your app, make sure you add `AcquireIOConfig.plist` into your project main bundle and set values for attributes in `AcquireIOConfig.plist`. You can copy `AcquireIOConfig.plist` from Frameworks/AcquireIO.framework/AcquireIOConfig.plist.

| Property | Description |
| :--- | :--- |
| `Colors` | Colors are specified in hexadecimal format, e.g. `#FFFFFF` is White. \# is required before code |
| `Fonts` | Font names should be specified by their family name & style. For example, **CaviareDreams-Bold** refers to Caviare Dreams _family_ of bold _style_. See using custom fonts section for more details |

### Global Attributes {#global-attributes}

These attributes control the looks of in-app support over many screens.

| Property | Description |
| :--- | :--- |
| `THEME_COLOR` | Applies theme color to whole support SDK according to your app theme. Default theme color is `#448ee1` |
| `FONT_NAME` | Global font face - applies to texts for sections list, Chat list, Offline form and all. Default font is system font with size according to requirement |
| `BOLD_FONT_NAME` | Applies to headers on chat screen and title of pages. Default font is system bold font with size according to requirement |

### Navigation Bar {#navigation-bar}

| Property | Description |
| :--- | :--- |
| `BAR_STYLE` | Use `UIBarStyleBlack` or `UIBarStyleDefault`. Default bar style is `UIBarStyleDefault` |
| `BAR_TINTCOLOR` | The tint color to apply to the navigation bar background. This color is not made translucent by default unless you set the isTranslucent property to true. Default `BAR_TINTCOLOR` is `#FFFFFF` |
| `TINT_COLOR` | The tint color is navigation title and back and other bar button items color. For more see image bellow. Default color is `#000000` |

[![](https://developers.acquire.io/media/data/article/e8608c12-1a29-47c9-95c5-984a0ca17bce.png)](https://developers.acquire.io/media/data/article/e8608c12-1a29-47c9-95c5-984a0ca17bce.png)

### System Button Attributes {#system-button-attributes}

These attributes applies on default bottom right support button.

| Property | Description |
| :--- | :--- |
| `BACKGROUND_COLOR` | Applies to background color of button. Default theme color is `THEME_COLOR` |
| `BUTTON_INSET_BOTTOM` | Inset button from bottom in `NSNumber`. default bottom inset is 0. |
| `BUTTON_INSET_RIGHT` | Inset button from right in `NSNumber`. default right inset is 0. |

### System Button Badge Attributes {#system-button-badge-attributes}

These attributes applies on default bottom right support button notification badge.

| Property | Description |
| :--- | :--- |
| `BACKGROUND_COLOR` | Applies to background color of button badge. Default color is red |
| `TEXT_COLOR` | Button badge color. Default color is `#ffffff`. |

### Using Custom Fonts {#using-custom-fonts}

Add the font to your project. Edit your app's plist file and add a key `"Fonts provided by application"` to it. Under the key, list out file names of all the fonts you want to use in your app and in support. If you've already listed such fonts, skip this step.

[![](https://developers.acquire.io/media/data/article/font-screen.png)](https://developers.acquire.io/media/data/article/font-screen.png)

**Step 2:** Copy the font's full name. To do this, select the font in Finder and hit **`COMMAND`** `⌘+I` \(Get Info\).

[![](https://developers.acquire.io/media/data/article/fontName-screen.png)](https://developers.acquire.io/media/data/article/fontName-screen.png)

**Step 3:** Paste the font name into `AcquireIOConfig.plist`, wherever necessary

[![](https://developers.acquire.io/media/data/article/AcquireIOConfigPlistFont.png)](https://developers.acquire.io/media/data/article/AcquireIOConfigPlistFont.png)

**Step 4:** Test the font and theme in simulator. If font couldn't load by SDK then it will show error —

[![](https://developers.acquire.io/media/data/article/sdk-theme.png)](https://developers.acquire.io/media/data/article/sdk-theme.png)

### Orientation support {#orientation-support}

By default, the iOS SDK will follow the orientation of the app.

