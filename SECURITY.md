# Security

## Verify what you download

Every release lists a `SHA256SUMS.txt`. Check the file before installing:

**Windows (PowerShell)**
```powershell
Get-FileHash .\f2w-cash-1.0.33-windows-x64.zip -Algorithm SHA256
```

**Android / Linux / macOS**
```bash
sha256sum f2w-cash-1.0.33-arm64-v8a.apk
```

The hash must match the line in `SHA256SUMS.txt`. If it does not, do not install it.
Only download from this repository's **Releases** page or Google Play.

Android APKs are signed with the developer's release key. Installing an update over an
existing installation only works when the signature matches, which protects against a
modified APK replacing the app.

The Windows build is **not code-signed** yet. Windows SmartScreen may show "Windows
protected your PC". Verify the checksum first, then choose _More info → Run anyway_.

## How your data is protected

- **Encrypted database.** All records are stored in an AES-256 encrypted local database.
  The key is generated on the device and kept in secure storage (Android Keystore /
  Windows Credential Manager). It never leaves the device.
- **App lock.** Optional passcode (stored only as a salted, iterated hash; compared in constant time) and biometrics,
  with automatic lock after a chosen time in the background and a delay after wrong attempts.
- **No app-data cloud backup** by the OS (`allowBackup=false`).
- **Least-privilege Google Drive access** (`drive.file`): the app can only read files it created.
- **Local-only PC Manager** bound to `127.0.0.1` with a random session token and 30-minute
  expiry.
- **On-device AI and OCR.** Questions to the assistant and receipt images are processed
  on the device.
- **Release builds** are obfuscated and contain no debug switches that unlock paid
  features.

### Public identifiers inside the apps

Like every app that uses Google sign-in, Firebase, and RevenueCat, the builds contain
**public** client identifiers (Firebase API key / app ID, OAuth client ID, the RevenueCat
public SDK key, and on Windows the OAuth desktop client secret, which Google documents as
not confidential for installed apps). They identify the app, not a user, and they cannot
read anyone's data. Access is restricted on the provider side (API key restrictions,
OAuth consent, `drive.file` scope).

## Known limitations

- Local backup files you export (JSON/CSV) are not encrypted. Keep them private.
- A forgotten app passcode cannot be recovered; the local data must then be reset (restore
  from your backup or Google Drive).
- Pro purchases are tied to Google Play. An APK from this repository uses Google Play
  billing too, but the Play Store version is the most reliable way to buy or restore Pro.

## Reporting a vulnerability

Please **do not** open a public issue for security problems. Use GitHub's
**"Report a vulnerability"** (Security tab → Advisories) on this repository. Include steps
to reproduce and the app version. You will get a response as soon as possible; please allow
time for a fix before public disclosure.
