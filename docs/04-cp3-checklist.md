# Checklist Deliverable CP3

## Proyek LUGGIO — Sistem Pelacakan Bagasi RFID Bandara Indo-Aero

| Item | Keterangan |
|---|---|
| Nomor Dokumen | LUGGIO-CP3-CHK-001 |
| Versi | 1.0 |
| Tanggal | 22 November 2026 |
| Status | Checklist internal |
| Proyek | LUGGIO: Sistem Pelacakan Bagasi RFID Bandara Indo-Aero |
| Baseline | Baseline 0 dan Baseline 1 |

---

## 1. Ringkasan Status

| Area | Status | Catatan |
|---|---|---|
| XML jadwal (FIXED, M8, FINAL) | Selesai | Sudah diperbaiki: remaining duration dan assignment dates diselaraskan. |
| File `.mpp` | **Perlu impor ulang** | File `.mpp` yang dibuat dari XML versi awal masih memanjang (518 hari / finish 2028). Impor ulang ketiga XML terbaru dan simpan sebagai `.mpp`. |
| M8 WPD/EVM | Dokumen selesai | Screenshot tabel EV, S-Curve, dan Gantt masih perlu ditempel. |
| M9 Change Management | Dokumen selesai | 02/CR/2026, analisis dampak, notulen CCB, dan CR log tersedia. |
| M10 Closing Report | Dokumen selesai | Section A–H tersedia; risk register ringkasan tersedia. |
| DOCX/PDF | Selesai | Dikonversi dari Markdown dengan pandoc. |
| Sign-off | Perlu tanda tangan | Nama dan tanggal sudah diisi. |

---

## 2. Checklist A — Administrasi dan Dokumen

| No | Item | Bukti | Status | Catatan |
|---|---|---|---|---|
| A1 | Project Charter v1.0 | PDF Charter | Tersedia | Tanggal 2 Feb 2026 |
| A2 | WBS dan WBS Dictionary | MPP/WBS | Tersedia | Termasuk 1.4.7 |
| A3 | Jadwal proyek | MPP/XML | Tersedia | Baseline 0 dan Baseline 1 |
| A4 | Risk Register | `docs/05-risk-register.md` | Tersedia | Ringkasan; lampirkan file asli jika ada |
| A5 | Laporan mingguan 1–10 | Dokumen mingguan | Tersedia | Lampirkan jika diminta |
| A6 | M8 WPD/EVM | `docs/03-wpd-earned-value.md` | Tersedia | Screenshot perlu ditempel |
| A7 | M9 Change Management | `docs/01-change-management.md` | Tersedia | Final |
| A8 | M10 Closing Report | `docs/02-closing-report.md` | Tersedia | Final |
| A9 | Checklist CP3 | Dokumen ini | Tersedia | Internal |

---

## 3. Checklist B — MS Project / MPP

### B.1 Verifikasi File

| No | File | Nilai yang harus muncul | Status |
|---|---|---|---|
| B1 | `..._FIXED.mpp` | Finish 24 Apr 2026; Duration 53d; Cost Rp219.678.233; Baseline 1 kosong | Perlu impor ulang |
| B2 | `..._M8_PROGRESS.mpp` | Status 20 Mar 2026; % Complete 57%; AC Rp124.388.145; CPI 1,00; SPI ±0,82 | Perlu impor ulang |
| B3 | `..._M9_M10_FINAL.mpp` | Finish 1 Mei 2026; Duration 58d; Cost Rp234.678.233; Baseline 1 Rp234.678.233; semua task 100% | Perlu impor ulang |

### B.2 Pemeriksaan Wajib Setelah Impor

- [ ] Tidak ada task dengan durasi >60 hari.
- [ ] Tidak ada finish 2027/2028.
- [ ] Status Date M8 = 20 Maret 2026.
- [ ] Status Date FINAL = 1 Mei 2026.
- [ ] Baseline 0 finish 24 April 2026; cost Rp219.678.233.
- [ ] Baseline 1 finish 1 Mei 2026; cost Rp234.678.233.
- [ ] Task 1.4.7 Middleware & Adaptor API DCS ada, 5 hari, Rp15.000.000.
- [ ] Task 1.6.1/1.6.2 memiliki predecessor 1.4.7.
- [ ] Tidak ada split task.
- [ ] Resource dan kalender terbawa.
- [ ] Custom field Text1/Text2 terbawa.

