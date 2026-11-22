# Change Request Log (CR Log)

## Proyek LUGGIO — Sistem Pelacakan Bagasi RFID Bandara Indo-Aero

| Item | Keterangan |
|---|---|
| Nomor Dokumen | LUGGIO-CP3-CRLOG-001 |
| Versi | 1.0 |
| Tanggal | 1 Mei 2026 |
| Status | Final |
| Proyek | LUGGIO: Sistem Pelacakan Bagasi RFID Bandara Indo-Aero |
| Periode | 9 Februari–1 Mei 2026 |
| Baseline | Baseline 0 (24 April 2026) → Baseline 1 (1 Mei 2026) |
| Disusun oleh | Muhammad Hasbi Assidiqi — Change Administrator |
| Persetujuan | Ir. Primary Putri Ardiva — Project Manager |
| Dokumen terkait | Form 02/CR/2026; M9 Change Management; M10 Closing Report |
| Jumlah CR | 1 diajukan; 1 disetujui; 1 ditutup |

---

## 1. Tujuan

CR Log digunakan untuk mencatat seluruh permintaan perubahan proyek secara berurutan, meliputi identitas CR, dampak biaya dan jadwal, keputusan CCB, status implementasi, serta penutupan. Log memastikan tidak ada perubahan yang dilaksanakan tanpa persetujuan dan menyediakan jejak audit (*audit trail*) untuk evaluasi proyek.

---

## 2. Aturan Pencatatan

1. Setiap permintaan perubahan wajib memiliki **ID unik** dengan format `CR-XXX`.
2. CR dicatat pada hari pengajuan, sebelum analisis dampak dimulai.
3. Status CR mengikuti alur: **Submitted → Under Review → Approved/Rejected → Implemented → Verified → Closed**.
4. Perubahan yang disetujui harus memperbarui baseline terkait (jadwal, biaya, lingkup) dan dokumen proyek.
5. CR yang ditolak tetap dicatat beserta alasan penolakan.
6. Perubahan darurat yang sudah dilaksanakan sebelum persetujuan wajib diretroaktifkan melalui CCB dan dicatat sebagai `Emergency`.

---

## 3. Ringkasan Log

| Total CR | Disetujui | Ditolak | Ditunda | Dalam proses | Ditutup |
|---:|---:|---:|---:|---:|---:|
| **1** | **1** | 0 | 0 | 0 | **1** |

Seluruh perubahan yang diajukan selama proyek telah selesai dan ditutup pada 1 Mei 2026.

---

## 4. Register Change Request

| ID | Tanggal | Pemohon | Judul | Kategori | Status | Tanggal Tutup |
|---|---|---|---|---|---|---|
| CR-001 (02/CR/2026) | 18 Mar 2026 | M. Nabiel L. H. | Pengembangan Middleware & Adaptor API DCS | Preventive Action / teknis-lingkup | Closed | 1 Mei 2026 |

### 4.1 Detail Dampak dan Keputusan

| Item | Isi |
|---|---|
| WBS | 1.4.7 (baru); 1.6.1–1.6.6 |
| Dampak biaya | +Rp15.000.000 |
| Dampak jadwal | +5 hari kerja |
| Keputusan CCB | Disetujui dengan syarat, 24 Maret 2026 |
| Baseline 0 | 24 April 2026; Rp219.678.233 |
| Baseline 1 | 1 Mei 2026; Rp234.678.233 |

Detail CR-001 tersedia pada **Form Change Request 02/CR/2026** (`docs/06-cr-form.md`).

---

## 5. Riwayat Status CR-001

| Tanggal | Status | Aktivitas | PIC |
|---|---|---|---|
| 18 Mar 2026 | Submitted | Pengajuan CR oleh System Analyst | M. Nabiel L. H. |
| 18–23 Mar 2026 | Under Review | Analisis dampak scope, jadwal, biaya, resource, kualitas, risiko | PM, SA, QA |
| 24 Mar 2026 | Approved | Rapat CCB dan keputusan | Sponsor / CCB |
| 25 Mar 2026 | Baseline Updated | Baseline 1 ditetapkan | PM |
| 2–8 Apr 2026 | Implemented | Desain, implementasi, unit test, integration test | SA, Developer, QA |
| 9–15 Apr 2026 | Verified | SIT dan regresi | QA |
| 17–22 Apr 2026 | Verified | UAT dan simulasi bagasi nyasar | QA / User |
| 23–28 Apr 2026 | Implemented | Pelatihan dan sosialisasi | Trainer / PM |
| 1 Mei 2026 | Closed | Serah terima dan penutupan CR | PM |

