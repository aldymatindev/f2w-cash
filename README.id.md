# f2w-cash

**Aplikasi keuangan pribadi yang privat dan bisa offline, untuk Android dan Windows.**
Data uangmu tetap di perangkatmu. Tidak wajib membuat akun.

[English](README.md) · [Fitur](docs/FEATURES.md) · [Instalasi](docs/INSTALL.md) ·
[Privasi](PRIVACY.md) · [Keamanan](SECURITY.md)

## Kenapa f2w-cash

- **Data di perangkatmu sendiri.** Transaksi, akun, budget, dan foto disimpan di database
  lokal terenkripsi. Tidak ada yang diunggah kecuali kamu menyalakan sinkron Google Drive.
- **Bisa offline.** Mencatat, laporan, budget, scan struk, dan asisten chat jalan tanpa internet.
- **Tanpa iklan, tanpa pelacak, tanpa SDK analitik.**
- **AI lokal.** Tanya "pengeluaran bulan ini berapa?" atau ketik "makan bakso 25rb kemarin
  pakai gopay"; asisten menjawab dari datamu di HP. Model bahasa opsional berjalan di perangkat.

## Unduh

Ambil versi terbaru di **[Releases](../../releases)**:

- Android (kebanyakan HP): `f2w-cash-<versi>-arm64-v8a.apk`
- Android 32-bit lama: `f2w-cash-<versi>-armeabi-v7a.apk`
- Windows 10/11 64-bit: `f2w-cash-<versi>-windows-x64.zip` (ekstrak, jalankan `f2w_cash.exe`)

Selalu cocokkan SHA-256 file dengan `SHA256SUMS.txt` di halaman rilis
(lihat [Instalasi](docs/INSTALL.md)). Aplikasi juga tersedia di Google Play.

## Privasi singkat

Tidak ada server f2w-cash yang menyimpan data keuanganmu. Fitur opsional menghubungi pihak
ketiga hanya saat kamu memakainya: Google Sign-In & Google Drive (Drive milikmu sendiri),
Google Play / RevenueCat (status Pro), API kurs, API harga investasi, dan unduhan model AI
lokal. Rincian lengkap (bahasa Inggris): [PRIVACY.md](PRIVACY.md).

## Dukungan

Buka [issue](../../issues) untuk bug atau saran. **Jangan** unggah screenshot yang
menampilkan saldo atau catatan transaksi. Masalah keamanan dilaporkan secara privat sesuai
[SECURITY.md](SECURITY.md).
