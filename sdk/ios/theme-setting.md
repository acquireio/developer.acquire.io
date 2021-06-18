# Theme Setting

## Theme Settings

> Using `UIAppearance`
>
> UIAppearance customizations are applied to AcquireIOSupport SDK by default. However if there is a conflicting property, then the value in `ThemeOptions` key in `AcquireIOConfig` will take precedence.
>
> For example: If the app uses `UIAppearance` to change the color of Navigation Bar title and also specifies a color for the same property in the _AcquireIOConfig ThemeOptions_ - NSDictionary, then the value in dictionary will be used.
>
> In order to use the UIAppearance value, the app must leave the corresponding entry in the `ThemeOptions` blank.

### Introduction

Head over to Theming if you want to customize your SDK integration's typeface, colors or fonts. It can be achieved via simple key-value pairs in option dictionary.

#### Configuration

Theme customization can be configured via `AcquireIOConfig` class:

```text
let options = [String : Any]()
let config = AcquireIOConfig.config
config.setDict(options)

//Pass `config` to- setAccount: withOptions:config
```

Set _Dictionary_ options in format of key-value. Color code will be hex value of color, start from \#. You can remove and leave blank for default theme effect.

> Sample format for setting Config options:

```text
let themeDict = [
                  "ACQUIREIO_GLOBAL": [
                      "THEME_COLOR":"#ff87b8"
                  ],
                  "ACQUIREIO_NAVIGATION_BAR": [
                      "BAR_STYLE": "UIBarStyleBlack",
                      "BAR_TINTCOLOR": "#ff87b8",
                      "TINT_COLOR": "#FFFFFF"
                  ],
                  "ACQUIREIO_BADGE_VIEW": [
                      "BACKGROUND_COLOR": "#ff0000",
                      "BORDER_COLOR": "#FE0319",
                      "TEXT_COLOR": "#ff0000"
                  ],
                  
                  "ACQUIREIO_SYSTEM_BUTTON": [
                      "BACKGROUND_COLOR": "#ff0000",
                      "BUTTON_INSET_BOTTOM": NSNumber(value: 100),
                      "BUTTON_INSET_RIGHT": NSNumber(value: 90)
                  ]
                ]

 let option = [ ...
                "ThemeOptions": themeDict
              ]
```

#### Config Options

Along with Theme settings, SDK supports following optional customization options.

```text
 let option = [
                "ThemeOptions": themeDict,
                "ShowVideoButton": true,
                "ShowAudioButton": true,
                "ShowChatButton": true,            
                "isHideNewChat": false,
                "SessionConnectAndStartAuto": true,
                "disableAttachment": false,
                "ShowThreadList": true,
                "ButtonImageName": "chat.png",
                "ShowLocalNotificationInApp": true,
                "DisableNetworkMessage": false ] as [String : Any]
```

* `ShowVideoButton` : To show video call button in top bar of visitor's main chat messages screen. Default value is set to `true`.
* `ShowAudioButton` : To show audio call button in top bar of visitor's main chat messages screen. Default value is set to `true`.
* `ShowChatButton` : To hide support system button on bottom right of screen , set to `false` and it will hide the button but chat functionality will not be affected by this option. Default value set to `true`.
* `isHideNewChat` : if set to `true`, user won't be able to start new chat with agents. if set to `false`, user can start new chat with agents. Default value set to `false`.
* `SessionConnectAndStartAuto` : Session will be automatically connected to server and start, no need to invoke any additional method for start session. If you set `false`, then you must call `AcquireIO.support.startSession()` method to start new connection with server. Default value is set to `true`.
* `disableAttachment` : To disable uploading attachment to agents. Default value is set to `false`.
* `ShowThreadList` : To show list of sessions/threads. Default value is set to `true`.
* `ButtonImageName` : To set an Image for AcquireIOsupport chat system button. Custom Image should be put in main bundle of app. Image size 30x30 px, 60x60 px for @2x.
* `ShowLocalNotificationInApp` : To allow SDK to show in-app notification when app state is Active. Default value is `true`.
* `DisableNetworkMessage` : To disable showing “Please Check Internet Connection” message when there is no internet connectivity. Default value is set to `false`, which mean SDK will show this message if not specified in config options.