### 5.1 Catatan Penting per Tahap

| Tahap | Catatan |
|---|---|
| Submitted | Temuan protokol legacy DCS saat desain integrasi. |
| Under Review | Opsi A–D dievaluasi; Opsi C (middleware in-house) dipilih. |
| Approved | Disetujui dengan 6 syarat; Baseline 1 ditetapkan 25 Maret 2026. |
| Implemented | 5 hari kerja; 12/12 skenario integration test lulus. |
| Verified | SIT 100% skenario kritis lulus; UAT 98,4% lulus, 2 defect minor ditutup. |
| Closed | CR ditutup bersama closing report; 50 personel terlatih. |

## 6. Dampak Kumulatif terhadap Baseline

| Baseline | Tanggal Selesai | Durasi | BAC | Status |
|---|---|---:|---:|---|
| Baseline 0 (awal) | 24 April 2026 | 53 hari | Rp219.678.233 | Tidak diubah |
| Baseline 1 (setelah CR-001) | 1 Mei 2026 | 58 hari | Rp234.678.233 | Aktif sampai closing |

| Item | Baseline 0 | Baseline 1 | Selisih |
|---|---:|---:|---:|
| Durasi | 53 hari | 58 hari | +5 hari (+9,43%) |
| Biaya | Rp219.678.233 | Rp234.678.233 | +Rp15.000.000 (+6,83%) |
| Milestone 3 | 24 April 2026 | 1 Mei 2026 | +5 hari |
| Pagu tersisa | Rp65.321.767 | Rp50.321.767 | −Rp15.000.000 |

---

## 7. CR yang Ditolak atau Ditunda

| ID | Tanggal | Deskripsi | Alasan | Status |
|---|---|---|---|---|
| — | — | Tidak ada | — | — |

Tidak ada CR yang ditolak atau ditunda selama proyek. Opsi alternatif di dalam CR-001 (integrasi langsung, vendor middleware, dan penundaan integrasi) ditolak pada tingkat analisis opsi, bukan sebagai CR terpisah.

---

## 8. Lessons Learned dari Pengelolaan CR

1. **Validasi antarmuka eksternal sejak perencanaan.** Protokol DCS seharusnya diverifikasi sebelum baseline disetujui.
2. **Satu CR, satu formulir, satu keputusan.** Pemisahan formulir dan log membuat jejak audit lebih jelas.
3. **Dampak harus terukur.** CR-001 memiliki angka pasti: +5 hari dan +Rp15.000.000.
4. **Baseline 0 tidak boleh diubah.** Baseline 1 digunakan untuk menilai kinerja setelah perubahan.
5. **Status CR harus diperbarui pada rapat mingguan** agar tidak ada perubahan yang menggantung.

---

## 9. Tanda Tangan

| Nama | Jabatan | Peran | Tanda tangan | Tanggal |
|---|---|---|---|---|
| Muhammad Hasbi Assidiqi | Network/Hardware Engineer | Change Administrator |  | 1 Mei 2026 |
| Ir. Primary Putri Ardiva | Kepala Divisi TI | Project Manager |  | 1 Mei 2026 |
| Ir. H. Max Verstappen | Direktur Operasional | Project Sponsor |  | 1 Mei 2026 |

---

## Lampiran — Rekap per Kategori

| Kategori | Jumlah CR | Dampak Biaya | Dampak Jadwal |
|---|---:|---:|---:|
| Teknis / lingkup | 1 | +Rp15.000.000 | +5 hari |
| Jadwal | 0 | — | — |
| Biaya | 0 | — | — |
| Kualitas | 0 | — | — |
| **Total** | **1** | **+Rp15.000.000** | **+5 hari** |

---

*Dokumen ini merupakan lampiran CP3 Proyek LUGGIO dan menjadi bagian dari M9 Change Management.*