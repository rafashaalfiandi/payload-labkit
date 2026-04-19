# Governance Dataset

Dokumen ini menetapkan aturan penggunaan dataset agar repo tetap profesional dan aman dipakai untuk belajar.

## Prinsip Umum

- dataset diperlakukan sebagai bahan studi, bukan checklist eksekusi massal;
- gunakan subset yang relevan dengan tujuan sesi;
- semua penggunaan harus berada dalam scope lab atau target berizin;
- setiap sesi harus punya baseline, hipotesis, dan catatan hasil.

## Aturan Penggunaan

- jangan menjalankan seluruh file mentah tanpa seleksi;
- jangan mencampur banyak kategori payload dalam satu hipotesis uji;
- jangan menyimpan bukti sensitif di repo ini;
- dokumentasikan versi target, konfigurasi, dan tanggal uji.

## Aturan Kurasi Internal

- tambahkan dokumentasi sebelum menambah dataset baru;
- jelaskan peran dataset dan risiko salah pakai;
- gunakan penamaan file yang konsisten;
- pertahankan kompatibilitas bila rename berisiko memutus workflow lama.

## Kualitas Dataset yang Baik

- ada tujuan belajar yang jelas;
- ada konteks penggunaan;
- ada batasan penggunaan;
- ada hubungan ke workflow dan template.

## Anti-Pattern

- dump file tanpa klasifikasi;
- payload tanpa konteks;
- wordlist besar tanpa strategi sampling;
- dokumentasi yang hanya menjelaskan “apa”, bukan “kapan” dan “mengapa”.

## Rekomendasi Operasional

- buat subset lokal untuk tiap sesi;
- simpan hasil sesi di folder terpisah di luar dataset mentah;
- evaluasi dataset berdasarkan nilai belajar, bukan panjang file.
