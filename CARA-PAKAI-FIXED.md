# Paket XML CP3 — Jadwal, M8, dan M9/M10

Ada **tiga file XML** di folder ini. Semuanya berasal dari jadwal yang sama
(Baseline 0: 9 Feb – 24 Apr 2026, 53 hari kerja), tetapi disiapkan untuk
kebutuhan yang berbeda.

| File | Isi | Dipakai untuk |
|---|---|---|
| `Projek Akhir MPTI_RFID pelacakan bagasi bandara_FIXED.xml` | Jadwal bersih, Baseline 0, **tanpa** progress dan **tanpa** CR | Master / arsip. Jika ingin mulai dari nol. |
| `Projek Akhir MPTI_RFID pelacakan bagasi bandara_M8_PROGRESS.xml` | Baseline 0 + progress simulasi per **20 Mar 2026** | Screenshot **M8**: EV table, EV over time, S-Curve, Gantt progress. |
| `Projek Akhir MPTI_RFID pelacakan bagasi bandara_M9_M10_FINAL.xml` | Baseline 0 + **01/CR/2026** + **02/CR/2026** (paralel) + semua task 100% | Screenshot **M9** (verifikasi CR) dan **M10** (closing/final EV). |

> File `.mpp` tidak bisa dibuat di macOS. Buka XML di MS Project (Windows),
> lalu **Save As** menjadi `.mpp` dengan nama yang sesuai.

> **PENTING — impor ulang XML terbaru (22 Nov 2026).**
> File `.mpp` yang dibuat dari XML versi awal masih memiliki durasi memanjang
> (contoh: finish 2027/2028) karena `Remaining Duration` dan tanggal assignment
> masih membawa nilai lama. XML di repo ini **sudah diperbaiki**: remaining
> duration = duration, dan tanggal assignment = tanggal task.
>
> Silakan buka ulang ketiga XML terbaru di MS Project, lalu **Save As** `.mpp`
> (timpa file lama). Setelah itu cek **Project → Statistics**:
>
> - FIXED dan M8_PROGRESS: finish **24 Apr 2026**, duration **53d**
> - FINAL: finish **24 Apr 2026**, duration **53d**, cost **Rp242.678.233**
>
> **Aturan CR (mulai revisi ini):** dua CR disetujui CCB 24 Mar 2026 —
> 01/CR/2026 Middleware API DCS (5 hari, Rp15.000.000) dan 02/CR/2026
> Validasi & Retry RFID (3 hari, Rp8.000.000). Keduanya **dikerjakan paralel
> di dalam _float_**, sehingga **tanggal selesai proyek tetap 24 Apr 2026**.
> Baseline 0 tidak digeser; yang berubah hanya **BAC** menjadi
> **Rp242.678.233**. Jangan menggeser milestone 1.6.6.
> - Tidak boleh ada tanggal 2027/2028 atau durasi >60 hari.
>
> Jika masih muncul durasi memanjang, jangan disimpan — beri tahu saya.

---

## 1. Kenapa jadwal asli 187 hari?

Bukan karena network-nya salah, tetapi karena:

1. **Task di-split manual** sehingga durasi ikut menghitung celah kosong:
   - 1.6.2 SIT: 5d → 30d
   - 1.6.3 UAT: 4d → 28d
   - 1.6.4 Pelatihan: 3d → 27d
   - 1.6.5 Laporan akhir: 3d → 27d
   - 1.5.3 Kalibrasi: 4d → 10d
   - 1.2.1 Survei: 5d → 8d
   - 1.4.1, 1.4.3, 1.4.6, 1.6.1: ada segmen terpisah
2. **Milestone 1.6.6** dijadwalkan manual dengan finish 29 Oktober 2026,
   padahal seluruh pekerjaan sudah selesai 30 September.

Baseline 0 di MPP asli sebenarnya sudah benar: **9 Feb – 24 Apr 2026, 53 hari**.
Perbaikan ini mengembalikan jadwal aktif agar sama dengan Baseline 0.

Satu hal lain yang diperbaiki: **baseline cost** di MPP asli tidak konsisten
(beberapa task punya baseline cost 0 atau nilai lama). Di ketiga XML ini
baseline cost sudah disamakan dengan biaya rencana, sehingga:

