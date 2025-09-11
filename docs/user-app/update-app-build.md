# Update the app’s build and version numbers

The default version number of the app is 1.0.0. To update it, navigate to the pubspec.yaml file and update the following line:


version: 1.0.0+1
The version number is three numbers separated by dots, such as 1.0.0 in the example above, followed by an optional build number such as 1 in the example above, separated by a +

Both the version and the build number may be overridden in Flutter’s build by specifying --build-name and --build-number, respectively.

In iOS build-name uses CFBundleShortVersionString while build-number uses CFBundleVersion. Read more about iOS versioning at Core Foundation Keys on the Apple Developer’s site.

You may also override the pubspec.yaml build name and number in Xcode:

Open Runner.xcworkspace in your app’s ios folder.
Select Runner in the Xcode project navigator, then select the Runner target in the settings view sidebar.

In the Identity section, update the Version to the user-facing version number you wish to publish
In the Identity section, update the Build identifier to a unique build number used to track this build on App Store Connect. Each upload requires a unique build number.
