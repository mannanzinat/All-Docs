Create an app bundle
Run flutter build ipa to produce an Xcode build archive .xcarchive file in your project build/ios/archive/directory and an App Store app bundle (.ipa file) in build/ios/ipa.

Consider adding the --obfuscate and --split-debug-info flags to obfuscate your Dart code to make it more difficult to reverse engineer.

If you are not distributing to the App Store, you can optionally choose a different export method --export-method ad-hoc, --export-method development or --export-method enterprise.
