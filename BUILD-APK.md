# JARVIS — Shihan's Personal AI Operating System

## Build an installable Android APK with EAS

Requirements:
- Node.js 20+ recommended
- npm (pnpm is optional; the project includes `pnpm-lock.yaml`)
- An Expo/EAS account

From this folder:

```bash
npm install -g eas-cli
npm install
npx eas login
npx eas build --platform android --profile preview
```

The `preview` profile is configured to produce an installable APK (`buildType: apk`).

### If using pnpm

```bash
corepack enable
corepack prepare pnpm@9.12.0 --activate
pnpm install --frozen-lockfile
npx eas login
npx eas build --platform android --profile preview
```

### Important

The app's server-side AI/voice features require their corresponding backend environment variables and services. The APK can still be built without exposing those secrets in the source archive; configure required server secrets in the deployment environment rather than committing them to the project.
