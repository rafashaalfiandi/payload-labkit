# Metodologi Uji

Dokumen ini adalah SOP ringkas agar proses belajar dan validasi tetap konsisten.

## Langkah Inti

1. Identifikasi titik input.
2. Tentukan konteks pemrosesan input.
3. Siapkan baseline request.
4. Jalankan pengujian terkontrol dengan satu perubahan per iterasi.
5. Bandingkan hasil dengan baseline.
6. Kelompokkan sinyal hasil.
7. Verifikasi ulang.
8. Tulis akar masalah dan rekomendasi.

## Baseline Minimum

- URL dan endpoint;
- metode HTTP;
- parameter atau field;
- status code;
- ukuran atau bentuk response;
- waktu response;
- observasi visual atau pesan error.

## Kategori Hasil

- `Negative`
  Tidak ada perubahan berarti.
- `Ambiguous`
  Ada perubahan, tetapi belum cukup kuat.
- `Strong Signal`
  Ada perubahan konsisten yang mengarah ke risiko nyata.
- `Confirmed`
  Akar masalah dapat dijelaskan dan direproduksi.

## Panduan Observasi Per Topik

### XSS

Perhatikan:

- posisi refleksi input;
- konteks output;
- encoding output;
- DOM mutation atau render-time behavior.

### SQLi

Perhatikan:

- beda hasil benar dan salah;
- error leakage;
- perubahan data, layout, atau pesan;
- delay yang konsisten jika relevan.

### Command Injection

Perhatikan:

- apakah input diteruskan ke shell;
- apakah aplikasi membangun string command;
- apakah argumen dipisahkan dengan aman;
- apakah error atau log mendukung analisis.

## Aturan Kualitas Pengujian

- satu hipotesis per sesi;
- satu perubahan per iterasi;
- hasil negatif tetap dicatat;
- semua klaim harus punya baseline dan bukti;
- verifikasi minimal dua kali untuk temuan penting.

## Kualitas Temuan

Temuan yang baik:

- dapat direproduksi;
- punya bukti memadai;
- menjelaskan akar masalah;
- punya rekomendasi konkret.

Temuan yang lemah:

- hanya berdasarkan satu respons ambigu;
- tidak punya baseline;
- tidak jelas apakah berasal dari kerentanan nyata;
- tidak dapat diuji ulang.
