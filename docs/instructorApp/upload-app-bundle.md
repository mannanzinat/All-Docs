Upload the app bundle to App Store Connect
Run flutter build ipa to produce an Xcode build archive .xcarchive file in your project’s build/ios/archive/directory and an App Store app bundle (.ipa file) in build/ios/ipa.

Once the app bundle is created, upload it to App Store Connect by either:

If you are not distributing to the App Store, you can optionally choose a different export method --export-method ad-hoc, --export-method development --export-method ad-hoc, --export-method development or --export-method enterprise.

Install and open the Apple Transport macOS . Drag and drop the build/ios/ipa/*.ipa app bundle into the app.
upload the app bundle from the command line by running:
xcrun altool --upload-app --type ios -f build/ios/ipa/*.ipa --apiKey your_api_key --apiIssuer your_issuer_id


Run man altool for details about how to authenticate with the App Store Connect API key.

Or open build/ios/archive/MyApp.xcarchive in Xcode.
Click the Validate App button. If any issues are reported, address them and produce another build. You can reuse the same build ID until you upload an archive
