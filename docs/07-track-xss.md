# Track XSS

Dokumen ini menyusun jalur belajar `XSS` agar lebih sistematis dan tidak berhenti pada copy-paste payload.

## Tujuan Track

- memahami konteks refleksi;
- membedakan server-side rendering dan DOM-based behavior;
- menghubungkan hasil observasi dengan mitigasi yang tepat.

## Kompetensi yang Harus Dikuasai

- membaca request/response HTML;
- mengenali sink output;
- membedakan HTML, attribute, URL, dan JavaScript context;
- mengevaluasi output encoding dan sanitization.

## Urutan Latihan

1. Identifikasi semua input yang direfleksikan.
2. Kelompokkan konteks output.
3. Uji indikator sederhana di lab.
4. Catat perbedaan refleksi, render, dan perilaku DOM.
5. Cocokkan hasil dengan mitigasi yang sesuai.

## Checklist Observasi

- input muncul di mana;
- karakter khusus diubah atau tidak;
- ada event-driven behavior atau tidak;
- perubahan terjadi di server response atau browser runtime;
- ada kontrol seperti CSP atau template escaping.

## Artefak yang Harus Disimpan

- baseline response;
- request uji;
- screenshot atau bukti DOM;
- kesimpulan konteks output;
- rekomendasi encoding/sanitization yang relevan.

## Kesalahan Umum

- tidak membedakan refleksi dengan eksekusi;
- mencampur konteks HTML dan JavaScript;
- menganggap satu filter cukup untuk semua sink;
- tidak mengecek retest setelah perbaikan.

## Keluaran Akhir yang Diharapkan

- peta sink input;
- bukti konteks output;
- akar masalah teknis;
- rekomendasi mitigasi yang spesifik per sink.
