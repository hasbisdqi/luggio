# Formulir Permintaan Perubahan (Change Request Form)

## Proyek LUGGIO — Sistem Pelacakan Bagasi RFID Bandara Indo-Aero

| Item | Keterangan |
|---|---|
| Nomor Formulir | LUGGIO-CP3-CR-001 |
| Nomor CR | **CR-001** — Form **02/CR/2026** |
| Tipe CR | Preventive Action |
| Prioritas | High |
| Versi | 1.0 |
| Tanggal Pengajuan | 18 Maret 2026 |
| Status | Closed — 1 Mei 2026 |
| Proyek | LUGGIO: Sistem Pelacakan Bagasi RFID Bandara Indo-Aero |
| Baseline Terdampak | Baseline 0 (24 April 2026) → Baseline 1 (1 Mei 2026) |
| Dokumen terkait | Project Charter v1.0; MPP LUGGIO; M9 Change Management; CR Log |
| Pemohon | Muhammad Nabiel Lukman Hakim — System Analyst |
| Keputusan CCB | Disetujui dengan syarat, 24 Maret 2026 |

---

## Bagian 1 — Identitas Pemohon

| Field | Isi |
|---|---|
| Nama pemohon | Muhammad Nabiel Lukman Hakim |
| Jabatan | System Analyst — Divisi TI Bandara Indo-Aero |
| Unit kerja | Divisi TI |
| Kontak | Nabielluqman@gmail.com |
| Tanggal pengajuan | 18 Maret 2026 |
| Peran dalam proyek | Analis kebutuhan dan spesifikasi integrasi DCS |

---

## Bagian 2 — Ringkasan Perubahan

| Field | Isi |
|---|---|
| Judul CR | Pengembangan Middleware & Adaptor API DCS |
| Kategori | Perubahan teknis dan lingkup (integrasi sistem eksternal) |
| Prioritas | Tinggi |
| Jenis perubahan | Penambahan pekerjaan baru (WBS 1.4.7) |
| WBS terdampak | 1.4.7 (baru), 1.6.1, 1.6.2, 1.6.3, 1.6.4, 1.6.5, 1.6.6 |
| Requirement terkait | FR-10 (integrasi DCS), FR-03 (respons real-time), FR-12 (audit log) |
| Perkiraan durasi | 5 hari kerja |
| Perkiraan biaya | Rp15.000.000 |
| Dampak jadwal | Finish 24 April 2026 → 1 Mei 2026 (+5 hari kerja) |
| Dampak biaya | BAC Rp219.678.233 → Rp234.678.233 (+Rp15.000.000) |

---

## Bagian 3 — Deskripsi Perubahan yang Diminta

Menambahkan **layanan middleware/adaptor** antara aplikasi LUGGIO dan *Departure Control System* (DCS) Bandara Indo-Aero.

Middleware tersebut berfungsi untuk:

1. Menerjemahkan pesan internal LUGGIO (REST/JSON) ke format protokol legacy DCS, dan sebaliknya.
2. Menangani antrean pesan, *retry*, dan *idempotency* agar data bagasi tidak duplikat atau hilang.
3. Mencatat *audit log* untuk setiap transaksi integrasi.
4. Menyediakan monitoring koneksi dan *alert* jika DCS tidak merespons.
5. Menyediakan mekanisme *fallback* dan sinkronisasi ulang setelah gangguan koneksi.

Pekerjaan ditempatkan sebagai **WBS 1.4.7**, setelah 1.4.6 (Fitur Ekspor Laporan Statistik, Log, dan Backup) dan sebelum fase pengujian 1.6.

---

## Bagian 4 — Alasan dan Justifikasi

### 4.1 Masalah yang Ditemukan

Saat penyusunan spesifikasi integrasi (WBS 1.2.3), tim menemukan bahwa:

1. DCS tidak menyediakan endpoint REST/JSON modern; komunikasi menggunakan protokol legacy.
2. Format pesan, kode penerbangan, dan struktur data bagasi berbeda dari model data internal LUGGIO.
3. Diperlukan mekanisme antrean, *retry*, *idempotency*, dan *audit log* untuk menjaga konsistensi data.
4. Integrasi langsung tanpa lapisan adaptor berisiko menggagalkan SIT/UAT dan tidak memenuhi FR-10.

### 4.2 Justifikasi Bisnis

