# Workflow Lab

Dokumen ini mendefinisikan alur kerja lab yang rapi dari persiapan sampai retest.

## Fase 1: Persiapan

- tetapkan scope;
- siapkan target lab;
- buat folder bukti;
- pilih dataset dan topik sesi;
- tulis hipotesis awal.

## Fase 2: Baseline

- kirim request normal;
- catat status code;
- catat ukuran atau bentuk respons;
- catat waktu respons;
- simpan screenshot bila relevan.

## Fase 3: Pengujian Terkontrol

- ubah satu variabel per iterasi;
- beri label request;
- bandingkan dengan baseline;
- hentikan bila perilaku keluar dari scope yang direncanakan.

## Fase 4: Analisis

- kelompokkan hasil ke `negative`, `ambiguous`, `strong-signal`, atau `confirmed`;
- simpulkan apakah akar masalah ada di input handling, output handling, query construction, atau process execution;
- tulis rekomendasi teknis yang dapat dikerjakan.

## Fase 5: Pelaporan

- pindahkan hasil penting ke template report;
- pisahkan bukti, analisis, dan rekomendasi;
- catat batasan pengujian dan asumsi.

## Fase 6: Retest

- verifikasi patch pada skenario yang sama;
- verifikasi juga variasi yang masih satu akar masalah;
- tandai status `Retest Passed` atau `Retest Failed`.

## Format Status Kerja

- `Planned`
- `In Progress`
- `Observed`
- `Confirmed`
- `Mitigated`
- `Retest Passed`
- `Retest Failed`
