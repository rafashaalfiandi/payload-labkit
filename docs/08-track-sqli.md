# Track SQLi

Dokumen ini menyusun jalur belajar `SQL injection` agar fokus pada observasi backend dan kualitas validasi, bukan sekadar volume payload.

## Tujuan Track

- memahami bagaimana input memengaruhi logika query;
- membedakan indikasi kuat dan lemah;
- menghubungkan temuan dengan query parameterization dan error handling.

## Kompetensi yang Harus Dikuasai

- mengenali endpoint yang memproses data dinamis;
- mencatat perbedaan response berdasarkan variasi input;
- memahami peran query parameterization;
- membaca error leakage secara hati-hati.

## Urutan Latihan

1. Bangun baseline request normal.
2. Pilih parameter yang paling berisiko.
3. Lakukan pembandingan respons secara terukur.
4. Catat perbedaan status, ukuran, konten, atau delay.
5. Validasi apakah perubahan konsisten.
6. Susun rekomendasi pada level code dan data access.

## Checklist Observasi

- parameter mana yang diuji;
- ada error leakage atau tidak;
- hasil berubah secara konsisten atau ambigu;
- ada perbedaan true/false behavior;
- patch menutup akar masalah atau hanya memblokir pola tertentu.

## Artefak yang Harus Disimpan

- request baseline;
- request pembanding;
- ringkasan perbedaan respons;
- catatan asumsi DBMS bila ada;
- rekomendasi penggunaan prepared statement atau ORM safe pattern.

## Kesalahan Umum

- tidak menyimpan baseline;
- langsung memakai variasi kompleks;
- menganggap error generik sebagai bukti final;
- menulis dampak tanpa bukti reproduksi yang kuat.

## Keluaran Akhir yang Diharapkan

- matriks endpoint dan parameter berisiko;
- bukti perbedaan respons yang konsisten;
- analisis akar masalah query handling;
- retest plan setelah mitigasi.
