# Install

## Android (APK)

1. Download the APK for your phone from [Releases](../../../releases)
   (`arm64-v8a` fits almost all phones from 2017 on).
2. Verify the checksum (see [SECURITY.md](../SECURITY.md)).
3. Open the file. If Android asks, allow _Install unknown apps_ for your browser or file
   manager, then install.
4. Optional: turn that permission off again afterwards.

Updating: install the newer APK over the old one. Your data is kept.
If you installed from Google Play, keep updating through Google Play (the Play version and
the GitHub APK can be signed differently, so Android may refuse to install one over the
other without uninstalling — **uninstalling deletes local data**, so make a backup first).

Requirements: Android 7.0 (API 24) or newer. On-device AI models need Android 11+, a 64-bit
phone, and 4 GB RAM or more (8 GB+ recommended for larger models).

## Windows

1. Download `f2w-cash-<version>-windows-x64.zip` from [Releases](../../../releases).
2. Verify the checksum.
3. Right-click the zip → _Extract All_. Keep all files together.
4. Run `f2w_cash.exe`. If SmartScreen appears, choose _More info → Run anyway_
   (the build is not code-signed yet).

Data location on Windows: `%APPDATA%` / `Documents\f2w-cash` (encrypted database, photos,
backups). Updating: extract the new version over the old folder or into a new folder;
your data is stored separately and is kept.

Requirements: Windows 10/11 64-bit. Receipt OCR on Windows uses the bundled Tesseract files
in the `ocr` folder.

## Moving to a new device

Use **Backup** (local JSON) or **Google Drive sync**, then restore on the new device.
