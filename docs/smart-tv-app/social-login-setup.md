---
title:   Social Login

sidebar_label:   Social Login Setup
---

# Setup Google login for Android

&nbsp;

You have to create Firebase project first __[See Tutorial]__ if you did not created yet.

[See Tutorial]: http://192.168.1.54/website-laravel/docs/google-firebase-setup-nvg7h



Video tutorial

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/xDGEE6J55kw/0.jpg)](https://www.youtube.com/watch?v=xDGEE6J55kw)

OR follow bellow step:

Go Firebase console then navigation to Authentication Sign in Method.

Select Android.
Provide Android Package name.
Register App.
Remove existing google Google-service.json 
and download and update googleService.json file inside android flider.
Hit skip this step.
Done!

# Setup Google login for iOS

Video tutorial

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/SLQewouovcs/0.jpg)](https://www.youtube.com/watch?v=SLQewouovcs)


OR follow bellow step:
Go Firebase console then navigation to Authentication Sign in Method .
Select IOS.
Provide iOS bundle id from PRODUCT_BUNDLE_IDENTIFIER.
Register App.
Remove existing google Google-serviceInfo.plist and download and update googleServiceInfo.plist file inside iOS flider.
Hit skip this step.
Copy REVERSED_CLIENT_ID from google-serviceInfo.plist GO IOS/Runner/info.plist update com.googleusercontent.apps.
Done!


# Setup Facebook login on Android


[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/VEe2kc8uIfw/0.jpg)](https://www.youtube.com/watch?v=VEe2kc8uIfw)



OR follow bellow step:
    - Select Facebook login.

- QuickStart > iOS > Next add Bundle ID (From iOS/Runner/ Runner.XcodeProj> Project.pbxproj find PRODUCT_BUNDLE)IDENTIFIER > Continue > Next > Update fb id from info.plist.

Update FacebookAppID then next .
Register App.
Update FacebookAppID then next .

Add Valid Auth Redirect URL.
Then Go fb settings/basic Add privacy policy url Terms of Service.
Then Save Changes.Choose Category.

Then Submit IN Development.
Go firebase console then add app id copy app secret from fb and add to firebase.
Done!

Setup Phone Login for Android
Goto Firebase console.
Navigation to Authentication Sign in Method.
Click and enable phone login.
Done!


# Setup Apple Login for iOS

Apple login is available for iOS only.
Goto Firebase console.
Navigation to Authentication Sign in Method.
Click and enable phone login.
Done!


Generate And Add SHA-Certificate Fingerprint
Generate SHA-Certificate Fingerprint by below command

# For mac

```keytool -list -v -keystore ~/.android/debug.keystore -alias androiddebugkey -storepass android -keypass 
android```


# For Windows

```keytool -list -v -keystore "\.android\debug.keystore" -alias androiddebugkey -storepass android -keypass android```

# Add SHA-Certificate Fingerprint to Firebase
First generate certificate and copy it.
Then goto project setting and add fingerprint.
All done!!!
