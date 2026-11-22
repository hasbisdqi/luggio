# CHANGE REQUEST FORM

**PT. Angkasa Pura / Bandara Indo-Aero**

| Informasi | Detail | Informasi | Detail |
|---|---|---|---|
| **Nama Proyek** | LUGGIO – Sistem Pelacakan Bagasi Bandara | **Tanggal Pengajuan** | 18/03/2026 |
| **Nama Pemohon** | Muhammad Nabiel Lukman Hakim — System Analyst | **Nama Pengajuan** | Pengembangan Middleware API DCS |
| **ID Request** | CR-001/LUGGIO/2026 | **Tipe CR** | Corrective Action — Scope, Schedule, Cost |
| **Prioritas CR** | Low: [ ] | Medium: [ ] | High: [x] |

### Deskripsi Perubahan

Penambahan work package berupa pengembangan Middleware API DCS untuk mengatasi ketidakcocokan antara API sistem *Departure Control System* (DCS) bandara dengan sistem LUGGIO. Middleware diperlukan sebagai lapisan penghubung agar proses pertukaran dan sinkronisasi data bagasi dapat berjalan dengan baik.

Work package ditempatkan sebagai **WBS 1.4.7 — Pengembangan Middleware & Adaptor API DCS**, setelah 1.4.6 (Fitur Ekspor Laporan Statistik, Log, dan Backup) dan sebelum fase pengujian 1.6.

### Alasan Pengajuan

Berdasarkan hasil pengujian integrasi, ditemukan bahwa API DCS membutuhkan penyesuaian tambahan agar dapat berkomunikasi dengan sistem LUGGIO. Perubahan ini diperlukan untuk memastikan integrasi sistem berjalan stabil dan data bagasi dapat disinkronisasi secara akurat.

### Dampak Perubahan

| Scope | Duration | Cost |
|---|---|---|
| Penambahan 1 work package: Pengembangan Middleware API DCS (WBS 1.4.7) | Tambahan 5 hari kerja pada aktivitas terkait. Dikerjakan secara paralel agar tanggal selesai proyek (24 April 2026) tidak berubah. | +Rp15.000.000 |

Rincian biaya:

| Komponen | Volume | Tarif | Total |
|---|---|---:|---:|
| Analisis dan desain adaptor | 2 hari | Rp3.500.000/hari | Rp7.000.000 |
| Implementasi dan unit test | 2 hari | Rp3.000.000/hari | Rp6.000.000 |
| Integrasi, dokumentasi, serah terima | 1 hari | Rp2.000.000/hari | Rp2.000.000 |
| **Total** | **5 hari** | | **Rp15.000.000** |

### Keputusan

| Approved | Rejected | Deferred |
|---|---|---|
| [x] | [ ] | [ ] |

| Informasi | Detail |
|---|---|
| **Tanggal Keputusan** | 24/03/2026 |
| **Pembuat Keputusan** | Change Control Board (CCB) – Project Manager dan Sponsor |

**Catatan:** Perubahan disetujui dengan ketentuan bahwa tanggal penyelesaian akhir proyek tetap mengikuti baseline awal (24 April 2026). Pekerjaan dikerjakan paralel dengan aktivitas pengujian 1.6 sehingga tidak menggeser milestone akhir. Biaya Rp15.000.000 dibebankan pada *management reserve* di dalam pagu Charter Rp285.000.000.

**Dicatat pada CR Log:** baris 1 — ID CR `01/CR/2026`, status *Approved*.

---

## Tanda Tangan

| Nama | Jabatan | Peran | Tanda tangan | Tanggal |
|---|---|---|---|---|
| Muhammad Nabiel Lukman Hakim | System Analyst | Pemohon |  | 18/03/2026 |
| Ir. Primary Putri Ardiva | Kepala Divisi TI | Project Manager |  | 24/03/2026 |
| Ir. H. Max Verstappen | Direktur Operasional | Project Sponsor / Ketua CCB |  | 24/03/2026 |
| Muhammad Hasbi Assidiqi | Network/Hardware Engineer | Change Administrator |  | 24/03/2026 |

---

*Formulir ini merupakan lampiran CP3 Proyek LUGGIO — Change Request 01/CR/2026.*