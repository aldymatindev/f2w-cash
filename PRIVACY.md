# Privacy

_Last updated: 2026-11-19 · applies to f2w-cash 1.0.33 and later._

f2w-cash is built so that **your financial data never has to leave your device**. There is
no f2w-cash server that receives or stores your transactions, balances, notes, or photos.

## What is stored, and where

| Data | Location | Protection |
|---|---|---|
| Transactions, accounts, categories, budgets, loans, goals, settings, chat history | App-private database on the device (Hive) | Encrypted (AES-256); the key is kept in Android Keystore / Windows Credential Manager via secure storage |
| Receipt and goal photos | App-private folder `images/` | Private to the app (Android sandbox / your Windows user profile) |
| Compressed data snapshot (on logout) and sync cache | App-private folder `db/` | Private to the app |
| Local backups you create (JSON/CSV) | Android: `Android/media/net.f2w.cash/backups` · Windows: `Documents\f2w-cash\backups` | **Not encrypted** — readable by anyone with access to the file. Store and share them carefully |
| Exports (CSV/PDF/Excel) you share | Wherever you send them | Leave the app only when you choose to share |
| Downloaded AI models | App-private storage | Model files only, no personal data |

Android system backup of app data is **disabled** (`allowBackup=false`), so the encrypted
database is not copied to Google's device backup.

## Network use (only when you use the feature)

| Feature | Service | What is sent |
|---|---|---|
| Sign in with Google (optional) | Google Sign-In, Firebase Authentication | Your Google account identity |
| Google Drive sync / backup (optional) | Google Drive API | Your data file and photos, to **your own** Drive, in folder `f2w-cash`. Scope `drive.file`: the app can only see files it created |
| Pro subscription | Google Play Billing, RevenueCat | Purchase status and an anonymous app user ID. No financial data |
| Release notes in the app | Firebase Remote Config | Standard request metadata; no personal data |
| Exchange rates (multi-currency) | open.er-api.com | Currency codes only |
| Investment prices | Yahoo Finance, pasardana.id | Ticker / fund symbols only |
| Receipt scan (Android) | Google ML Kit via Play Services | **Nothing** — text recognition runs on the device. The model is downloaded by Play Services |
| Voice input | Your device's speech recognizer | Handled by the system service (on many Android phones this is Google's speech service) |
| Local AI model download (optional) | Hugging Face (LiteRT-LM catalog) | The model file request only. Questions and data are **never** sent; the model runs on the device |
| App update check (Android) | Google Play | Standard Play update check |

f2w-cash contains **no advertising SDK and no analytics SDK**. Crashes are not reported to
any server.

## PC Manager (browser access)

The built-in PC Manager web page listens only on `127.0.0.1` (this device). It is not
reachable over Wi-Fi. Access needs a random session token, and the session ends after
30 minutes.

## Permissions (Android)

| Permission | Why |
|---|---|
| Internet | Optional online features listed above |
| Camera, photos | Receipt scanning and attaching photos (only when you choose to) |
| Microphone | Voice input for notes (only when you tap the mic) |
| Biometric | App lock |
| Notifications, run at boot | Budget, bill, and savings reminders (scheduled locally) |
| Billing | Pro subscription through Google Play |
| Advertising ID (`AD_ID`) | Declared in the manifest; f2w-cash has no ad or analytics SDK and does not read or use the advertising ID |

## Deleting your data

- **Logout and clear this device** in Settings removes all local data (after an optional sync).
- Uninstalling the app removes the encrypted database and app-private files.
  Local backups in `Android/media/...` or `Documents\f2w-cash\backups` stay until you delete them.
- Data in your Google Drive is under your control; delete the `f2w-cash` folder there.

## Children

f2w-cash is not directed at children under 13.

## Contact

Questions about privacy: open an issue in this repository (without personal data), or use
the contact in [SECURITY.md](SECURITY.md) for sensitive matters.
