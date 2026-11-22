# CHANGE REQUEST FORM

**PT. Angkasa Pura / Bandara Indo-Aero**

| Informasi | Detail | Informasi | Detail |
|---|---|---|---|
| **Nama Proyek** | LUGGIO – Sistem Pelacakan Bagasi Bandara | **Tanggal Pengajuan** | 21/03/2026 |
| **Nama Pemohon** | Muhammad Nabiel Lukman Hakim — System Analyst | **Nama Pengajuan** | Pengembangan Validasi dan Retry RFID |
| **ID Request** | CR-002/LUGGIO/2026 | **Tipe CR** | Corrective Action — Scope, Schedule, Cost |
| **Prioritas CR** | Low: [ ] | Medium: [x] | High: [ ] |

### Deskripsi Perubahan

Penambahan work package berupa pengembangan mekanisme validasi pembacaan RFID dan fitur retry otomatis ketika proses pembacaan tag RFID gagal. Fitur ini bertujuan meningkatkan keandalan sistem dalam mendeteksi dan mencatat perpindahan bagasi.

Work package ditempatkan sebagai **WBS 1.4.8 — Validasi dan Retry Pembacaan RFID**, setelah 1.4.7 (Middleware & Adaptor API DCS) dan sebelum fase pengujian 1.6.

### Alasan Pengajuan

Berdasarkan hasil pengujian perangkat RFID, ditemukan adanya kemungkinan kegagalan pembacaan tag akibat posisi tag, gangguan sinyal, atau kondisi perangkat pembaca. Oleh karena itu, diperlukan mekanisme validasi dan percobaan pembacaan ulang untuk mengurangi kesalahan pencatatan data bagasi.

### Dampak Perubahan

| Scope | Duration | Cost |
|---|---|---|
| Penambahan 1 work package: Pengembangan Validasi dan Retry RFID (WBS 1.4.8) | Tambahan 3 hari kerja pada aktivitas terkait. Dikerjakan secara paralel agar tanggal selesai proyek (24 April 2026) tidak berubah. | +Rp8.000.000 |

Rincian biaya:

| Komponen | Volume | Tarif | Total |
|---|---|---:|---:|
| Analisis aturan validasi dan desain retry | 1 hari | Rp3.000.000/hari | Rp3.000.000 |
| Implementasi dan unit test | 1 hari | Rp3.000.000/hari | Rp3.000.000 |
| Integration test dan tuning pembaca RFID | 1 hari | Rp2.000.000/hari | Rp2.000.000 |
| **Total** | **3 hari** | | **Rp8.000.000** |

### Keputusan

| Approved | Rejected | Deferred |
|---|---|---|
| [x] | [ ] | [ ] |

| Informasi | Detail |
|---|---|
| **Tanggal Keputusan** | 24/03/2026 |
| **Pembuat Keputusan** | Change Control Board (CCB) – Project Manager dan Sponsor |

**Catatan:** Perubahan disetujui dengan ketentuan bahwa tanggal penyelesaian akhir proyek tetap mengikuti baseline awal (24 April 2026). Pekerjaan dikerjakan paralel dengan aktivitas pengujian 1.6 sehingga tidak menggeser milestone akhir. Biaya Rp8.000.000 dibebankan pada *management reserve* di dalam pagu Charter Rp285.000.000.

**Dicatat pada CR Log:** baris 2 — ID CR `02/CR/2026`, status *Approved*.

---

## Tanda Tangan

| Nama | Jabatan | Peran | Tanda tangan | Tanggal |
|---|---|---|---|---|
| Muhammad Nabiel Lukman Hakim | System Analyst | Pemohon |  | 21/03/2026 |
| Ir. Primary Putri Ardiva | Kepala Divisi TI | Project Manager |  | 24/03/2026 |
| Ir. H. Max Verstappen | Direktur Operasional | Project Sponsor / Ketua CCB |  | 24/03/2026 |
| Muhammad Hasbi Assidiqi | Network/Hardware Engineer | Change Administrator |  | 24/03/2026 |

---

*Formulir ini merupakan lampiran CP3 Proyek LUGGIO — Change Request 02/CR/2026.*