- Memenuhi **FR-10** tanpa mengubah sistem DCS milik bandara.
- Menurunkan risiko kegagalan integrasi pada SIT/UAT.
- Menjaga akurasi data bagasi dan waktu respons dashboard di bawah 3 detik.
- Menyediakan jejak audit untuk investigasi bagasi nyasar.
- Biaya dan durasi masih berada di dalam pagu Charter Rp285.000.000.

### 4.3 Dampak Jika Tidak Dilakukan

- FR-10 tidak terpenuhi pada saat serah terima.
- Risiko kegagalan integrasi DCS tinggi; SIT/UAT berpotensi mundur lebih dari 5 hari.
- Data bagasi berisiko duplikat atau hilang saat koneksi terputus.

---

## Bagian 5 — Alternatif yang Dipertimbangkan

| Opsi | Deskripsi | Biaya | Durasi | Risiko | Keputusan |
|---|---|---:|---:|---|---|
| A | Integrasi langsung tanpa middleware | Rp0 | 0 hari | Tinggi | Ditolak |
| B | Lisensi middleware vendor | ±Rp25.000.000 | ±10 hari | Rendah | Ditolak (biaya/lead time) |
| C | Middleware/adaptor in-house | Rp15.000.000 | 5 hari | Sedang | **Dipilih** |
| D | Menunda integrasi setelah go-live | Rp0 | 0 hari | Tinggi | Ditolak (FR-10 tidak terpenuhi) |

Alasan memilih Opsi C: biaya terkendali, sesuai kebutuhan spesifik DCS, dapat dipelihara tim internal, dan tidak menambah ketergantungan vendor.

---

## Bagian 6 — Analisis Dampak

### 6.1 Dampak terhadap Lingkup

| Aspek | Sebelum CR | Setelah CR |
|---|---|---|
| Integrasi DCS | Diasumsikan langsung dari backend | Melalui middleware/adaptor khusus |
| WBS | Tidak ada task middleware | Task 1.4.7, 5 hari |
| Pengujian | Tanpa skenario middleware | Tambah 12 skenario integrasi, retry, idempotency |
| Dokumen | Spesifikasi integrasi | Desain adaptor, runbook, integration test report |
| Hardware | Tidak berubah | Tidak berubah |
| Lingkup bisnis | Tidak berubah | Tidak berubah |

Tidak ada *deliverable* yang dihapus atau dikurangi.

### 6.2 Dampak terhadap Jadwal

| Item | Baseline 0 | Baseline 1 | Variance |
|---|---|---|---:|
| Tanggal mulai | 9 Februari 2026 | 9 Februari 2026 | 0 |
| Tanggal selesai | 24 April 2026 | **1 Mei 2026** | **+5 hari kerja** |
| Durasi proyek | 53 hari | **58 hari** | +5 hari (+9,43%) |
| Milestone 3 | 24 April 2026 | **1 Mei 2026** | +5 hari |

Task yang bergeser:

| WBS | Task | Baseline 0 | Baseline 1 |
|---|---|---|---|
| 1.4.7 | Middleware & Adaptor API DCS | — | 2–8 April 2026 |
| 1.6.1 | Pengujian Seluruh Modul | 2–9 April 2026 | 9–16 April 2026 |
| 1.6.2 | Laporan SIT | 2–8 April 2026 | 9–15 April 2026 |
| 1.6.3 | Laporan UAT & Simulasi Bagasi Nyasar | 10–15 April 2026 | 17–22 April 2026 |
| 1.6.4 | Pelatihan Staf | 16–21 April 2026 | 23–28 April 2026 |
| 1.6.5 | Laporan Akhir & Serah Terima | 22–24 April 2026 | 29 April–1 Mei 2026 |
| 1.6.6 | Milestone 3 | 24 April 2026 | 1 Mei 2026 |

Jalur kritis setelah perubahan: **1.4.6 → 1.4.7 → 1.6.1/1.6.2 → 1.6.3 → 1.6.4 → 1.6.5 → 1.6.6**.

### 6.3 Dampak terhadap Biaya

| Item | Nilai |
|---|---:|
| Baseline 0 (BAC) | Rp219.678.233 |
| Biaya CR-001 | Rp15.000.000 |
| Baseline 1 (BAC) | **Rp234.678.233** |
| Variance | +Rp15.000.000 (+6,83%) |
| Pagu Charter | Rp285.000.000 |
| Sisa pagu setelah CR | **Rp50.321.767** |
| Contingency reserve proyek | Rp13.500.000 (tidak ditarik khusus untuk CR) |
| Management reserve awal | Rp65.321.767 |
| Management reserve setelah CR | Rp50.321.767 |

