# Lab Setup

Dokumen ini merangkum setup lab yang aman, rapi, dan bisa dipakai berulang.

## Tujuan Setup

- memastikan eksperimen dilakukan di lingkungan terisolasi;
- memudahkan reproduksi hasil;
- menjaga bukti dan catatan tetap terstruktur.

## Prinsip Lab Aman

- gunakan VM, container, atau host lokal yang terisolasi;
- pisahkan data latihan dari data nyata;
- aktifkan logging bila memungkinkan;
- buat snapshot sebelum eksperimen besar;
- simpan bukti di lokasi yang terorganisir.

## Komponen Minimal

- browser;
- proxy HTTP seperti Burp Suite Community atau OWASP ZAP;
- editor teks atau note-taking tool;
- aplikasi lab yang memang aman untuk latihan;
- repo ini sebagai sumber dataset dan dokumentasi.

## Topologi Sederhana

1. `Attacker workstation`
   Browser, proxy, dataset, dan catatan.
2. `Target lab`
   Aplikasi lokal, container, atau VM latihan.
3. `Evidence storage`
   Folder untuk request sample, screenshot, dan report.

## Struktur Folder yang Disarankan

```text
lab-work/
├── notes/
├── requests/
├── screenshots/
├── findings/
└── reports/
```

## Checklist Pra-Uji

- scope jelas;
- target adalah lab atau berizin;
- snapshot tersedia;
- baseline plan sudah ditulis;
- folder bukti siap dipakai;
- template note dan report sudah tersedia.

## Checklist Pasca-Uji

- bukti sudah dipilah;
- catatan observasi sudah dirapikan;
- temuan penting sudah direproduksi;
- retest plan sudah dibuat;
- lingkungan bisa dipulihkan.

## Rekomendasi Operasional

- satu sesi, satu tujuan utama;
- satu temuan, satu catatan yang rapi;
- satu baseline per endpoint penting.
