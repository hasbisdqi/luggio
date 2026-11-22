# luggio

Proyek **LUGGIO: Sistem Pelacakan Bagasi RFID Bandara Indo-Aero**.

## Deliverable CP3

Dokumen lengkap ada di folder [`docs/`](docs/README.md):

- [M8 — WPD & Earned Value](docs/03-wpd-earned-value.md)
- [M9 — Change Management](docs/01-change-management.md)
- [Form CR 02/CR/2026](docs/06-cr-form.md)
- [CR Log](docs/07-cr-log.md)
- [M10 — Closing Report](docs/02-closing-report.md)
- [Risk Register](docs/05-risk-register.md)
- [Checklist CP3](docs/04-cp3-checklist.md)

Versi DOCX dan PDF tersedia di `docs/docx/` dan `docs/pdf/`.

## Jadwal

Tiga file XML disiapkan untuk kebutuhan berbeda:

| File | Isi | Kegunaan |
|---|---|---|
| `..._FIXED.xml` | Baseline 0, tanpa progress | Master/arsip |
| `..._M8_PROGRESS.xml` | Progress 20 Mar 2026 | Screenshot M8 |
| `..._M9_M10_FINAL.xml` | 01/CR/2026 + 02/CR/2026 (paralel) + 100% | M9/M10 |

## Penting — impor ulang ke MPP

File `.mpp` yang dibuat dari XML versi awal masih memiliki durasi memanjang karena `Remaining Duration` dan tanggal assignment membawa nilai lama. XML di repo ini sudah diperbaiki.

Buka ulang ketiga XML terbaru di MS Project (Windows), lalu **Save As** `.mpp`. Cek **Project → Statistics**:

- FIXED/M8: finish **24 Apr 2026**, 53 hari.
- FINAL: finish **24 Apr 2026**, 53 hari (BAC Rp242.678.233).
- Tidak boleh ada tanggal 2027/2028 atau durasi >60 hari.

Langkah lengkap: [`CARA-PAKAI-FIXED.md`](CARA-PAKAI-FIXED.md).
