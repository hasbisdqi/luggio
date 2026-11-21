# Perbaikan Jadwal MPP — 187 hari → 53 hari (24 April 2026)

File: `Projek Akhir MPTI_RFID pelacakan bagasi bandara_FIXED.xml`

## Kenapa 187 hari?

Jadwal asli di MPP tidak rusak karena logika network, tapi karena:

1. **Task di-split manual** sehingga durasi ikut menghitung celah kosong:
   - 1.6.2 SIT: 5d → 30d
   - 1.6.3 UAT: 4d → 28d
   - 1.6.4 Pelatihan: 3d → 27d
   - 1.6.5 Laporan akhir: 3d → 27d
   - 1.5.3 Kalibrasi: 4d → 10d
   - 1.2.1 Survei: 5d → 8d
   - 1.4.1, 1.4.3, 1.4.6, 1.6.1: ada segmen terpisah
2. **Milestone 1.6.6** dijadwalkan manual dengan finish 29 Oktober 2026, padahal semua pekerjaan sudah selesai 30 September.

Baseline 0 di file asli sebenarnya sudah benar: **9 Feb – 24 Apr 2026, 53 hari**. Perbaikan ini mengembalikan jadwal aktif agar sama dengan baseline tersebut.

## Yang dilakukan file FIXED

| Item | Sebelum | Sesudah |
|---|---|---|
| Finish proyek | 29 Okt 2026 | **24 Apr 2026** |
| Durasi | 187 hari | **53 hari** |
| Split task | 10 task | **0** |
| Milestone 3 | manual, 29 Okt | auto, 24 Apr |
| Status Date | 20 Mar 2026 | 20 Mar 2026 (tetap) |
| Baseline 0 | ada | **tetap utuh** |
| Baseline 1 | ada (duplikat) | **dikosongkan** (diisi setelah CR-001) |
| Total cost | Rp219.678.233 | **Rp219.678.233** (tetap) |
| Actual cost | Rp34.015.133 | Rp34.015.133 (tetap) |
| Custom field | Text1, Text2 | tetap |
| Resource & kalender | lengkap | tetap |

## Cara pakai (di komputer ber-MS Project)

1. Backup file `.mpp` lama.
2. Buka MS Project → **File → Open → Browse**.
3. Pilih file `Projek Akhir MPTI_RFID pelacakan bagasi bandara_FIXED.xml`
   (ubah filter ke *All Files* / *XML*).
4. **File → Save As** → simpan sebagai `.mpp` dengan nama yang sama seperti aslinya.
5. Verifikasi lewat **Project → Project Information → Statistics**:

   | Field | Nilai yang harus muncul |
   |---|---|
   | Start | 9 Feb 2026 |
   | Finish | **24 Apr 2026** |
   | Duration | **53 hari** |
   | Work | ±1.488 jam |
   | Cost | **Rp219.678.233** |
   | Status Date | 20 Mar 2026 |

6. Cek Gantt: tidak boleh ada bar terpotong (split) dan milestone 1.6.6 harus di 24 Apr.

## Setelah file terbuka — lanjut M8

1. **Jangan set ulang Baseline 0.** Baseline 0 sudah benar dan dipakai untuk Earned Value.
2. Isi **% Complete** hanya di leaf task:
   - 1.1, 1.2, 1.3 → 100%
   - 1.4 → 50%
   - 1.5, 1.6 → 0%
3. **Perhatian:** task 1.3.1, 1.3.2, 1.3.3 sudah punya *Actual Cost* Rp34.015.133 tetapi **% Complete masih 0%**. Kalau dibiarkan, EV = 0 dan **CPI = 0**. Pilih salah satu:
   - isi % Complete ketiga task itu ke 100% (paling mudah), atau
   - kosongkan Actual Cost-nya dulu.
4. Set **Status Date = 20 Mar 2026** (sudah terisi di file).
5. Tampilkan tabel **Earned Value** dan **Earned Value Over Time** (Visual Reports) untuk S-Curve.
6. Setelah CR-001 disetujui, baru:
   - tambah task middleware 5 hari + Rp15.000.000,
   - **Set Baseline → Baseline 1** (jangan timpa Baseline 0).

## Catatan budget

Charter menetapkan pagu **Rp285.000.000**, sedangkan total cost di MPP **Rp219.678.233**. Selisih **Rp65.321.767** sebaiknya dijelaskan sebagai **management reserve** (di luar BAC), bukan dinaikkan ke cost task. Dengan begitu:

- BAC (EV) = Rp219.678.233
- Pagu yang tidak boleh dilampaui = Rp285.000.000
- CR-001 (+Rp15.000.000) masih aman di dalam pagu.

## Batasan

File ini adalah **MSPDI XML**, bukan `.mpp`, karena mesin yang memprosesnya (macOS) tidak memiliki MS Project. MS Project perlu membukanya sekali lalu menyimpannya sebagai `.mpp` seperti langkah di atas. Semua task, link, resource, kalender, baseline, biaya, dan custom field sudah diperiksa ulang dan ikut terbawa.
