OVERSTACK - PHONE APP (no web browser needed to install or play)

=== ANDROID (APK file) ===
You need a computer with:
- Node.js (LTS): https://nodejs.org
- Android Studio: https://developer.android.com/studio

1. Open a terminal in this folder and run:
     npm install
     npx cap add android
     npx cap sync
     npx cap open android
2. Android Studio opens. Wait until syncing finishes (bottom status bar).
3. Optional app icon: right-click "app" > New > Image Asset > pick icon-512.png from this folder.
4. Menu: Build > Build App Bundle(s) / APK(s) > Build APK(s). Click "locate" when done.
   The file is app-debug.apk.
5. Send the APK to friends WITHOUT a browser: WhatsApp, Discord, Telegram, Quick Share,
   or the Google Drive app. They tap the file, allow "Install unknown apps" for that app
   when Android asks, and it installs like any app.
   Note: if a phone has parental controls that block installing apps from outside the
   Play Store, it can only get the game through Google Play (needs a Play Console account).

=== IPHONE (TestFlight) ===
iPhones can't install APK files. You need a Mac with Xcode and the Apple Developer Program
(paid yearly membership).
1. In this folder on the Mac:  npm install, then  npx cap add ios,  npx cap sync,  npx cap open ios
2. In Xcode: select the "App" target > Signing & Capabilities > choose your Team.
3. Product > Archive, then Distribute App > App Store Connect > Upload.
4. In App Store Connect (appstoreconnect.apple.com) > your app > TestFlight, add your friends
   as testers using their Apple ID email.
5. Friends install the free "TestFlight" app from the App Store, then open TestFlight and
   tap "Redeem" with the code from their invite email. No browser needed.

=== Updating the game ===
Replace www/index.html with the new version, run  npx cap sync,  and build again.
Friends install the new APK over the old one (their save is kept), or get the TestFlight update.
