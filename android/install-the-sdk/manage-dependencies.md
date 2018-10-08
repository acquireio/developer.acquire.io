# Manage Dependencies

### Steps to integrate sdk to your app

Follow the below steps to integrate Acquire with your existing app.

#### Update your Gradle files

In your project-level build.gradle build file:

```javascript
allprojects {
    repositories {
        maven {
            // Add this line 
            url "http://107.155.116.28:8086/artifactory/libs-release-local"
        }
    }
}
```

 So the top level gradle file will look like this :

```javascript
buildscript {
   repositories {
       jcenter()
      google()
   }
   dependencies {
       classpath 'com.android.tools.build:gradle:3.0.1'
       classpath 'com.google.gms:google-services:3.1.1'
   }
}

allprojects {
   repositories {
       jcenter()
       google()
       maven {
           url "http://107.155.116.28:8086/artifactory/libs-release-local"
       }
   }
}
```

 In your app-level build.gradle file:

```javascript
dependencies {
 implementation fileTree(dir: 'libs', include: ['*.jar'])
implementation 'com.android.support:design:27.1.1'
implementation 'com.android.support:appcompat-v7:27.1.1'
implementation 'com.android.support:multidex:1.0.3'
implementation 'com.android.support:support-emoji-appcompat:27.1.1'
implementation('io.socket:socket.io-client:1.0.0') {
   exclude group: 'org.json', module: 'json'
}
implementation 'com.acquireio:core:1.+'

}

```

 Your App level gradle file will look like this :

```javascript
android {
   compileSdkVersion 26
   buildToolsVersion "26.0.2"
   defaultConfig {
       applicationId "you-package-name"
       minSdkVersion 21
       targetSdkVersion 26
       multiDexEnabled true
       versionCode 1
       versionName "1.0"
   }
   buildTypes {
       release {
           minifyEnabled false
           proguardFiles getDefaultProguardFile('proguard-android.txt'),     'proguard-rules.pro'
       }
   }
}

dependencies {
 implementation fileTree(dir: 'libs', include: ['*.jar'])
implementation 'com.android.support:design:27.1.1'
implementation 'com.android.support:appcompat-v7:27.1.1'
implementation 'com.android.support:multidex:1.0.3'
implementation 'com.android.support:support-emoji-appcompat:27.1.1'
implementation('io.socket:socket.io-client:1.0.0') {
   exclude group: 'org.json', module: 'json'
}
implementation 'com.acquireio:core:1.+'
}

```

{% hint style="danger" %}
 **IMPORTANT** : To reduce apk size \(e.g. for release version\). use  " `'`**`com.acquireio:core-arm-v7a:1.+`**`'` " instead of " `'`**`com.acquireio:core:1.+`**`'` ". It will support nearly all devices.
{% endhint %}

```text

```

