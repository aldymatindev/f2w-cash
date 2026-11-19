# f2w-cash

**Private, offline-first personal finance app for Android and Windows.**
Your money data stays on your device. No account is required to use it.

[Bahasa Indonesia](README.id.md) · [Features](docs/FEATURES.md) · [Install](docs/INSTALL.md) ·
[Privacy](PRIVACY.md) · [Security](SECURITY.md) · [Changelog](CHANGELOG.md)

---

## Why f2w-cash

- **Your data, your device.** Transactions, accounts, budgets, and photos are stored in an
  encrypted local database on your phone or PC. Nothing is uploaded unless you turn on
  Google Drive sync yourself.
- **Works offline.** Recording, reports, budgets, receipt scanning, and the finance chat
  assistant all work without internet.
- **No ads, no trackers, no analytics SDK.**
- **Local AI.** Ask "how much did I spend this month?" or type "lunch 25k yesterday with
  gopay" and the assistant answers from your own data on the device. Optional language
  models run fully on-device.

## Download

Get the latest version from **[Releases](../../releases)**.

| Platform | File | Notes |
|---|---|---|
| Android 7.0+ (most phones) | `f2w-cash-<version>-arm64-v8a.apk` | Recommended |
| Android (older 32-bit phones) | `f2w-cash-<version>-armeabi-v7a.apk` | |
| Android emulator / x86 | `f2w-cash-<version>-x86_64.apk` | |
| Windows 10/11 64-bit | `f2w-cash-<version>-windows-x64.zip` | Unzip and run `f2w_cash.exe` |

The app is also published on Google Play. Always verify the SHA-256 checksum of a
download against `SHA256SUMS.txt` in the release — see [Install](docs/INSTALL.md).

## Highlights

- Income, expense, and transfer tracking with categories, sub-categories, splits, and
  multiple accounts and currencies (automatic conversion when you change your main currency).
- Budgets, savings goals with auto-deposit, loans, bills, recurring transactions,
  challenges, and family profiles.
- Calendar, daily, monthly, and summary views; statistics, insights, and spending forecast.
- Receipt scanning (OCR) on the device; bank statement import (CSV/PDF).
- Export to CSV, PDF, and Excel; local backup and optional Google Drive sync.
- App lock with passcode and biometrics.
- English and Indonesian.

Full list: [docs/FEATURES.md](docs/FEATURES.md).

## Privacy in one paragraph

f2w-cash does not run a server that stores your finances. Data is kept in an encrypted
database on your device. Optional features contact third parties only when you use them:
Google Sign-In and Google Drive (your own Drive, `drive.file` scope only), Google Play /
RevenueCat (Pro subscription status), an exchange-rate API, market price APIs for
investments, and model downloads for local AI. Details: [PRIVACY.md](PRIVACY.md).

## Support

Open an [issue](../../issues) for bugs and suggestions. Please do **not** post screenshots
that show your balances or transaction notes. Report security problems privately as
described in [SECURITY.md](SECURITY.md).