### B.3 Nilai Referensi

| Field | FIXED/M8 | FINAL |
|---|---|---|
| Start | 9 Feb 2026 | 9 Feb 2026 |
| Finish | 24 Apr 2026 | 1 Mei 2026 |
| Duration | 53 hari | 58 hari |
| Cost | Rp219.678.233 | Rp234.678.233 |
| Baseline 0 | Rp219.678.233 | Rp219.678.233 |
| Baseline 1 | — | Rp234.678.233 |
| Status Date | 20 Mar 2026 | 1 Mei 2026 |

---

## 4. Checklist C — M8 WPD/Earned Value

| No | Item | Bukti | Status |
|---|---|---|---|
| C1 | Status date dan baseline | M8_PROGRESS | Tersedia |
| C2 | Tabel WPD (BAC, EV, AC, CV) | Dokumen M8 | Tersedia |
| C3 | Tabel PV, EV, SV, SPI | Dokumen M8 | Tersedia |
| C4 | Perhitungan CPI, SPI, EAC, ETC, VAC, TCPI | Dokumen M8 | Tersedia |
| C5 | Analisis varians biaya | Dokumen M8 | Tersedia |
| C6 | Analisis varians jadwal | Dokumen M8 | Tersedia |
| C7 | S-Curve / Earned Value Over Time | Screenshot MS Project | **Perlu screenshot** |
| C8 | Tabel Earned Value | Screenshot MS Project | **Perlu screenshot** |
| C9 | Gantt % Complete | Screenshot MS Project | **Perlu screenshot** |
| C10 | Corrective actions | Dokumen M8 | Tersedia |

Angka acuan M8:

- BAC work packages: Rp216.678.233
- PV: ±Rp149.897.333
- EV/AC: Rp122.578.233
- CV: Rp0
- SV: −Rp27.319.100
- CPI: 1,00
- SPI: 0,818
- EAC: Rp216.678.233
- VAC: Rp0

---

## 5. Checklist D — M9 Change Management

| No | Item | Bukti | Status |
|---|---|---|---|
| D1 | Form Change Request 02/CR/2026 | `docs/06-cr-form.md` | Tersedia |
| D2 | Analisis dampak scope | Bab 7.1 | Tersedia |
| D3 | Analisis dampak jadwal | Bab 7.2 | Tersedia |
| D4 | Analisis dampak biaya | Bab 7.3 | Tersedia |
| D5 | Analisis dampak resource | Bab 7.4 | Tersedia |
| D6 | Analisis dampak kualitas | Bab 7.5 | Tersedia |
| D7 | Analisis dampak risiko | Bab 7.6 | Tersedia |
| D8 | Opsi yang dipertimbangkan | Bab 8 | Tersedia |
| D9 | Notulen CCB | Bab 9 | Tersedia |
| D10 | Keputusan dan syarat | Bab 9.4 | Tersedia |
| D11 | CR log | `docs/07-cr-log.md` (`docs/xlsx/07-cr-log.xlsx`) | Tersedia |
| D12 | Baseline 1 ditetapkan | Bab 10.3 | Tersedia |
| D13 | Sign-off | Lampiran C | Perlu tanda tangan |

Angka acuan M9:

- 02/CR/2026: 5 hari, Rp15.000.000.
- Baseline 0: 24 Apr 2026, Rp219.678.233.
- Baseline 1: 1 Mei 2026, Rp234.678.233.
- Status: Closed 1 Mei 2026.

---

## 6. Checklist E — M10 Closing Report

