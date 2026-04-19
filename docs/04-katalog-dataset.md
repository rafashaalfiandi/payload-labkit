# Katalog Dataset

Dokumen ini mengubah file mentah di repo menjadi katalog belajar yang lebih terstruktur.

## Ringkasan Cepat

| Dataset | Peran | Prioritas Belajar | Risiko Salah Pakai |
| --- | --- | --- | --- |
| `xss-payloads.txt` | Belajar context dan output handling | Tinggi | Sedang |
| `sqli-payloads.txt` | Belajar perilaku query dan observasi logic flaw | Tinggi | Tinggi |
| `command-injection.txt` | Belajar boundary input ke shell | Menengah | Tinggi |
| `useragents.txt` | Dataset pendukung untuk variasi header | Menengah | Rendah |
| `worldlist-directory-login.txt` | Dataset pendukung untuk pola path | Menengah | Menengah |

## 1. `xss-payloads.txt`

### Tujuan Belajar

- memahami letak refleksi input;
- membedakan HTML body, attribute, URL, script, dan DOM sink;
- mengevaluasi encoding output;
- mengamati dampak parser behavior dan event handling.

### Cocok Dipakai Saat

- ada input yang direfleksikan kembali ke respons;
- aplikasi memproses HTML atau template dinamis;
- Anda ingin memetakan konteks input sebelum memikirkan mitigasi.

### Cara Pakai yang Disarankan

- mulai dari sampel kecil;
- kelompokkan hasil menurut konteks output;
- catat mana yang hanya terefleksi dan mana yang memicu perilaku berbeda;
- fokus pada akar masalah seperti missing encoding atau sink DOM yang tidak aman.

### Hal yang Harus Dicatat

- lokasi refleksi;
- apakah karakter di-escape;
- apakah ada CSP;
- apakah respons berubah sebelum atau sesudah render.

## 2. `sqli-payloads.txt`

### Tujuan Belajar

- memahami perbedaan hasil benar dan salah;
- mengenali error handling database;
- memetakan asumsi query di backend;
- membedakan observasi yang kuat dan indikasi palsu.

### Cocok Dipakai Saat

- ada form login, search, filter, sorting, atau lookup;
- ada perbedaan respons terhadap input tidak biasa;
- Anda ingin memvalidasi apakah parameter diperlakukan sebagai data atau instruksi query.

### Cara Pakai yang Disarankan

- mulai dari perbandingan baseline terhadap input uji sederhana;
- catat perubahan status code, ukuran respons, dan pesan error;
- simpan matriks hasil per endpoint dan per parameter;
- retest setelah patch untuk memastikan akar masalah benar-benar tertutup.

### Hal yang Harus Dicatat

- tipe DBMS jika diketahui;
- perbedaan true/false behavior;
- indikasi error leakage;
- pola parameterization di sisi aplikasi.

## 3. `command-injection.txt`

### Tujuan Belajar

- memahami bahaya saat input diteruskan ke shell;
- mengenali perbedaan validasi input dan pemisahan argument;
- memetakan pola pemanggilan command yang tidak aman.

### Cocok Dipakai Saat

- aplikasi menerima input yang berkaitan dengan utilitas OS;
- ada fitur ping, traceroute, export, convert, backup, atau wrapper tool;
- Anda sedang mengaudit pemanggilan proses di server-side code.

### Cara Pakai yang Disarankan

- gunakan hanya di lab aman dan terisolasi;
- fokus pada analisis pola kode dan validasi, bukan eksekusi agresif;
- verifikasi apakah aplikasi memakai shell langsung atau API argument-safe;
- dokumentasikan perbaikan pada level kode, bukan hanya pemblokiran karakter.

### Hal yang Harus Dicatat

- fungsi yang dipakai aplikasi;
- apakah shell di-invoke;
- apakah input menjadi satu string atau dipisah per argumen;
- kontrol allowlist yang ada.

## 4. `useragents.txt`

### Tujuan Belajar

- menguji adaptasi perilaku aplikasi berdasarkan profil klien;
- melihat dampak middleware, cache, dan WAF terhadap variasi header;
- memahami pentingnya baseline saat melakukan request variation testing.

### Cocok Dipakai Saat

- ingin melihat beda output desktop/mobile;
- ada logic berbasis browser detection;
- ingin menguji konsistensi akses dan rendering.

### Cara Pakai yang Disarankan

- perlakukan sebagai dataset pendukung, bukan dataset utama;
- pilih subset kecil yang representatif;
- bandingkan hasil berdasar kelompok browser atau device family.

## 5. `worldlist-directory-login.txt`

### Tujuan Belajar

- memahami pola penamaan route sensitif;
- belajar membangun subset wordlist yang relevan;
- menguji coverage path di lab secara terukur.

### Cocok Dipakai Saat

- menyusun daftar jalur admin/login internal di lab;
- menguji konsistensi routing dan naming convention;
- ingin membuat wordlist yang lebih kecil dan lebih presisi.

### Cara Pakai yang Disarankan

- gunakan subset, bukan seluruh file, untuk sesi latihan;
- labeli kategori path yang sedang diuji;
- prioritaskan pembacaan pola, bukan volume request.

## Strategi Penggunaan Profesional

1. Tentukan tujuan pengujian per sesi.
2. Pilih satu dataset utama dan bila perlu satu dataset pendukung.
3. Ambil sampel kecil dan bangun baseline.
4. Catat perubahan secara disiplin.
5. Simpulkan kelemahan kontrol input, output, query, atau proses, bukan sekadar “payload bekerja”.

## Prioritas Belajar

1. `xss-payloads.txt`
2. `sqli-payloads.txt`
3. `command-injection.txt`
4. `useragents.txt`
5. `worldlist-directory-login.txt`
