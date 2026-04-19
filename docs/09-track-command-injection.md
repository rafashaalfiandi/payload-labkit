# Track Command Injection

Dokumen ini menyusun jalur belajar `command injection` dengan fokus pada boundary input server-side dan desain pemanggilan proses yang aman.

## Tujuan Track

- memahami kapan input mencapai shell atau system command;
- membedakan sanitization, escaping, dan argument separation;
- mengevaluasi desain aplikasi yang memakai proses eksternal.

## Kompetensi yang Harus Dikuasai

- membaca pola pemanggilan proses di kode;
- mengenali kapan shell digunakan;
- memahami allowlist dan pemisahan argument;
- mendokumentasikan risiko tanpa memperluas aksi destruktif.

## Urutan Latihan

1. Identifikasi fitur aplikasi yang memanggil utilitas OS.
2. Petakan parameter yang masuk ke command.
3. Audit apakah aplikasi membangun string command.
4. Bandingkan perilaku normal dan anomali di lab aman.
5. Nilai apakah mitigasi berada di level input, API, atau arsitektur.

## Checklist Observasi

- fungsi atau library apa yang dipakai;
- shell terlibat atau tidak;
- input menjadi satu string atau argumen terpisah;
- ada allowlist, fixed command map, atau wrapper yang aman;
- ada log atau error yang membantu reproduksi.

## Artefak yang Harus Disimpan

- potongan alur kode relevan;
- baseline request;
- bukti perubahan perilaku;
- rekomendasi mengganti string execution ke API yang lebih aman.

## Kesalahan Umum

- fokus pada separator, bukan pada akar masalah di kode;
- mengabaikan argument injection;
- tidak membedakan wrapper internal dengan shell invocation;
- tidak merencanakan retest setelah refactor.

## Keluaran Akhir yang Diharapkan

- peta fitur yang memanggil proses eksternal;
- penilaian tingkat risiko tiap entrypoint;
- rekomendasi perbaikan yang dapat diimplementasikan engineering.
