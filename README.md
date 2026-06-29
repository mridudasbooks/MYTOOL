# MRIDUDAS Android App

A WebView wrapper for the MRIDUDAS Offline Library.

## Build Instructions

### Prerequisites
- Android Studio Hedgehog (2023.1) or newer
- JDK 17
- Android SDK 34

### Steps

1. **Open in Android Studio**
   File → Open → select this folder

2. **Sync Gradle**
   Android Studio will download the Gradle wrapper automatically.

3. **Build APK**
   Build → Build Bundle(s) / APK(s) → Build APK(s)
   The output APK will be at:
   `app/build/outputs/apk/debug/app-debug.apk`

4. **Build Release APK**
   - Generate a signing keystore if needed:
     `keytool -genkey -v -keystore mridudas.keystore -alias mridudas -keyalg RSA -keysize 2048 -validity 10000`
   - Configure signing in `app/build.gradle` under `signingConfigs`
   - Build → Generate Signed Bundle / APK

### AIDE (Android IDE on Phone)
1. Open AIDE → Import Project → select this folder
2. Build & Run

### Command Line
```bash
./gradlew assembleDebug
# APK → app/build/outputs/apk/debug/app-debug.apk
```

## Features
- Full offline operation – all assets loaded from `assets/www/`
- IndexedDB, DOM Storage, WebSQL enabled
- File picker for images / audio / PDFs
- Download support for exported backups
- Hardware-accelerated rendering
- Back-button WebView navigation
- Immersive / edge-to-edge display

## Package Details
| Item | Value |
|------|-------|
| Package | com.mridudas.library |
| Min SDK | 21 (Android 5.0) |
| Target SDK | 34 (Android 14) |
| Version | 1.0 (code 1) |
