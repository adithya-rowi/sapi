# sapi

Minimal Android Hello World app.

## Requirements

- JDK 17
- Android SDK 35
- Gradle 8.9

## Build

```bash
gradle :app:assembleDebug
```

APK output:

```text
app/build/outputs/apk/debug/app-debug.apk
```

Pushing to GitHub also runs the included GitHub Actions workflow and publishes `sapi-debug-apk` as a workflow artifact.