Rincian estimasi biaya:

| Komponen | Volume | Tarif | Total |
|---|---:|---:|---:|
| Analisis dan desain adaptor | 2 hari | Rp3.500.000/hari | Rp7.000.000 |
| Implementasi dan unit test | 2 hari | Rp3.000.000/hari | Rp6.000.000 |
| Integrasi, dokumentasi, serah terima | 1 hari | Rp2.000.000/hari | Rp2.000.000 |
| **Total** | **5 hari** | | **Rp15.000.000** |

### 6.4 Dampak terhadap Resource

| Resource | Alokasi | Keterangan |
|---|---|---|
| System Analyst | 2 hari | Desain kontrak antarmuka dan pemetaan data |
| Software Developer | 2 hari | Implementasi adaptor dan unit test |
| QA / Tester | 1 hari | Integration test dan regresi |
| Project Manager | Parsial | Monitoring, CCB, pembaruan baseline |
| Hardware/vendor | Tidak ada | Tidak ada pengadaan baru |

Tidak diperlukan penambahan personel tetap; beban diserap tim yang ada.

### 6.5 Dampak terhadap Kualitas

Pengujian tambahan:

- 12 skenario integrasi DCS (normal, timeout, duplikasi, retry, data tidak valid).
- 4 skenario gangguan koneksi dan sinkronisasi ulang.
- 2 skenario performa (respons <3 detik dan throughput puncak).
- Regresi modul yang terdampak.

Kriteria penerimaan:

- 100% skenario kritis lulus.
- Tidak ada kehilangan atau duplikasi data bagasi.
- Waktu respons dashboard tetap <3 detik.
- Audit log terbentuk untuk setiap transaksi.
- Tidak ada *critical defect* terbuka saat UAT.

### 6.6 Dampak terhadap Risiko

| Risiko | Sebelum | Setelah | Respons |
|---|---|---|---|
| Ketidakcocokan protokol DCS | Tinggi | Rendah | Middleware, contract test, simulator |
| Keterlambatan integrasi | Tinggi | Sedang | Jadwal 5 hari, monitoring harian |
| Duplikasi/kehilangan data | Sedang | Rendah | Idempotency, queue, retry, audit log |
| Ketergantungan vendor DCS | Sedang | Rendah | Koordinasi awal dan akses simulator |
| Overrun biaya CR | Rendah | Rendah | Cap Rp15.000.000, laporan biaya mingguan |
| Konflik resource | Sedang | Rendah | Alokasi SA/Developer/QA sejak awal |

### 6.7 Dampak terhadap Pengadaan dan Kontrak

Tidak ada pengadaan hardware baru. Middleware dikembangkan in-house menggunakan server lokal yang sudah ada. Tidak diperlukan amendemen kontrak vendor perangkat keras.

---

## Bagian 7 — Rekomendasi Pemohon

Pemohon merekomendasikan **Opsi C (middleware in-house)** untuk disetujui dengan syarat:

1. Biaya tidak melebihi Rp15.000.000.
2. Integration test dengan simulator DCS lulus sebelum SIT.
3. Tidak ada perubahan pada sistem DCS inti.
4. Baseline 1 ditetapkan setelah jadwal diperbarui.
5. Status CR dilaporkan pada rapat mingguan sampai ditutup.

---

## Bagian 8 — Keputusan CCB

| Field | Isi |
|---|---|
| Tanggal rapat CCB | 24 Maret 2026 |
| Waktu | 10.00–11.30 WIB |
| Tempat | Ruang Rapat Divisi TI / hybrid |
| Ketua | Ir. H. Max Verstappen (Project Sponsor) |
| Sekretaris | Muhammad Hasbi Assidiqi (Change Administrator) |
| Kuorum | 7 dari 7 anggota hadir |
| **Keputusan** | **Disetujui dengan syarat** |
| Tanggal keputusan | 24 Maret 2026 |
| Baseline 1 ditetapkan | 25 Maret 2026 |
| Status akhir | **Closed — 1 Mei 2026** |

### 8.1 Syarat Persetujuan

1. Biaya implementasi tidak melebihi Rp15.000.000.
2. Integration test dengan simulator DCS wajib lulus sebelum SIT.
3. Tidak ada perubahan pada sistem DCS inti; perubahan hanya pada sisi LUGGIO.
4. Baseline 1 ditetapkan setelah jadwal diperbarui; Baseline 0 tidak diubah.
5. Laporan status CR disampaikan pada rapat mingguan sampai CR ditutup.
6. Seluruh dokumen (desain, test report, runbook) diserahkan saat closing.

