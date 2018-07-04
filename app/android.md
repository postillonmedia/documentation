# Android

## Commands

**Open Dev-Menu**  
`adb shell input keyevent 82`


**Reload Application**  
`adb shell am broadcast -a react.native.RELOAD`


## Intent-Filter

**Steady**  
Filter: `postillon://steady-auth`  
Command: `adb shell am start -W -a android.intent.action.VIEW -d "postillon://steady-auth" com.postillon`  


**Article**  
Filter: `postillon://article`  
Command: `adb shell am start -W -a android.intent.action.VIEW -d "postillon://article" com.postillon`  


**Web**  
Filter:
 * `http(s)://der-postillon.com`
 * `http(s)://www.der-postillon.com`
 * `http(s)://the-postillon.com`
 * `http(s)://www.the-postillon.com`

Command: `adb shell am start -W -a android.intent.action.VIEW -d "http://der-postillon.com/2018/02/milliardenboni.html" com.postillon`


## Release
This project uses Gradle 4.4 to build the APK file.
To build the APK follow the steps, starting in the root directory of this project:

1. `cd android`

2. `gradlew assembleRelease --console plain`

3. `cd ..`

4. The generated APK-File needs to be signed. An unsigned APK-File can not be installed. To sign an APK you must create a keystore-File.  
Windows:
```cmd
jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore postillon.keystore android\app\build\outputs\apk\release\app-release-unsigned.apk postillon
```
Unix:
```shell
jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore postillon.keystore android/app/build/outputs/apk/release/app-release-unsigned.apk postillon
```
