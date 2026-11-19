# sapi BCA sandbox test, complete overlay

Copy these files over the existing sapi repository. Existing Gradle files and GitHub Actions can stay.

Uses BCA SNAP OAuth B2B and Banking Balance Inquiry from the BCA Developer API documentation updated 17 March 2025 and Sandbox Guide v1.1, April 2025: https://developer.bca.co.id/en/Dokumentasi

```bash
cd backend
cp env-template.txt .env
openssl rand -hex 32   # save only in TESTER_TOKEN
# Fill BCA sandbox values locally. Never commit or share credentials/private keys.
npm run check
npm start
adb reverse tcp:8787 tcp:8787
```

Build the Android APK as before. Paste only TESTER_TOKEN into the app. BCA success requires responseCode 2001100. The backend is sandbox-only, loopback-only, redacts identity fields, and exposes no transfer endpoint.
