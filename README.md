Ponyville Live! Ionic/Cordova Mobile App
==========================

### Building

Install Node.js, then npm install Cordova and Ionic. Add local platforms using 'ionic platform add xxx' as per needed. Be sure to have the necessary prereqs for each platform (e.g. Android SDK for android and be on a mac computer for iOS)

Android Studio compatible project folder is located under "platforms/android/" - use this for platform specific tweaks to HTML or Plugin/Java code. Build APKs for release from here in Android Studio.

ALWAYS BE SURE TO UPDATE MAIN SOURCE (in "www/") if edited within the 'platforms/' folder. THAT IS THE MASTER REPO, and will overwrite the HTML source in the 'platforms/xxx' folders if ever re-compiled in Ionic/Cordova (see below).

### COMPILING FROM HTML SOURCE

FIRST: Working platforms builds are under the 'platforms' folder, and HTML/JS can be editted there without re-compiling in Ionic/Cordova. Only do this if there has been significant updates to the plugins used in the PVL project. There have been platform-specific edits to the cordova plugins (specially Media and LocalNotifications) THAT WILL BE OVERWRITTEN if the below instructions are done. You have been warned :)

Don't try to compile Android using Ionic ('ionic build android'), it doesn't support support multiDexEnabled in gradle build (as far as I can see). Use 'cordova prepare android' (for Android) instead to build to Platforms folder; continue working there as needed in Android Studio

XCode/iOS instructions to come.

