# React-Native-A-to-Z
React Native A to Z

# Basic Setup for mac:

export ANDROID_HOME=/Users/lover/Library/Android/sdk
export PATH=${PATH}:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools
export PATH=${PATH}:$ANDROID_HOME/tools:$ANDROID_HOME/emulator
export PATH=${PATH}:$ANDROID_HOME/tools:$ANDROID_HOME/tools
export PATH=${PATH}:$ANDROID_HOME/tools:$ANDROID_HOME/tools/bin



Bundle debug build:

#React-Native 0.49.0+
react-native bundle --dev false --platform android --entry-file index.js --bundle-output ./android/app/build/intermediates/assets/debug/index.android.bundle --assets-dest ./android/app/build/intermediates/res/merged/debug

#React-Native 0-0.49.0
react-native bundle --dev false --platform android --entry-file index.android.js --bundle-output ./android/app/build/intermediates/assets/debug/index.android.bundle --assets-dest ./android/app/build/intermediates/res/merged/debug
Then to build the APK's after bundling:

$ cd android
#Create debug build:
$ ./gradlew assembleDebug

#Create release build:
$ ./gradlew assembleRelease 
#Generated `apk` will be located at `android/app/build/outputs/apk`

https://medium.com/@adityasingh_32512/solved-unable-to-load-script-from-assets-index-android-bundle-bdc5e3a3d5ff
