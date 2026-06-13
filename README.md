# 360 Android App

## Fastest way to get the APK (5 minutes)

### Option A — GitHub Actions (easiest, no setup)

1. Push this folder to a new GitHub repo
2. Go to **Actions** tab → the build runs automatically
3. When it finishes, click the run → **Artifacts** → download `360-debug.apk`
4. Transfer to your Galaxy and install

The workflow also creates a **Release** automatically with the APK attached.

---

### Option B — Build locally with Android Studio

1. Open Android Studio → File → Open → select this folder
2. Wait for Gradle sync (~2 min first time)
3. Build → Build Bundle(s) / APK(s) → Build APK(s)
4. APK will be at: `app/build/outputs/apk/debug/app-debug.apk`

---

### Option C — Command line (if you have Android SDK installed)

```bash
chmod +x gradlew
./gradlew assembleDebug
# APK: app/build/outputs/apk/debug/app-debug.apk
```

---

## Installing on Galaxy

1. Settings → Apps → Special app access → Install unknown apps
2. Enable for your file manager / browser
3. Tap the APK → Install

## What's in the app

- Full Android-redesigned UI (bottom nav, native feel)
- Bundled entirely in the APK — works offline
- Search, AI chat (calls your Supabase edge function), weather, games, settings
- 6 color themes + dark mode
- Your app icon + "360" name