- **BAC (Baseline 0) = Rp219.678.233**
- Total cost proyek = **Rp219.678.233**
- Pagu Charter = **Rp285.000.000**
- Selisih Rp65.321.767 = **management reserve** (di luar BAC)

---

## 2. Ringkasan angka penting

### Baseline 0 (dipakai untuk Earned Value)

| Item | Nilai |
|---|---|
| Start | 9 Feb 2026 |
| Finish | **24 Apr 2026** |
| Durasi | **53 hari kerja** |
| Total cost / BAC | **Rp219.678.233** |
| Split task | 0 |

### M8 — status 20 Mar 2026 (file `M8_PROGRESS`)

| Item | Nilai |
|---|---|
| Status Date | 20 Mar 2026 |
| % Complete proyek | **51%** |
| Progress per fase | 1.1–1.3 = 100%; 1.4 = 50%; 1.5–1.6 = 0% |
| BAC (work packages) | Rp239.678.233 |
| EV (work packages) | **Rp122.578.233** |
| AC (work packages) | **Rp122.578.233** |
| PV (work packages) | ± **Rp149.897.333** |
| EV/AC total proyek | ± **Rp124.388.145** (termasuk fixed cost) |
| CV | **Rp0** |
| SV | ± **−Rp27.319.100** |
| CPI | **1,00** |
| SPI | **0,818** |
| EAC (work packages) | Rp239.678.233 |
| EAC total proyek | Rp242.678.233 |
| VAC | Rp0 |

Catatan: angka EV/AC/PV di tabel MS Project bisa berbeda tipis karena
pembulatan dan karena fixed cost proyek Rp3.000.000. Gunakan angka yang
muncul di **Project → Statistics** dan tabel **Earned Value** saat screenshot.
CPI tetap 1,00 dan SPI tetap sekitar 0,818.

### M9/M10 — setelah 01/CR/2026 dan 02/CR/2026 (file `M9_M10_FINAL`)

| Item | Baseline 0 (awal) | Setelah 2 CR |
|---|---|---|
| Finish | 24 Apr 2026 | **24 Apr 2026** |
| Durasi | 53 hari | **53 hari** |
| Total cost (BAC) | Rp219.678.233 | **Rp242.678.233** |
| 01/CR/2026 | — | +Rp15.000.000 (5 hari, paralel) |
| 02/CR/2026 | — | +Rp8.000.000 (3 hari, paralel) |

| Item | Nilai akhir |
|---|---|
| BAC | **Rp242.678.233** |
| EV | **Rp242.678.233** |
| AC | **Rp242.678.233** |
| CV | **Rp0** |
| CPI | **1,00** |
| EAC | **Rp242.678.233** |
| VAC | **Rp0** |
| SPI saat selesai | 1,00 |

CR di file FINAL (keduanya type **Corrective Action**):

| CR | WBS | Nama | Durasi | Biaya | Penjadwalan |
|---|---|---|---|---|---|
| 01/CR/2026 | 1.4.7 | Pengembangan Middleware API DCS | 5 hari | Rp15.000.000 | 2–8 Apr 2026, paralel (predecessor 1.4.6) |
| 02/CR/2026 | 1.4.8 | Pengembangan Validasi dan Retry RFID | 3 hari | Rp8.000.000 | 2–6 Apr 2026, paralel dengan 1.4.7 |

Karena keduanya paralel dan berada di dalam *float* fase pengembangan, fase
pengujian–penutupan **tidak bergeser** dan milestone 1.6.6 tetap 24 Apr 2026.

---

## 3. Cara pakai di komputer ber-MS Project

### A. File FIXED (master, opsional)

1. Buka MS Project → **File → Open → Browse**.
2. Pilih `..._FIXED.xml` (filter: *All Files* atau *XML*).
3. **File → Save As** → simpan sebagai
   `Projek Akhir MPTI_RFID pelacakan bagasi bandara_FIXED.mpp`.
4. Cek **Project → Project Information → Statistics**:
   Start 9 Feb 2026, Finish **24 Apr 2026**, Duration **53d**,
   Cost **Rp219.678.233**, Status Date 20 Mar 2026.
