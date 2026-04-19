# Roadmap Belajar

Dokumen ini menyusun jalur belajar dari fondasi sampai pelaporan yang siap dipakai di lingkungan kerja.

## Fase 1: Fondasi Web App Testing

### Fokus

- memahami HTTP request dan response;
- mengenali parameter, header, cookie, dan body;
- memahami trust boundary;
- mengenali perbedaan input, processing, sink, dan output.

### Hasil Belajar

- mampu memetakan titik masuk input;
- mampu menjelaskan mengapa input tidak tepercaya harus dianggap data;
- mampu membuat baseline request sederhana.

## Fase 2: Pemahaman Konteks

### Fokus

- memahami konteks HTML, attribute, JavaScript, SQL, dan shell;
- mengenali kapan input hanya tampil dan kapan benar-benar diproses;
- membaca hubungan antara perilaku aplikasi dan akar masalah teknis.

### Hasil Belajar

- tidak sekadar mencoba payload;
- mampu memilih jenis pengujian sesuai konteks sink.

## Fase 3: Penguasaan Dataset

### Fokus

- membaca karakter file payload dan wordlist;
- membedakan dataset utama dan dataset pendukung;
- memilih sampel kecil yang relevan untuk sesi uji.

### Hasil Belajar

- mampu menyusun sesi belajar berbasis hipotesis;
- mampu menghindari pendekatan “jalankan semuanya”.

## Fase 4: Latihan Lab Terstruktur

### Fokus

- membangun baseline;
- menguji satu perubahan per iterasi;
- menyimpan bukti yang relevan;
- mengelompokkan hasil secara konsisten.

### Hasil Belajar

- hasil uji dapat direproduksi;
- temuan lebih mudah dikaji ulang oleh orang lain.

## Fase 5: Validasi Mitigasi

### Fokus

- melakukan retest;
- memverifikasi bahwa patch menutup akar masalah;
- mengecek variasi yang masih satu keluarga risiko.

### Hasil Belajar

- mampu membedakan fix gejala dan fix akar masalah;
- mampu menulis rekomendasi yang bisa dikerjakan engineering.

## Fase 6: Reporting Profesional

### Fokus

- menulis ringkasan yang akurat;
- memisahkan fakta, analisis, dan asumsi;
- menjelaskan dampak secara realistis;
- menyertakan rekomendasi dan status retest.

### Hasil Belajar

- laporan dapat dipakai engineering, QA, dan security reviewer;
- hasil latihan punya nilai operasional yang lebih tinggi.

## Urutan Belajar yang Disarankan

1. Mulai dari `XSS` untuk belajar konteks output dan observasi cepat.
2. Lanjut ke `SQLi` untuk memahami input terhadap logika backend.
3. Masuk ke `Command Injection` setelah memahami boundary server-side.
4. Gunakan `useragents.txt` dan `worldlist-directory-login.txt` sebagai dataset pendukung.

## Tanda Anda Siap Naik Level

- sudah terbiasa membuat baseline;
- sudah bisa menjelaskan alasan memilih dataset;
- sudah bisa membedakan sinyal kuat dan false positive;
- sudah bisa melakukan retest dengan disiplin.

## Kesalahan Umum

- terlalu fokus pada jumlah payload;
- tidak mencatat kondisi baseline;
- tidak membedakan konteks sink;
- menyimpulkan terlalu cepat dari satu respons ambigu.
