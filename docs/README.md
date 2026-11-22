# Deliverable CP3 — Proyek LUGGIO

Folder ini berisi dokumen CP3 untuk Proyek **LUGGIO: Sistem Pelacakan Bagasi RFID Bandara Indo-Aero**.

## Daftar Dokumen

| Dokumen | Markdown | DOCX | PDF |
|---|---|---|---|
| M8 — WPD & Earned Value | [03-wpd-earned-value.md](03-wpd-earned-value.md) | [DOCX](docx/03-wpd-earned-value.docx) | [PDF](pdf/03-wpd-earned-value.pdf) |
| M9 — Change Management | [01-change-management.md](01-change-management.md) | [DOCX](docx/01-change-management.docx) | [PDF](pdf/01-change-management.pdf) |
| CR Form — 02/CR/2026 | [06-cr-form.md](06-cr-form.md) | [DOCX](docx/06-cr-form.docx) | [PDF](pdf/06-cr-form.pdf) |
| CR Log | [07-cr-log.md](07-cr-log.md) | [XLSX](xlsx/07-cr-log.xlsx) — template *Change Request Log* | — (dibuat manual dari XLSX) |
| M10 — Closing Report | [02-closing-report.md](02-closing-report.md) | [DOCX](docx/02-closing-report.docx) | [PDF](pdf/02-closing-report.pdf) |
| Risk Register | [05-risk-register.md](05-risk-register.md) | [DOCX](docx/05-risk-register.docx) | [PDF](pdf/05-risk-register.pdf) |
| Checklist CP3 | [04-cp3-checklist.md](04-cp3-checklist.md) | [DOCX](docx/04-cp3-checklist.docx) | [PDF](pdf/04-cp3-checklist.pdf) |

## Angka Acuan

| Item | Baseline 0 | Baseline 1 |
|---|---:|---:|
| Finish | 24 Apr 2026 | 1 Mei 2026 |
| Durasi | 53 hari | 58 hari |
| BAC | Rp219.678.233 | Rp234.678.233 |
| 02/CR/2026 | — | +Rp15.000.000 (5 hari) |

M8 status 20 Mar 2026:

- % Complete proyek: 57%
- EV/AC work packages: Rp122.578.233
- EV/AC total proyek: ±Rp124.388.145
- PV work packages: ±Rp149.897.333
- CPI: 1,00
- SPI: 0,818

M10 final:

- EV: Rp219.678.233
- AC: Rp234.678.233
- CV: −Rp15.000.000
- CPI: 0,936
- EAC: Rp234.678.233
- VAC: −Rp15.000.000

## Penting — Impor Ulang XML ke MPP

File `.mpp` yang dibuat dari XML versi awal masih memiliki durasi memanjang karena `Remaining Duration` dan tanggal assignment membawa nilai lama. XML di repo ini sudah diperbaiki.

Silakan buka ulang ketiga XML terbaru di MS Project (Windows), lalu **Save As** `.mpp`:

1. `..._FIXED.xml` → finish 24 Apr 2026, 53 hari.
2. `..._M8_PROGRESS.xml` → status 20 Mar 2026, 57%.
3. `..._M9_M10_FINAL.xml` → finish 1 Mei 2026, 58 hari, Baseline 1.

Setelah impor, cek **Project → Statistics**. Tidak boleh ada tanggal 2027/2028 atau durasi >60 hari. Detail langkah ada di [`../CARA-PAKAI-FIXED.md`](../CARA-PAKAI-FIXED.md).

## Regenerasi DOCX/PDF

Dari root repo:

```bash
pandoc docs/01-change-management.md -o docs/docx/01-change-management.docx --from markdown+pipe_tables --toc --toc-depth=2
pandoc docs/01-change-management.md -o docs/pdf/01-change-management.pdf --from markdown+pipe_tables --pdf-engine=xelatex --toc --toc-depth=2 -V geometry:margin=2cm -V fontsize=10pt -V mainfont="Times New Roman" -V lang=id
```

Ulangi untuk `02-closing-report`, `03-wpd-earned-value`, `04-cp3-checklist`, dan `05-risk-register`.

## Catatan

- Screenshot MS Project untuk M8/M10 masih perlu ditempel pada placeholder di dokumen M8 dan M10.
- Sign-off perlu tanda tangan Sponsor, PM, dan User Representative.
- Risk Register disusun sebagai ringkasan; jika ada file asli, lampirkan file asli sebagai dokumen utama.
