## Soal Evaluasi Harian

Jelaskan definisi Mobile App Development sesuai pemahaman anda beserta fokus utama dan output teknisnya!

Bandingkan perbedaan mendasar antara Web Development dan Mobile App Development dalam aspek target eksekusi, distribusi, dan akses hardware. Berikan contoh implikasi praktis dari perbedaan tersebut dalam pengembangan aplikasi sehari-hari.

Uraikan tahapan Discovery & Requirement dalam siklus hidup aplikasi mobile. Bagaimana tahap ini memengaruhi keputusan target platform (Android/iOS) dan kebutuhan offline/online?

Deskripsikan tahapan Perancangan Arsitektur & Teknologi dalam Mobile App Development, khususnya dalam konteks React Native sesuai pemahaman anda. Mengapa pemilihan strategi state management dan navigasi menjadi krusial di tahap ini?

Jelaskan perbedaan antara pendekatan Native Development dan Hybrid Development dalam pengembangan aplikasi mobile. Sertakan keuntungan serta kekurangan masing-masing, dan berikan contoh framework yang relevan selain dari yang telah disampaikan di materi.

Apa yang dimaksud dengan Cross-Platform Native Development? Bandingkan keuntungan dan kekurangannya dengan pendekatan native.

Posisikan React Native dalam ekosistem pengembangan aplikasi mobile. Bagaimana React Native berbeda dari ReactJS dalam hal target, sintaks dasar, dan styling?

Analisis tantangan utama dalam pengembangan aplikasi mobile dibandingkan dengan web. Bagaimana pendekatan cross-platform seperti React Native mengatasi tantangan ini?

Uraikan tahapan Pengujian dan Build, Signing, serta Release dalam Mobile App Development menggunakan React Native!

Berdasarkan penjelasan diatas, jelaskan kenapa React native menjadi pilihan dalam development application mobile saat ini?

## JAWABAN

1. Apa itu definisi dari Mobile app development sesuai pemahaman dari saya Mobile app development adalah merancang dan membangun sebuah aplikasi perangkat lunak yang berjalan di perangkat mobile seperti smartphone dan table dan out put teknis adalah aplikasi yang ada di perangakat kita sehari hari contoh aplikasi seperti e-wallet m-banking dan masih banyak lain nya

2. Oke saya akan jelaskan perbedaan antara web development dan mobile app develoment penurut pemahaman dari saya

Target eksekusi

- Web devoloment itu aplikasi yang berjalan lewat browser kayak google chromium sahari dll contoh nya kayak websine e-commerce bisa langsung bukan lewat url nampa download terlebih dahulu

- Mobile app development itu aplikasi yang berjalan lewat perangkat mobile seperti ANDORID/IOS jadi harus di instal terlebih dahulu lewat playstore atau app store contoh nya uber grap gojek e.wallet dll

Distribusi

- Web lebih mudah untuk di distibusi kan hanya cukup uplode ke server dan semua user bisa akses lewat link browser

- Mobile Lebih ribet karna harus melalui proses publishing yang resmi kayak google playstore dan app store jadi agak ribet apa lagi jika app nya belom optimal di beberapa device

Akses untuk hardware

- Web lebih terbatas dalam mengakses hardware karna hanya berjalan di web browser

- Untuk Mobile app bisa mangakses penuh fitur bawaan dari hardware kayak gyro kamera gps wifi bluetooth dll

Implikasi Praktis:

- Kalau mau bikin aplikasi toko online biasa, web udah cukup karena fokusnya di akses cepat tanpa install

- Tapi kalau mau bikin aplikasi yang butuh akses kamera & notifikasi, kayak scanner app atau delivery tracking, maka mobile app jauh lebih cocok

3. Tahapan Discovery & Requirement dalam Mobile App Development

- Discovery dan requiremnt adalah tahap awal buat memahami tujuan aplikasi, kebutuhan user, fitur utama, dan batasan proyek sebelum mulai coding. di sini kita menentukan masalah yang harus di selesikan, siapa user-nya fitur apa yang penting dan harus riset target dan platform

tahap ini sangat penting karana akan menentukan apakah aplikasi di buat Android, IOS, atau keduanya dan apakah butuh bekerja secara ofline atau online atu hybrib

4. Tahapan Perancangan Arsitektur & Teknologi dalam Mobile App

- Di tahap Perancangan arsiktektur dan teknologi ini kita nentuin teknis aplikasi dan teknologi apa yang dipakai sebelum mulai coding. ini termaksud cara aplikasi mengelola data, alur layar, dan cara komunikasi antar bagian aplikasi

dalam kontesk react native tahap ini meliputi

Struktur Project (folder, komponen, services)

Pemilihan State Management (misal: Context API, Redux, Zustand)

Navigasi App (React Navigation: stack, tab, drawer)

APIs & Backend yang dipakai (REST, GraphQL, Firebase)

Handling Storage (AsyncStorage / local DB)

- Kenapa state management & navigasi krusial?