### Theme Settings

To skin your app, make sure you add AcquireIOConfig `ThemeOptions` key.

* Colors are specified in hexadecimal format, e.g. \#FFFFFF is White. \# is required before code.
* Font names should be specified by their family name & style. For example, **CaviareDreams-Bold** refers to **Caviare Dreams family** of **bold** style. See using custom fonts section below for more details.

#### Global Attribute

These attributes control the looks of in-app support over many screens.

| Property | Description |
| :--- | :--- |
| THEME\_COLOR | Applies theme color to whole support SDK according to your app theme. Default theme color is \#3A6 |
| FONT\_NAME | Global font face - applies to texts for sections list, Chat list, Offline form and all. Default font is system font with size according to requirements |
| BOLD\_FONT\_NAME | Applies to headers on chat screen and title of pages. Default font is system bold font with size according to requirement |

#### Navigation Bar

| Property | Description |
| :--- | :--- |
| BAR\_STYLE | Use UIBarStyleBlack or UIBarStyleDefault. Default bar style is UIBarStyleDefault |
| BAR\_TINTCOLOR | The tint color to apply to the navigation bar background. This color is not made translucent by default unless you set the isTranslucent property to true. Default BAR\_TINTCOLOR is \#FFFFFF |
| TINT\_COLOR | The tint color is navigation title and back and other bar button items color. Default color is \#000000 |

#### System Button Attributes

These attributes applies on default bottom right support button.

| Property | Description |
| :--- | :--- |
| BACKGROUND\_COLOR | Applies to background color of button. Default theme color is THEME\_COLOR |
| BUTTON\_INSET\_BOTTOM | Inset button from bottom in NSNumber. default bottom inset is 0. |
| BUTTON\_INSET\_RIGHT | Inset button from right in NSNumber. default right inset is 0. |

#### System Badge Button Attributes

These attributes applies on default bottom right support button notification badge.

| Property | Description |
| :--- | :--- |
| BACKGROUND\_COLOR | Applies to background color of button badge. Default color is red |
| BORDER\_COLOR | Applies border to the badge button |
| TEXT\_COLOR | Button badge color. Default color is \#ffffff. |

#### Using Custom Fonts

**Step 1.** Add the font to your project. Edit your app's plist file and add a key "Fonts provided by application" to it. Under the key, list out file names of all the fonts you want to use in your app and in support. If you've already listed such fonts, skip this step.

![Add Custom Fonts](https://gblobscdn.gitbook.com/assets%2F-LMa9C05MmCnAr03_v9O%2F-LN9EeARIb0jlqCV5rMw%2F-LN9F1_w4tEq2jAlh6ye%2Ffont-screen.png?alt=media&token=0683d74a-3780-4987-a517-2399008718c3)

**Step 2.** Copy the font's full name. To do this, select the font in Finder and hit `COMMAND` `⌘+I` \(Get Info\).

![Get full Name of the font](https://gblobscdn.gitbook.com/assets%2F-LMa9C05MmCnAr03_v9O%2F-LN9EeARIb0jlqCV5rMw%2F-LN9FCAVkyfSaMNtD3UV%2FfontName-screen.png?alt=media&token=889e571b-effb-4059-aa0b-55346b3be3f2)

**Step 3.** Paste the font name into

Set AcquireIOConfig with `@"ThemeOptions" -> @"ACQUIREIO_GLOBAL" ->@"FONT_NAME""` , wherever necessary

![Add custom font in your themeOptions](https://gblobscdn.gitbook.com/assets%2F-LMa9C05MmCnAr03_v9O%2F-LNxYVHfRlIavnBiPh8X%2F-LNxeuBmaeWBQyOh1kJq%2Fimage-sample-code-config-dict.png?alt=media&token=7828300b-bc6c-407b-b495-a7ae334b7996)