| No | Item | Bukti | Status |
|---|---|---|---|
| E1 | Ringkasan eksekutif | Bagian A | Tersedia |
| E2 | Verifikasi lingkup dan deliverable | Bagian B | Tersedia |
| E3 | Kinerja jadwal (B0 vs B1) | Bagian C | Tersedia |
| E4 | Kinerja biaya (EVM akhir) | Bagian D | Tersedia |
| E5 | Kualitas, risiko, dan KPI | Bagian E | Tersedia |
| E6 | Manajemen perubahan | Bagian F | Tersedia |
| E7 | Lessons learned | Bagian G | Tersedia |
| E8 | Serah terima dan sign-off | Bagian H | Tersedia |
| E9 | Risk register | `docs/05-risk-register.md` | Tersedia | Ringkasan; lampirkan file asli jika ada |
| E10 | Screenshot Project Statistics | MS Project | **Perlu screenshot** |
| E11 | Screenshot tabel EV akhir | MS Project | **Perlu screenshot** |
| E12 | Screenshot Gantt Baseline 1 | MS Project | **Perlu screenshot** |

Angka acuan M10:

- EV: Rp219.678.233
- AC: Rp234.678.233
- CV: −Rp15.000.000
- CPI: 0,936
- EAC: Rp234.678.233
- VAC: −Rp15.000.000
- Finish: 1 Mei 2026

---

## 7. Checklist F — Format dan Submission

| No | Item | Status | Catatan |
|---|---|---|---|
| F1 | Markdown source | Tersedia | Folder `docs/` |
| F2 | DOCX | Tersedia | Hasil pandoc |
| F3 | PDF | Tersedia | Hasil pandoc + xelatex |
| F4 | Penomoran halaman | Perlu dicek | Sesuaikan template kampus |
| F5 | Cover dan identitas kelompok | Perlu dicek | Tambahkan nama/NIM jika diminta |
| F6 | Daftar isi | Perlu dicek | Generate otomatis di Word/PDF |
| F7 | Penamaan file | Selesai | `01-...`, `02-...`, `03-...`, `04-...` |
| F8 | Upload ke LMS | Belum | Sesuai instruksi kampus |
| F9 | Push ke GitHub | Selesai | Commit terakhir dicek sebelum submit |

---

## 8. Catatan Penting

1. **Impor ulang XML terbaru.** File `.mpp` yang dibuat dari XML versi awal memiliki durasi memanjang karena `Remaining Duration` dan tanggal assignment masih membawa nilai lama. XML terbaru sudah diperbaiki. Buka XML → Save As `.mpp`, lalu cek **Project → Statistics**.
2. **Jangan menimpa Baseline 0.** Baseline 0 adalah pembanding tetap. Baseline 1 sudah terisi di file FINAL.
3. **Setelah impor, tekan F9** untuk recalculate. Jika ada pergeseran 1 hari pada 1.6.3, set ulang Baseline 1 dan gunakan tanggal hasil recalculate.
4. **Screenshot M8** harus diambil dari file `M8_PROGRESS.mpp` dengan status date 20 Maret 2026 dan Baseline for Earned Value = Baseline.
5. **Screenshot M10** harus diambil dari file `M9_M10_FINAL.mpp` dengan Baseline 0 dan Baseline 1 terlihat.
6. **Risk Register** perlu dilampirkan jika dosen meminta file terpisah; ringkasan sudah ada di M10 Bagian E.
7. **Sign-off** perlu tanda tangan basah/digital dari Sponsor, PM, dan User Representative.

---

## 9. File Deliverable

| File | Deskripsi |
|---|---|
| `docs/01-change-management.md` | M9 Change Management |
| `docs/02-closing-report.md` | M10 Closing Report |
| `docs/03-wpd-earned-value.md` | M8 WPD/EVM |
| `docs/04-cp3-checklist.md` | Checklist ini |
| `docs/05-risk-register.md` | Risk Register ringkasan |
| `docs/06-cr-form.md` | Form Change Request 02/CR/2026 (sumber pengisian template DOCX) |
| `docs/07-cr-log.md` | CR Log (sumber pengisian template XLSX) |
| `docs/xlsx/07-cr-log.xlsx` | CR Log dalam format template Excel |
| `Projek Akhir MPTI_RFID pelacakan bagasi bandara_FIXED.xml` | Jadwal bersih |
| `Projek Akhir MPTI_RFID pelacakan bagasi bandara_M8_PROGRESS.xml` | Progress M8 |
| `Projek Akhir MPTI_RFID pelacakan bagasi bandara_M9_M10_FINAL.xml` | 02/CR/2026 + Baseline 1 |

---

*Checklist ini digunakan untuk memastikan seluruh deliverable CP3 lengkap sebelum submission.*
