

# Ionic-5-with-Angular-11 blank

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 11.0.0 and [Ionic Framework - Ionic Documentation](https://ionicframework.com/docs).

## Prerequisite

* Internet
* [Node 14.15.1](https://nodejs.org/en/download/)
* npm 6.14.8
* [Java SE Development Kit 8 - Downloads (oracle.com)](https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html)
* [Gradle | Installation](https://gradle.org/install/)
* [Download Android Studio and SDK tools | Android Developers](https://developer.android.com/studio)
* [Android Development - Ionic Documentation (ionicframework.com)](https://ionicframework.com/docs/developing/android)

> If you have an older version of Node.js and NPM, please update it.

## Installation

To see or use this application, you need to clone the base Ionic-5-with-Angular-11 repository from Github. Following the steps below will guide you to install the latest Ionic-5-with-Angular-11 version.

```
git clone --depth 1 https://github.com/teja8352/Ionic-5-with-Angular-11.git 
cd cd Ionic-5-with-Angular-11/
npm install  
ionic serve
```
If all the packages and modules installed successfully, the default web browser will open and you can see the default Ionic-5-with-Angular-11 application at `http://localhost:8100`. 

## Add Platforms
Run this below commands inside `Ionic-5-with-Angular-11/`
#### Add Android Platform
###### Debug Build
```
ionic cordova platform add android 
ionic cordova build android --prod --aot
```
**Note:**  Run `npm i -g cordova-res`  if any warning occurs for cordova-res then build the project.
###### Release Build
```
ionic cordova platform add android 
ionic cordova build android --prod --aot --release
keytool -genkey -v -keystore my-release-key.keystore -alias alias_name -keyalg RSA -keysize 2048 -validity 10000
jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore my-release-key.keystore HelloWorld-release-unsigned.apk alias_name
zipalign -v 4 HelloWorld-release-unsigned.apk HelloWorld.apk
```

#### Add IOS Platform
```
ionic cordova platform add ios 
ionic cordova build ios --prod --aot
From here, open the `.xcworkspace` file in `./platforms/ios/` to start Xcode.
```
 `resources`, `plugins`, `platforms\android`,  `platforms\ios`, `config.xml` will be created after adding the platform
 

 - resources - Where Application Logos and Splash screens will generate
 - plugins - Cordova plugins will be added to this folder when they installed
 - platforms - Android and IOS project/workspace will be added to this folder. 
 - config.xml - File to configure application name, id, permissions, etc. 

## Create a new Ionic project
Run this below commands to create new ionic project with Angular 11
```
npm install -g @angular/cli@latest @ionic/cli@latest cordova@latest
ionic start Ionic-5-with-Angular-11 blank --type=angular
cd Ionic-5-with-Angular-11/
ng update @angular/cli @angular/core rxjs
ionic serve
```
