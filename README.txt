REALME INCENTIVE — ANDROID / iOS SOURCE PROJECT
================================================

This is a Capacitor wrapper project prepared from the HTML source you uploaded.
The existing Netlify website is not changed. The Supabase project URL and public
publishable key already present in the source HTML are retained. No service-role
key was found in the supplied HTML.

APP IDENTITY
- Display name: Realme Incentive
- Android application ID / iOS Bundle ID: com.realme.incentive

IMPORTANT
- This package is the source project, not a compiled APK or signed iPhone IPA.
- Android APK compilation requires Android Studio + Android SDK.
- iOS compilation/signing requires a Mac with Xcode. App Store distribution
  additionally requires an Apple Developer account.
- The app still needs internet for Supabase, CDN libraries, login, data sync,
  and admin upload. Offline mode is not a substitute for cloud access.

BUILD ANDROID
1. Install Node.js LTS and Android Studio (with Android SDK).
2. Extract this project.
3. Open a terminal in the project folder and run:
      npm install
      npx cap add android
      npx cap sync android
      npx cap open android
4. In Android Studio, wait for Gradle sync.
5. For a test build: Build > Build Bundle(s) / APK(s) > Build APK(s).
6. For a distributable release: Build > Generate Signed Bundle / APK >
   APK, then create/choose a signing key and build the release APK.

BUILD iOS (Mac only)
1. Install Node.js LTS and Xcode.
2. In the project folder run:
      npm install
      npx cap add ios
      npx cap sync ios
      npx cap open ios
3. In Xcode, configure Signing & Capabilities with your Apple Developer team.
4. Test on a device, then archive and distribute using the intended Apple route.

WHEN HTML CHANGES
Replace www/index.html with the updated app HTML, then run:
      npx cap sync

SAFETY / DEPLOYMENT
- Do not upload this project over the existing web site's Netlify site.
- This is a separate native-app project. The existing website remains independent.
- Test promoter login, admin login, Supabase reads/writes, Excel upload,
  incentive values, stock validation, ASP, and all language modes before release.
- Do not put Supabase service-role credentials in client-side code.
