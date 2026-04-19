# Payload LabKit

Payload LabKit adalah toolkit belajar keamanan aplikasi web yang disusun ulang agar lebih rapi, lengkap, terstruktur, dan layak dipakai sebagai basis pembelajaran internal di lab terkontrol.

Repositori ini berisi dataset mentah, dokumentasi belajar, workflow lab, dan template kerja. Fokus utamanya adalah membantu pembelajar memahami konteks input, metode validasi, reproduksibilitas pengujian, dan kualitas pelaporan.

Repo ini tidak dikembangkan untuk memperluas eksploitasi agresif. Pengembangan difokuskan pada:

- struktur materi yang jelas;
- navigasi yang mudah;
- penggunaan yang aman di lab;
- dokumentasi yang profesional;
- alur belajar yang bisa dipakai individu maupun tim.

## Quick Start

1. Baca [docs/00-index.md](/home/rafasa/Downloads/payload-labkit-main/docs/00-index.md).
2. Ikuti [docs/01-roadmap-belajar.md](/home/rafasa/Downloads/payload-labkit-main/docs/01-roadmap-belajar.md).
3. Siapkan lingkungan aman lewat [docs/02-lab-setup.md](/home/rafasa/Downloads/payload-labkit-main/docs/02-lab-setup.md).
4. Pakai [docs/03-metodologi-uji.md](/home/rafasa/Downloads/payload-labkit-main/docs/03-metodologi-uji.md) sebagai SOP latihan.
5. Pelajari konteks dataset melalui [docs/04-katalog-dataset.md](/home/rafasa/Downloads/payload-labkit-main/docs/04-katalog-dataset.md).
6. Pilih jalur topik:
   - [docs/07-track-xss.md](/home/rafasa/Downloads/payload-labkit-main/docs/07-track-xss.md)
   - [docs/08-track-sqli.md](/home/rafasa/Downloads/payload-labkit-main/docs/08-track-sqli.md)
   - [docs/09-track-command-injection.md](/home/rafasa/Downloads/payload-labkit-main/docs/09-track-command-injection.md)
7. Dokumentasikan hasil dengan:
   - [templates/lab-note-template.md](/home/rafasa/Downloads/payload-labkit-main/templates/lab-note-template.md)
   - [templates/report-template.md](/home/rafasa/Downloads/payload-labkit-main/templates/report-template.md)

## Struktur Repo

### Dataset

- `xss-payloads.txt`
  Dataset mentah untuk pembelajaran refleksi input, encoding output, parser behavior, dan sink DOM/HTML.

- `sqli-payloads.txt`
  Dataset mentah untuk pembelajaran perbedaan kondisi true/false, error handling, variasi sintaks, dan observasi perilaku query.

- `command-injection.txt`
  Dataset mentah untuk menganalisis boundary input server-side dan pola pemanggilan shell yang tidak aman.

- `useragents.txt`
  Dataset pendukung untuk pengujian perilaku berbasis header dan variasi profil klien.

- `worldlist-directory-login.txt`
  Wordlist path/login yang dapat dipakai untuk memahami pola penamaan route dan entrypoint di lab.

### Dokumentasi

- [docs/00-index.md](/home/rafasa/Downloads/payload-labkit-main/docs/00-index.md)
- [docs/01-roadmap-belajar.md](/home/rafasa/Downloads/payload-labkit-main/docs/01-roadmap-belajar.md)
- [docs/02-lab-setup.md](/home/rafasa/Downloads/payload-labkit-main/docs/02-lab-setup.md)
- [docs/03-metodologi-uji.md](/home/rafasa/Downloads/payload-labkit-main/docs/03-metodologi-uji.md)
- [docs/04-katalog-dataset.md](/home/rafasa/Downloads/payload-labkit-main/docs/04-katalog-dataset.md)
- [docs/05-checklist-reporting.md](/home/rafasa/Downloads/payload-labkit-main/docs/05-checklist-reporting.md)
- [docs/06-glosarium.md](/home/rafasa/Downloads/payload-labkit-main/docs/06-glosarium.md)
- [docs/07-track-xss.md](/home/rafasa/Downloads/payload-labkit-main/docs/07-track-xss.md)
- [docs/08-track-sqli.md](/home/rafasa/Downloads/payload-labkit-main/docs/08-track-sqli.md)
- [docs/09-track-command-injection.md](/home/rafasa/Downloads/payload-labkit-main/docs/09-track-command-injection.md)
- [docs/10-governance-dataset.md](/home/rafasa/Downloads/payload-labkit-main/docs/10-governance-dataset.md)
- [docs/11-workflow-lab.md](/home/rafasa/Downloads/payload-labkit-main/docs/11-workflow-lab.md)

### Template Kerja

- [templates/lab-note-template.md](/home/rafasa/Downloads/payload-labkit-main/templates/lab-note-template.md)
- [templates/report-template.md](/home/rafasa/Downloads/payload-labkit-main/templates/report-template.md)

## Learning Paths

### Jalur 1: Fundamental

Cocok untuk pemula yang baru memahami HTTP, parameter, context, output encoding, dan baseline response.

### Jalur 2: Topic-Driven Practice

Cocok untuk pembelajar yang ingin berlatih per topik dengan alur observasi, hipotesis, dan retest yang konsisten.

### Jalur 3: Team Lab Operations

Cocok untuk tim internal yang ingin memakai repo ini sebagai materi onboarding, sesi latihan terstruktur, atau internal security QA.

## Inventaris Konten

Jumlah baris saat revisi dokumentasi ini dibuat:

- `xss-payloads.txt`: 7.271 baris
- `sqli-payloads.txt`: 4.313 baris
- `command-injection.txt`: 4.065 baris
- `useragents.txt`: 4.111 baris
- `worldlist-directory-login.txt`: 999.999 baris

Catatan:

- Nama file `worldlist-directory-login.txt` dipertahankan demi kompatibilitas dengan struktur repo saat ini.
- Dataset mentah sengaja tidak diposisikan sebagai materi awal. Gunakan dokumentasi untuk memahami konteks sebelum memilih sampel yang relevan.

## Prinsip Penggunaan

- Gunakan hanya pada lab lokal, CTF, sandbox, atau target yang memiliki izin eksplisit.
- Hindari penggunaan pada sistem produksi atau pihak ketiga tanpa otorisasi tertulis.
- Utamakan pembelajaran akar masalah, validasi mitigasi, dan disiplin dokumentasi.
- Jangan menyimpan data sensitif yang tidak relevan dengan tujuan uji.

## Nilai Tambah Versi Ini

- repositori lebih mudah dinavigasi;
- materi belajar lebih terstruktur;
- workflow pengujian lebih jelas;
- template kerja lebih siap pakai;
- cocok untuk belajar mandiri maupun kolaborasi tim.

## Lisensi

Mengikuti `MIT License` yang ada di repo ini.
