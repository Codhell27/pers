# PERSONAL OS — One-click online APK build

This project is a **local-only Android APK**:
- No Firebase
- No login/account
- No network permission
- Inventory, stats, and journal are stored locally in the Android WebView
- Export/import backup is included

## Build online with GitHub Actions

1. Create a GitHub repository.
2. Upload the contents of this project so `app/`, `build.gradle`, `settings.gradle`,
   `gradle.properties`, and `.github/` are at the repository root.
3. Open **Actions**.
4. Select **Build Personal OS APK**.
5. Click **Run workflow**.
6. Open the completed workflow run.
7. Under **Artifacts**, download `PersonalOS-APK`.
8. Extract it and install `app-debug.apk` on your Android phone.

## Important

Do not upload `node_modules`. This Android project does not use Node.js or npm.

This version intentionally uses only the Android platform APIs and does not depend on
AndroidX/AppCompat, avoiding Kotlin stdlib dependency conflicts in the online build.