State management ngatur alur data di aplikasi → biar data konsisten dan gak bikin kode berantakan.

Navigasi ngatur alur perpindahan antar layar → biar pengalaman pengguna jelas dan flow app rapi.

5. Perbedaan Native vs Hybrid Development + Kelebihan, Kekurangan & Contoh Framework

Native Development

Definisi
Bangun app langsung pakai bahasa resmi tiap platform (Android/iOS).

- Kelebihan

- Performa paling kenceng

- Akses fitur device lengkap (kamera, GPS, sensor)

- UI & UX paling halus/nyatu sama OS

Kekurangan

- Dua codebase (Android & iOS) → waktu & biaya lebih tinggi

- Butuh skill per platform

Contoh Framework

- Android: Kotlin / Java (Android Studio)
- iOS: Swift / Objective-C (Xcode)
- Hybrid Development

Definisi
App web (HTML/CSS/JS) dibungkus jadi app mobile via WebView.

Kelebihan

- Satu codebase multi-platform

- Cepat & murah buat bangun aplikasi simple

Kekurangan

- Performa kalah → animasi kadang patah-patah

- UI gak terlalu terasa “native”

- Akses hardware tergantung plugin

Contoh Framework

- Ionic

- Apache Cordova

-Capacitor

Kesimpulan singkat:
Native = performa & pengalaman terbaik tapi mahal.
Hybrid = cepat & murah, tapi performa & UX lebih lemah.

6. Apa itu Cross-Platform Native Development? Bandingkan dengan Native

Definisi

Cross-Platform native devolepment adalah perndekatan bikin aplikasi mobile dengan satu codebase yang bisa jalan di Android dan IOS tetap pakai komponen UI native buka webview

contoh react native, fluter

Kelebihan Cross-Platform Native

- Satu codebase untuk dua platform hemat waktu dan biaya
- UI dan performa mendekati native
- cocok buat tim kecil/startup
- Update cepat Hot reload

Kekurangan Cross-Platform Native

- Akses fitur hardware kadang perlu bridging

- Debugging lebih kompleks (JS + native layer)

- Kadang butuh penyesuaian UI per platform

7. Posisi React Native dalam ekosistem mobile & perbedaan dengan ReactJS
   posisi react native

- React native adalah framework cross- platform buat bikin apikin aplikasi mobile yang yang jalan di Androin dan IOS pakai JS/TS dan konsep dari react.

Perbedaan nya

- ReactJS bikin website render nya ke dom
- React Native bikin mobile app, render ke komponen native

8. Tantangan utama Mobile vs Web & gimana React Native bantu
   Tantangan Mobile dibanding Web

Mobile dev itu lebih ribet karena:

- Jaringan nggak selalu stabil → harus handle offline mode
- Baterai & memori terbatas → app harus efisien
- Ukuran layar & device beda-beda → UI harus responsive
- Izin & keamanan ketat (kamera, lokasi, storage)
- Proses publish ribet (App Store / PlayStore review)
- Testing harus di device nyata & emulator
- Lifecycle app kompleks (foreground, background, permission, crash, dll)

Gimana React Native bantu ngatasi?

React Native mempermudah dengan:

1 codebase untuk Android & iOS → hemat waktu

- Hot Reload → dev lebih cepat
- Komponen UI Native → performa lebih smooth
- Native Modules → akses fitur device (kamera, GPS, Bluetooth)
- Community gede + banyak library
- Flexbox → layout UI lebih gampang dan konsisten

9. Tahapan Pengujian + Build, Signing, & Release di React Native

- Tahapan Pengujian (Testing)

Di React Native, testing itu buat mastiin app jalan mulus dan bebas bug:

- Unit Test
  Ngetes fungsi kecil / logic (misalnya hitung total harga).

- Snapshot Test
  Cek tampilan UI nggak berubah tiba-tiba.

- Testing di Emulator & Device Asli
  Pastikan UI, gesture, dan fitur device (kamera, GPS, dll) beneran jalan.

- E2E Test (optional kalau di bootcamp belum)
  Tes alur user bener-bener dari buka app sampai selesai.

Intinya: pastiin fitur jalan, UI aman, dan app nggak nge-lag / error.

Tahapan build, Signingm dan release

Build app

- Android: hasil APK/AAB
- IOS: hasil IPA
  Ini proses compile app siap kirim ke store

Signing

- App dikasih digital signature key
- Biar Play Store / App Store yakin itu app resmi, bukan modifikasi curang

Release

- Upload ke Google Play Console / Apple App Store Connect
- Isi informasi app (deskripsi, ikon, screenshot, privacy policy)
- Tunggu review store
- Setelah lolos → app bisa di-download user

10. Kenapa react native menjadi pilihan dalam development application mobile saat ini?

- Karna react native bisa membuat aplikasi yang bisa berjalan di dua os yang berbeda Andorid dan IOS tampa harus belajar bahasa yang spefik untuk kedua hanya belajar react native bisa membuat app yang bisa berjalan di kedua os tersebut