### 8.2 Catatan Rapat

1. System Analyst memaparkan temuan protokol legacy DCS dan risiko integrasi langsung.
2. Project Manager menyampaikan dampak: +5 hari kerja, +Rp15.000.000, finish 1 Mei 2026.
3. QA menyampaikan kebutuhan pengujian tambahan dan kriteria penerimaan.
4. User Representative memastikan perubahan tidak mengganggu jadwal operasional dan pelatihan.
5. Sponsor menegaskan proyek harus tetap di bawah pagu Rp285.000.000 dan tidak boleh mengurangi lingkup.

---

## Bagian 9 — Rencana Implementasi dan Verifikasi

| No | Aktivitas | PIC | Tanggal | Output | Status |
|---|---|---|---|---|---|
| 1 | Finalisasi desain dan setup environment | System Analyst | 2 April 2026 | Desain adaptor, environment siap | Selesai |
| 2 | Implementasi adaptor dan unit test | Software Developer | 3–6 April 2026 | Kode, unit test | Selesai |
| 3 | Integration test dengan simulator DCS | Developer/QA | 7–8 April 2026 | Integration test report | Selesai |
| 4 | SIT dan regresi | QA | 9–15 April 2026 | SIT report | Selesai |
| 5 | UAT dan simulasi bagasi nyasar | QA/User | 17–22 April 2026 | UAT sign-off | Selesai |
| 6 | Pelatihan dan sosialisasi | Trainer/PM | 23–28 April 2026 | Training report | Selesai |
| 7 | Penutupan CR dan serah terima | Project Manager | 29 April–1 Mei 2026 | CR closed, closing report | Selesai |

### 9.1 Hasil Verifikasi

| Verifikasi | Hasil | Status |
|---|---|---|
| Unit test middleware | 100% test case lulus | Lulus |
| Integration test DCS simulator | 12/12 skenario lulus | Lulus |
| Pengujian retry/idempotency | Tidak ada duplikasi data | Lulus |
| Performa respons | 1,8 detik (<3 detik) | Lulus |
| SIT | 100% skenario kritis lulus | Lulus |
| UAT | 98,4% test case lulus; 2 defect minor ditutup | Lulus |
| Regresi modul terdampak | Tidak ada regresi kritis | Lulus |

### 9.2 Pembaruan Baseline

| Baseline | Tanggal selesai | Durasi | BAC | Status |
|---|---|---|---|---|
| Baseline 0 | 24 April 2026 | 53 hari | Rp219.678.233 | Tidak diubah |
| Baseline 1 | 1 Mei 2026 | 58 hari | Rp234.678.233 | Ditetapkan 25 Maret 2026 |

---

## Bagian 10 — Tanda Tangan

| Nama | Jabatan | Peran | Tanda tangan | Tanggal |
|---|---|---|---|---|
| Muhammad Nabiel Lukman Hakim | System Analyst | Pemohon |  | 18 Maret 2026 |
| Ir. Primary Putri Ardiva | Kepala Divisi TI | Project Manager |  | 24 Maret 2026 |
| Ir. H. Max Verstappen | Direktur Operasional | Project Sponsor / Ketua CCB |  | 24 Maret 2026 |
| Muhammad Hasbi Assidiqi | Network/Hardware Engineer | Change Administrator |  | 24 Maret 2026 |
| Rusdi | Koordinator Ground Handling & Check-In | User Representative |  | 24 Maret 2026 |

---

## Lampiran — Checklist Kelengkapan CR

- [x] Identitas pemohon lengkap.
- [x] Deskripsi perubahan jelas.
- [x] Justifikasi bisnis dan dampak jika tidak dilakukan.
- [x] Alternatif dipertimbangkan.
- [x] Analisis dampak scope, jadwal, biaya, resource, kualitas, risiko, dan pengadaan.
- [x] Rekomendasi pemohon.
- [x] Keputusan CCB dan syarat.
- [x] Rencana implementasi dan verifikasi.
- [x] Pembaruan baseline.
- [x] Tanda tangan.

---

*Formulir ini merupakan lampiran CP3 Proyek LUGGIO dan disusun berdasarkan Project Charter v1.0, jadwal MPP, serta data Baseline 0 dan Baseline 1.*