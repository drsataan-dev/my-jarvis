# JARVIS — Shihan | Android-ready project

This is an Expo/EAS Android-ready build of JARVIS. It is configured to produce an installable `.apk` without requiring you to create a native Android project by hand.

## Fastest APK build

Requirements:
- Node.js 20+
- An Expo account
- EAS CLI

From this folder:

```bash
npm install -g eas-cli
npm install
npx eas login
npx eas build --platform android --profile apk
```

The `apk` profile is explicitly configured as `buildType: apk`.

### Using pnpm

```bash
corepack enable
corepack prepare pnpm@9.12.0 --activate
pnpm install --frozen-lockfile
npx eas login
npx eas build --platform android --profile apk
```

EAS will build the APK in the cloud and provide a download URL when the build completes.

## Project configuration

- App name: `JARVIS — Shihan's Personal AI Operating System`
- Android package: `com.app.jarvisshihan`
- Expo SDK: 54
- React Native: 0.81.x
- Android minimum SDK: 24
- Architectures: `armeabi-v7a`, `arm64-v8a`
- Installable APK profile: `apk`
- Internal distribution profile: `preview`

## Important

The app contains server-side AI/voice functionality. API credentials and backend secrets should be supplied through the deployment environment, never hard-coded into the APK or committed to source control.

This archive is intentionally source-only; it does not contain signing credentials or private API keys.
