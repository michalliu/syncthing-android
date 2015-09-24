# syncthing-android

[![Build Status](http://android.syncthing.net/job/Syncthing-Android/badge/icon)](http://android.syncthing.net/job/Syncthing-Android/)
[![tip for next commit](https://tip4commit.com/projects/914.svg)](https://tip4commit.com/github/syncthing/syncthing-android)

A wrapper of [Syncthing](https://github.com/syncthing/syncthing) for Android.

<img src="market/screenshot_phone_1.png" alt="screenshot 1" width="200" /> 
<img src="market/screenshot_phone_2.png" alt="screenshot 2" width="200" /> 
<img src="market/screenshot_phone_3.png" alt="screenshot 3" width="200" />

[![Get it on Google Play](https://developer.android.com/images/brand/en_generic_rgb_wo_60.png)](https://play.google.com/store/apps/details?id=com.nutomic.syncthingandroid) [![Get it on F-Droid](https://f-droid.org/wiki/images/0/06/F-Droid-button_get-it-on.png)](https://f-droid.org/repository/browse/?fdid=com.nutomic.syncthingandroid)

# Translations

The project is translated on [Transifex](https://www.transifex.com/projects/p/syncthing-android/).

Translations can be updated using the [Transifex client](http://docs.transifex.com/developer/client/), using commands `tx push -s` and `tx pull -a`.

# Building

### Requirements
- Android SDK Platform (for the `compileSdkVersion` specified in [build.gradle](build.gradle))
- Android Support Repository

### Build instructions

Use `./gradlew assembleDebug` in the project directory to compile the APK.

To check for updated gradle dependencies, run `gradle dependencyUpdates`. Additionally, the git submodule in `ext/syncthing/src/github.com/syncthing/syncthing` may need to be updated.


### Building on Windows

To build the Syncthing app on Windows we need to include the native Syncthing binaries:
- Download the `syncthing-linux-386` and `syncthing-linux-arm` archives from [Syncthing releases](https://github.com/syncthing/syncthing/releases) and extract them. In each there is a `syncthing` executable. Rename and place both of these to `libs/x86/libsyncthing.so` and `libs/armeabi/libsyncthing.so` respectively.  
You will also need to replace the standard `build.gradle` file with [this one](https://gist.github.com/Moter8/9cfc191434d1989d86be).

# License

The project is licensed under the [MPLv2](LICENSE).
