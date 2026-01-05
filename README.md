# Daftar Payload Web

Salam, praktisi keamanan! Berikut tiga daftar payload yang dapat mendukung pengujian keamanan aplikasi web secara sistematis.

## Isi folder
- `xss-payloads.txt`: ribuan payload XSS (Cross-Site Scripting) singkat & encoded yang siap kamu coba di input vulnerable atau payload filter bypass.
- `sqli-payloads.txt`: kumpulan payload SQL Injection (boolean, union, time-based, enumeration, dan payload otomatis) untuk berbagai database dan konteks.
- `useragents.txt`: deretan string `User-Agent` untuk berbagai perangkat Android dan browser terbaru, berguna buat testing behavior berdasarkan header.

## Cara pakai
1. Pilih payload yang sesuai target (XSS/SQLi/User-Agent).
2. Masukkan payload ke parameter input, header, atau point injection di aplikasi target.
3. Kombinasikan dengan tooling (Burp, ffuf, sqlmap, dll.) untuk automasi.
4. Gunakan `useragents.txt` untuk mengganti header `User-Agent` agar request terlihat lebih natural.

## Catatan penting
- Semua file ini dibuat untuk tujuan _pentesting_ atau bug bounty dengan izin eksplisit, jadi jangan disalahgunakan. Gunakan secara bertanggung jawab.
- Creator tidak bertanggung jawab kalau ada pihak yang memakai list ini buat hal-hal yang melanggar hukum atau etika.
- Jangan unggah payload berpotensi berbahaya ke repo publik tanpa sadar riwayatnya.

## Lisensi
Konten disediakan tanpa jaminan apa pun dan dapat digunakan ulang di bawah `MIT License`. Sertakan file `COPYING` atau tentukan lisensi ini saat mendistribusikan ulang agar semua orang tahu hak dan batasannya.
