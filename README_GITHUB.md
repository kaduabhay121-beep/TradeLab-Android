# TradeLab Android v1 — GitHub APK Builder

This project is a lightweight Android WebView client for the existing TradeLab v2.8 paper-trading web application.

## Build an APK from a phone — no Android Studio required

1. Create a new GitHub repository, for example `tradelab-android`.
2. Upload **all contents inside this folder** to the repository root (including `.github/workflows/build-apk.yml`).
3. Open the repository on GitHub.
4. Open **Actions** → **Build TradeLab APK**.
5. Tap **Run workflow** if the workflow has not already run from your push.
6. Wait for the green build to finish.
7. Open the completed workflow run and scroll to **Artifacts**.
8. Download **TradeLab-v1-APK**. GitHub provides a ZIP containing `TradeLab-v1-debug.apk`.
9. Extract the ZIP on your phone and install the APK.

The workflow uses GitHub's hosted Ubuntu runner, Java 17, Android SDK 35 and Gradle 8.7. No Android Studio is required on the phone.

## Important

- This is a **debug APK** for personal/sideloaded use.
- It does not contain Angel One API credentials.
- The APK connects to the configured TradeLab web backend over HTTPS.
- Trading remains paper/simulated; the Android wrapper does not add real-order functionality.
- GitHub Actions availability/limits depend on your GitHub account and repository settings.

## Updating the app

Change the Android project, commit/push to GitHub, and the workflow will build a fresh APK automatically.
