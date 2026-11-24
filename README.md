# Jarvis - Hinglish AI Voice Assistant (Android)

Kotlin + XML app. Gemini (`gemini-2.5-flash`) brain, offline commands, AccessibilityService automation,
notification reader, foreground service, wake word ("Jarvis ...").

## APK GitHub pe build karo (PC/Termux ki zaroorat nahi)
1. Repo me push karo (branch `main`).
2. **Actions** tab -> *Build Jarvis APK* -> run complete hone do.
3. Run page ke **Artifacts** se `Jarvis-debug-apk` download karo.
4. Release chahiye? `git tag v1.0 && git push origin v1.0` -> APK Releases me aa jayega.

## Termux me build
```bash
pkg install openjdk-17 aapt2 gradle
echo "android.aapt2FromMavenOverride=/data/data/com.termux/files/usr/bin/aapt2" >> ~/.gradle/gradle.properties
echo "sdk.dir=$HOME/android-sdk" > local.properties
gradle assembleDebug
```

## Pehli baar setup (app ke Settings me)
Gemini API key paste karo, phir Accessibility, Notification access, Overlay aur Battery optimisation enable karo.
**API key kabhi repo me commit mat karo.** Wo app ke andar encrypted store hoti hai.