5. Gantt: tidak boleh ada bar terpotong; milestone 1.6.6 harus di 24 Apr.

### B. File M8_PROGRESS (untuk M8)

1. Buka `..._M8_PROGRESS.xml`, lalu **Save As**
   `..._M8_PROGRESS.mpp`.
2. Pastikan **Status Date = 20 Mar 2026**
   (Project → Project Information → Status Date).
3. Atur baseline untuk Earned Value:
   **File → Options → Advanced → Baseline for Earned Value = Baseline**.
4. Buka **View → Table → Earned Value** dan **Earned Value Over Time**
   (Visual Reports → Excel) untuk S-Curve.
5. Screenshot yang dibutuhkan M8:
   - tabel Earned Value (PV, EV, AC, CV, SV, CPI, SPI, EAC, VAC),
   - grafik Earned Value Over Time / S-Curve,
   - Gantt dengan % Complete,
   - Project Statistics.
6. Angka yang harus muncul: lihat tabel M8 di atas.

### C. File M9_M10_FINAL (untuk M9 dan M10)

1. Buka `..._M9_M10_FINAL.xml`, lalu **Save As**
   `..._M9_M10_FINAL.mpp`.
2. Cek **finish proyek tetap 24 Apr 2026** (milestone 1.6.6), durasi 53d.
3. Cek **cost total = Rp242.678.233** (BAC awal Rp219.678.233 + Rp23.000.000).
4. Cek task **1.4.7 Middleware API DCS** (5 hari, Rp15.000.000) dan
   **1.4.8 Validasi dan Retry RFID** (3 hari, Rp8.000.000); keduanya
   dijadwalkan paralel dan **tidak** memanjangkan jalur kritis.
5. Untuk M10, semua task sudah **100% complete**, status date 24 Apr 2026.
   Screenshot:
   - Project Statistics (finish 24 Apr 2026, cost Rp242.678.233),
   - tabel Earned Value akhir (EV, AC, CPI, EAC, VAC),
   - Gantt final dengan task 1.4.7 dan 1.4.8,
   - task 01/CR/2026 dan 02/CR/2026.
6. Angka akhir: EV Rp242.678.233; AC Rp242.678.233; CPI 1,00;
   EAC Rp242.678.233; VAC Rp0.

---

## 4. Hal yang perlu diperhatikan saat membuka di MS Project

1. **Jangan menggeser tanggal baseline.** Baseline 0 tetap 24 Apr 2026.
   Yang boleh diperbarui hanya biaya (BAC Rp242.678.233). Jika setelah
   recalculate finish bergeser, perbaiki durasi di dalam *float* — jangan
   memindahkan milestone 1.6.6.
2. Setelah file dibuka, tekan **F9** (Calculate Now). MS Project akan
   menghitung ulang summary dan sisa durasi.
3. Pada file FINAL, task 1.6.3 (UAT) mewarisi celah 1 hari dari baseline
   asli. Jika setelah F9 tanggalnya bergeser satu hari, itu normal selama
   **finish proyek tetap 24 Apr 2026**.
4. File M8 adalah **simulasi progress** sesuai skenario:
   1.1–1.3 100%, 1.4 50%, 1.5–1.6 0%. Kalau data aktual berbeda,
   ubah % Complete di MS Project — angka EV akan menyesuaikan otomatis.
5. Jangan mengubah **Actual Cost** task 1.3.1–1.3.3 secara manual kecuali
   perlu; di file M8 task-task itu sudah 100% sehingga AC-nya konsisten
   dengan biaya rencana.
6. Simpan sebagai `.mpp` **setelah** semua verifikasi, supaya file XML
   tetap menjadi arsip yang bisa dibuka ulang.

---

## 5. Batasan

File ini adalah **MSPDI XML**, bukan `.mpp`, karena mesin yang memprosesnya
(macOS) tidak memiliki MS Project. MS Project perlu membukanya sekali lalu
menyimpannya sebagai `.mpp`. Semua task, link, resource, kalender, baseline,
biaya, dan custom field sudah diperiksa ulang dan ikut terbawa.
