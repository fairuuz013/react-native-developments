1. Konsep Dasar React Native sebagai Framework Cross-Platform

React Native adalah framework cross-platform yang dikembangkan oleh Meta untuk membangun aplikasi mobile native (Android & iOS) menggunakan bahasa JavaScript dan library React.
Konsep utamanya adalah "Learn once, write anywhere" — kode logika dan UI ditulis dengan React, lalu dijalankan secara native melalui bridge yang menghubungkan JavaScript dan komponen native Android/iOS.

Perbedaan React Native vs React (Web)
Aspek React (Web) React Native
Platform Browser (DOM) Android & iOS
Elemen UI <div>, <span>, <p> <View>, <Text>, <Image>
Rendering Virtual DOM di browser Native UI melalui bridge
Styling CSS StyleSheet (mirip CSS-in-JS)
Output Website Aplikasi mobile native
New Architecture di React Native v0.80

React Native v0.80 memperkenalkan New Architecture yang menggantikan old bridge system dengan tiga komponen utama:

Fabric Renderer → rendering UI lebih cepat dan efisien.

TurboModules → modul native dimuat secara lazy (sesuai kebutuhan), mengurangi waktu startup aplikasi.

JSI (JavaScript Interface) → menghilangkan serialization data antara JS dan native, sehingga komunikasi langsung (tanpa overhead).

👉 Dampak: Performa aplikasi meningkat signifikan — UI lebih responsif, waktu muat lebih cepat, dan konsumsi memori lebih efisien.

2. Perbandingan React Native CLI vs Expo
   Aspek React Native CLI Expo
   Arsitektur Build langsung ke native Android/iOS melalui Gradle/Xcode. Build di atas React Native + layanan Expo SDK dan build service.
   Proses Build Manual: developer mengatur environment, SDK, dan native config. Otomatis: build dilakukan oleh Expo (tanpa konfigurasi native).
   Kelebihan Akses penuh ke kode native, cocok untuk fitur kompleks (Bluetooth, sensor, modul kustom). Setup cepat, cocok untuk pemula & prototyping cepat.
   Kekurangan Setup rumit, perlu konfigurasi Android Studio/Xcode. Tidak fleksibel jika butuh native module custom (kecuali eject).
   Contoh Skenario

Pilih React Native CLI → ketika membangun aplikasi restoran dengan fitur pembayaran offline dan integrasi printer Bluetooth.
Alasan: butuh akses ke API native Android.

Pilih Expo → untuk aplikasi katalog menu sederhana yang hanya menampilkan gambar dan teks.
Alasan: tidak butuh konfigurasi native, lebih cepat untuk MVP.

3. Komponen SDK Android dalam Environment CLI
   Komponen Fungsi Masalah jika tidak ada
   SDK Platforms (android-35) Berisi API level yang digunakan untuk compile dan run aplikasi. Error: "failed to find target with API level 35" saat build.
   Build Tools (35.0.0) Menyediakan aapt, dx, zipalign untuk membangun dan mengemas APK. Error: “No build tools found” atau “Task :app:compileDebugJavaWithJavac FAILED”.
   Platform Tools Berisi adb, fastboot untuk komunikasi antara PC dan perangkat/emulator. VS Code tidak bisa menjalankan npm run android karena perangkat tidak terdeteksi.

➡️ Jadi, ketiganya wajib ada agar proyek React Native bisa dibuild dan dijalankan lewat command-line.

4. Prasyarat Setup React Native CLI v0.80
   Komponen Fungsi Alasan Diperlukan
   Node.js Menjalankan kode JavaScript di luar browser (server-side). React Native menggunakan Node untuk menjalankan Metro bundler dan proses build JS.
   Watchman (khusus macOS/Linux) Mendeteksi perubahan file secara real-time. Membuat reload otomatis dan cepat saat file diubah.
   Yarn / npm Package manager untuk mengelola dependensi proyek. Dibutuhkan untuk menginstal library dan modul JavaScript.

🧩 Ketiganya menjadi “jembatan” agar JavaScript bisa dijalankan dan disinkronkan dengan native runtime (Java/Kotlin untuk Android, Swift/Obj-C untuk iOS).

5. Struktur Folder Utama React Native CLI
   myApp/
   │
   ├── android/ # Kode native Android (Gradle, MainActivity.java, dll)
   ├── ios/ # Kode native iOS (Xcode project)
   ├── app.json # Konfigurasi aplikasi
   ├── package.json # Daftar dependensi & script npm
   ├── App.js # Entry point utama aplikasi React Native
   ├── metro.config.js # Konfigurasi Metro bundler
   └── node_modules/ # Semua library JavaScript

Fungsi Utama

android/ → tempat build system dan konfigurasi native Android.

ios/ → untuk komponen native iOS.

App.js → titik masuk utama aplikasi (mirip index.js di React web).

metro.config.js → mengatur cara bundler membaca dan mengompilasi file JS.

Dukungan Cross-Platform

Struktur ini memungkinkan:

Penulisan logika bisnis dan UI di file JS (bersifat universal).

Build terpisah untuk Android & iOS tanpa menulis ulang logika.

Navigasi mudah di VS Code karena file JS disusun modular dan lintas platform.
