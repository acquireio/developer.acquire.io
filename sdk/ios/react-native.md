# React Native

## AcquireIO Support SDK

There are 2 variants for this SDK

1\) **AcquireIO support \(Core\)** for real-time chat and audio/video calls. 2\) **AcquireIO support \(Lite\)** for real-time chat.

> **Note**: Lite version supports only chat feature. To use audio/video calls, Core version is available.

This guide describes the process of implementing AcquireIOSupport SDK into your **React-Native app.**

You can refer [react-native-doc](https://reactnative.dev/docs/native-modules-ios) to use Native components.

We recommend using [CocoaPods](https://cocoapods.org/) as the most advanced way of managing iOS project dependencies.

#### Installation

AcquireIOSupport SDK is the same as any other third-party native library.

To connect AcquireIOSupport SDK to your app just add it into your Podfile:

**Step 1.** Create a Podfile in your project's root directory, if it doesn't exist yet.

**Step 2.** Add below lines at top of your `podfile`

```javascript
require_relative '../node_modules/react-native/scripts/react_native_pods'
require_relative '../node_modules/@react-native-community/cli-platform-ios/native_modules'
```

**Step 3.**

* **AcquireIOSupport-Core** : Podname to add Core SDK to your project
* **AcquireIOSupport-Lite** : Podname to add Lite SDK to your project

Add `podname` to Podfile as per requirement under your desired target. It must look like below:

```text
  target 'YourTargetName' do
  config = use_native_modules!

  # NOTE: For AcquireIOSupport-Core require dynamic frameworks
  use_frameworks!
  pod 'AcquireIOSupport-Core'

  use_react_native!(
     :path => config[:reactNativePath],
     # to enable hermes on iOS, change `false` to `true` and then install pods
     :hermes_enabled => false
   )

  end
```

**Note: use\_frameworks! is required to import any dynamic framework.**

**Step 4.** The AcquireIOSupport SDK supports **module stability** and therefore all its dependencies must be built-in with the **"Build Libraries for Distribution"** setting enabled, however this is not currently supported in Cocoapods. Running the below command will ensure Xcode builds the dependencies with the correct settings. Once Cocoapods supports module stability, this workaround can be removed.

Add the following at the end of your Podfile:

```bash
 post_install do |installer|
    react_native_post_install(installer)

     installer.pods_project.targets.each do |target|
       target.build_configurations.each do |config|
         config.build_settings['BUILD_LIBRARY_FOR_DISTRIBUTION'] = 'YES'
         config.build_settings['ENABLE_BITCODE'] = 'NO'
       end

     if (target.name&.eql?('FBReactNativeSpec'))
       target.build_phases.each do |build_phase|
         if (build_phase.respond_to?(:name) && build_phase.name.eql?('[CP-User] Generate Specs'))
           target.build_phases.move(build_phase, 0)
         end
       end
     end
   end
 end
```

4\) Run the below command to install the SDK to your project

```bash
      $ pod install --repo-update
```

5\) Open your project using the generated \*.xcworkspace file.

> #### **Note:** If you are new to CocoaPods, go to [CocoaPods](https://cocoapods.org/) to learn how to install it.

Make sure to always open the Xcode workspace instead of the project file when building your project:

```text
open YourTargetName.xcworkspace
```

#### Setup Info.plist

> _Since iOS 10, it's mandatory to add before you access privacy-sensitive data like Camera, Microphone, and so on, you must ask for the authorization, or your app will crash when you access them._

Open the file in your project named **info.plist**, right-click it, opening as _Source Code_, paste the below code to it. Or you can open info.plist as **Property List** by default, click the **add** button, Xcode will give you the suggested completions while typing `Privacy -` with the help of keyboard and

Remember to write your description of why you ask for this authorization, between `<string>` and `</string>`, or your app will be rejected by Apple:

```text
<!-- Camera -->
<key>NSCameraUsageDescription</key>
<string>$(PRODUCT_NAME) uses camera for video chat</string>

<!-- Microphone -->
<key>NSMicrophoneUsageDescription</key>
<string>$(PRODUCT_NAME) uses microphone for voice chat</string>

<!-- Photo Library -->
<key>NSPhotoLibraryUsageDescription</key>
<string>$(PRODUCT_NAME) send photo/video to agent</string>
```

Also, The AcquireIOSupport SDK uses a background mode `Audio` when you are video/voice call to agent/visitor. If you have not enabled it, the background voice will not work. When the **UIBackgroundModes** key contains the audio value, the system’s media frameworks automatically prevent the corresponding app from being suspended when it moves to the background

To allow your AcquireIOSupport SDK to play audio in the background, Enable it using the below steps 1\) Select your project file in the Navigator of Xcode. 2\) From the Capabilities section, switch on the **Background Modes** subsection 3\) Switch **ON** the Background Modes subsection. After background modes are listed, tick on the _Audio, Airplay & picture in the picture_

![Background Mode](https://s3.amazonaws.com/com.twilio.prod.twilio-docs/images/BackgroundModes.original.png)

### Setup and installation

* To import SDK to your project, add the below lines to your **App.js**

  ```text
  //Native modules
  import {NativeModules} from 'react-native';
  //Destructuring AcquireIO Setup from NativeModules
  const {AcquireIOSetup} = NativeModules;
  ```

  And to use in your `FILENAME.m` file, add

  ```text
  #import <AcquireIOSupport/AcquireIOSupport.h>
  ```

* To initialize SDK, call

  ```text
      AcquireIOSetup.initAcquireIO()
  ```

Your `FILENAME.m` should look like:

```text
#import "AcquireIOSetup.h"
#import <React/RCTLog.h>

@implementation AcquireIOSetup

RCT_EXPORT_MODULE(); // Use "AcquireIOSetup" as module's name


RCT_EXPORT_METHOD(initAcquireIO) {

  RCTLogInfo(@"Init AcquireIO");

  dispatch_async(dispatch_get_main_queue(), ^{

    //Config option
    NSDictionary *option = @{
                             @"ShowChatButton": @YES,
                             @"SessionConnectAndStartAuto":@YES  //@NO for manually start socket connection
                           };

    AcquireIOConfig *config = [AcquireIOConfig config];
    [config setDict:option];

    #warning(@"TODO: Add your ACCOUNT_ID (for example, xo3t0x)")
    [[AcquireIO support] setAccount:@"ACCOUNT_ID" withOptions:config];

    //[[AcquireIO support] startSession]; for manually start socket connection

  });

}

@end
```

* To know more about customization of AcquireIOSupport chat theme, Go to [Theme Customization](https://developer.acquire.io/v/2.0.0/sdk/ios/theme-setting).
* To know more about initialization methods, [click here](https://developer.acquire.io/v/2.0.0/sdk/ios/initialization).
* For AcquireIOSupport delegate methods, Go to [Delegate Methods](https://developer.acquire.io/v/2.0.0/sdk/ios/acquire-sdk-delegates).

### Demo App

* Check out our React-native demo app [here](https://drive.google.com/file/d/1BtggKOJyKK6vP_ZhoN1Agp6KqhwyDedC/view?usp=sharing).

### Contact us

* We're only a **message away!**. Feel free to contact us on [AcquireIO Support](https://acquire.io) for any queries you may have.

