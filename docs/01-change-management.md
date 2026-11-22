# Laporan Manajemen Perubahan (Change Management)

## Proyek LUGGIO — Sistem Pelacakan Bagasi RFID Bandara Indo-Aero

| Item | Keterangan |
|---|---|
| Nomor Dokumen | LUGGIO-CP3-M9-001 |
| Versi | 1.0 |
| Tanggal | 1 Mei 2026 |
| Status | Final |
| Proyek | LUGGIO: Sistem Pelacakan Bagasi RFID Bandara Indo-Aero |
| Baseline | Baseline 0 dan Baseline 1 |
| Penyusun | Muhammad Hasbi Assidiqi — Network/Hardware Engineer |
| Pemeriksa | Muhammad Nabiel Lukman Hakim — System Analyst |
| Persetujuan | Ir. Primary Putri Ardiva — Project Manager |
| Persetujuan | Ir. H. Max Verstappen — Project Sponsor |
| Dokumen terkait | Project Charter v1.0; MPP LUGGIO; Change Request Log; Closing Report |

---

## 1. Ringkasan Eksekutif

Selama tahap perancangan integrasi, tim menemukan bahwa *Departure Control System* (DCS) Bandara Indo-Aero masih menggunakan protokol dan format pesan legacy. Integrasi langsung dari aplikasi LUGGIO ke DCS berisiko tinggi terhadap kegagalan SIT, kehilangan data, dan tidak terpenuhinya FR-10. Oleh karena itu diajukan **Change Request CR-001** berupa penambahan layanan middleware/adaptor API DCS.

CR-001 telah dievaluasi oleh *Change Control Board* (CCB) pada **24 Maret 2026** dan disetujui dengan syarat. Dampak yang disetujui adalah penambahan **5 hari kerja** dan **Rp15.000.000**, sehingga Baseline 1 menjadi:

| Item | Baseline 0 | CR-001 | Baseline 1 |
|---|---:|---:|---:|
| Tanggal selesai | 24 April 2026 | +5 hari kerja | **1 Mei 2026** |
| Durasi | 53 hari | +5 hari | **58 hari** |
| Biaya (BAC) | Rp219.678.233 | +Rp15.000.000 | **Rp234.678.233** |

Perubahan ini tidak mengurangi lingkup, tidak mengubah pagu Charter sebesar Rp285.000.000, dan tidak menggunakan contingency reserve proyek. CR-001 dinyatakan **closed** pada 1 Mei 2026 setelah middleware terintegrasi, lulus SIT/UAT, dan diserahkan bersama dokumen penutupan proyek.

---

## 2. Latar Belakang

Proyek LUGGIO bertujuan menggantikan pemindaian barcode konvensional dengan RFID untuk mengurangi *unreadable rate* dari 8% menjadi di bawah 0,5%. Salah satu kebutuhan fungsional utama adalah **FR-10: integrasi dengan departure control system bandara untuk verifikasi data bagasi**.

Pada Project Charter v1.0, integrasi DCS tercantum sebagai bagian dari lingkup proyek, tetapi belum dirinci sebagai pekerjaan tersendiri di WBS. Saat spesifikasi integrasi disusun (WBS 1.2.3), tim menemukan bahwa:

1. DCS tidak menyediakan endpoint REST/JSON modern; komunikasi menggunakan protokol legacy.
2. Format pesan, kode penerbangan, dan struktur bagasi berbeda dari model data internal LUGGIO.
3. Diperlukan mekanisme antrean, *retry*, *idempotency*, dan *audit log* agar tidak terjadi duplikasi atau kehilangan data saat koneksi terputus.
4. Pengujian langsung tanpa lapisan adaptor berpotensi menggagalkan SIT dan UAT.

Temuan ini memenuhi kriteria perubahan karena memengaruhi **lingkup teknis, jadwal, biaya, dan risiko integrasi**. Sesuai prosedur manajemen perubahan, tim mengajukan CR-001 kepada CCB sebelum pekerjaan tambahan dilaksanakan.

---

## 3. Tujuan dan Ruang Lingkup Manajemen Perubahan

Tujuan penerapan manajemen perubahan pada proyek ini adalah:

1. Memastikan setiap perubahan lingkup, jadwal, biaya, atau kualitas dievaluasi secara formal.
2. Menjaga agar Baseline 0 tetap menjadi pembanding yang tidak berubah.
3. Menyediakan jejak audit (*audit trail*) atas keputusan perubahan.
4. Memastikan perubahan yang disetujui diimplementasikan, diuji, dan didokumentasikan.
5. Menjaga proyek tetap berada di dalam pagu Charter.

Ruang lingkup manajemen perubahan mencakup perubahan pada:

- lingkup pekerjaan dan *deliverable*;
- jadwal dan jalur kritis;
- biaya dan baseline biaya;
- kebutuhan fungsional/non-fungsional;
- risiko, kualitas, dan dokumen proyek.

---

## 4. Peran dan Tanggung Jawab

| Peran | Nama | Tanggung jawab dalam perubahan |
|---|---|---|
| Project Sponsor | Ir. H. Max Verstappen | Menyetujui perubahan yang berdampak pada pagu dan komitmen organisasi; ketua CCB. |
| Project Manager | Ir. Primary Putri Ardiva | Mengelola proses perubahan, memimpin analisis dampak, memperbarui baseline, dan melaporkan status. |
| Change Administrator | Muhammad Hasbi Assidiqi | Mencatat CR, mengelola log, menyiapkan dokumen CCB, dan mengarsipkan keputusan. |
| System Analyst | Muhammad Nabiel Lukman Hakim | Menganalisis dampak teknis dan kebutuhan integrasi; pemohon CR-001. |
| Software Developer | Santosa | Mengimplementasikan middleware/adaptor dan unit test. |
| QA / Tester | Siska | Menyusun test case integrasi, melaksanakan SIT/regresi, dan memverifikasi hasil. |
| User Representative | Rusdi | Memastikan perubahan tidak mengganggu proses operasional ground handling dan check-in. |

---

## 5. Prosedur Manajemen Perubahan

### 5.1 Identifikasi dan Pencatatan

Perubahan diidentifikasi oleh anggota tim, vendor, atau *user representative*. Change Administrator mencatatnya dalam **Change Request Log** dengan ID unik, tanggal, pemohon, deskripsi, dan kategori.

### 5.2 Analisis Dampak

Project Manager bersama System Analyst dan QA menganalisis dampak terhadap:

- lingkup dan *deliverable*;
- jadwal, jalur kritis, dan milestone;
- biaya, BAC, contingency, dan pagu;
- kualitas dan kriteria penerimaan;
- risiko dan resource;
- dokumen serta baseline.

### 5.3 Review CCB

CCB meninjau CR, analisis dampak, opsi penyelesaian, dan rekomendasi. CCB dapat:

- menyetujui tanpa syarat;
- menyetujui dengan syarat;
- menunda untuk meminta analisis tambahan;
- menolak.

### 5.4 Keputusan dan Komunikasi

Keputusan dicatat dalam notulen CCB dan dikomunikasikan kepada seluruh pemangku kepentingan. Perubahan yang disetujui menjadi dasar pembaruan jadwal dan baseline.

### 5.5 Implementasi

Pekerjaan perubahan dilaksanakan sesuai rencana, dengan PIC, tanggal, dan *output* yang jelas. Perubahan tidak boleh dilaksanakan sebelum disetujui, kecuali dalam kondisi darurat yang kemudian diretroaktifkan melalui CCB.

### 5.6 Verifikasi dan Penutupan

QA memverifikasi hasil melalui unit test, integration test, SIT, UAT, dan regresi. CR ditutup setelah kriteria penerimaan terpenuhi dan dokumen diperbarui.

### 5.7 Pembaruan Baseline dan Arsip

Baseline 0 tidak diubah. Setelah CR disetujui dan jadwal diperbarui, **Baseline 1** ditetapkan. Seluruh dokumen perubahan diarsipkan bersama laporan penutupan proyek.

---

## 6. Change Request CR-001

### 6.1 Identitas CR

| Field | Isi |
|---|---|
| ID CR | CR-001 |
| Tanggal pengajuan | 18 Maret 2026 |
| Pemohon | Muhammad Nabiel Lukman Hakim — System Analyst |
| Kategori | Perubahan teknis/lingkup (integrasi) |
| Prioritas | Tinggi |
| Status | Closed |
| WBS terdampak | 1.4.7 (baru), 1.6.1, 1.6.2, 1.6.3, 1.6.4, 1.6.5, 1.6.6 |
| Requirement terkait | FR-10, FR-03, FR-12 |
| Baseline | Baseline 0 → Baseline 1 |

### 6.2 Deskripsi Perubahan

Menambahkan **Pengembangan Middleware & Adaptor API DCS** sebagai pekerjaan baru di bawah WBS 1.4 (Pengembangan Software), setelah 1.4.6 (Fitur Ekspor Laporan Statistik, Log, dan Backup) dan sebelum fase pengujian 1.6.

Middleware berfungsi untuk:

1. Menerjemahkan pesan internal LUGGIO (REST/JSON) ke format legacy DCS dan sebaliknya.
2. Menangani antrean pesan, *retry*, dan *idempotency* agar data bagasi tidak duplikat.
3. Mencatat audit log setiap transaksi integrasi.
4. Menyediakan monitoring koneksi dan alert jika DCS tidak merespons.
5. Menyediakan mekanisme *fallback* dan sinkronisasi ulang setelah gangguan koneksi.

### 6.3 Justifikasi Bisnis

- Memenuhi FR-10 tanpa mengubah sistem DCS milik bandara.
- Mengurangi risiko kegagalan SIT/UAT akibat perbedaan protokol.
- Menjaga akurasi data bagasi dan waktu respons dashboard tetap di bawah 3 detik.
- Menyediakan jejak audit untuk investigasi bagasi nyasar.
- Biaya dan durasi masih berada di dalam pagu serta *management reserve* Charter.

### 6.4 Lingkup yang Berubah

| Aspek | Sebelum CR-001 | Setelah CR-001 |
|---|---|---|
| Integrasi DCS | Diasumsikan dapat dilakukan langsung dari backend | Melalui middleware/adaptor khusus |
| WBS | Tidak ada task middleware | Task 1.4.7, 5 hari |
| Pengujian | SIT/UAT tanpa skenario middleware | Tambah 12 skenario integrasi, retry, dan idempotency |
| Dokumen | Spesifikasi integrasi saja | Desain adaptor, runbook, integration test report |
| Hardware | Tidak berubah | Tidak berubah |
| Lingkup bisnis | Tidak berubah | Tidak berubah |

---

## 7. Analisis Dampak

### 7.1 Dampak terhadap Lingkup

CR-001 menambah satu *deliverable* teknis (middleware/adaptor) dan memperluas pengujian integrasi. Tidak ada *deliverable* yang dihapus atau dikurangi. Seluruh FR dalam Charter tetap berlaku.

### 7.2 Dampak terhadap Jadwal

| Item | Baseline 0 | Baseline 1 | Variance |
|---|---|---|---|
| Tanggal mulai | 9 Februari 2026 | 9 Februari 2026 | 0 |
| Tanggal selesai | 24 April 2026 | **1 Mei 2026** | **+5 hari kerja** |
| Durasi proyek | 53 hari | **58 hari** | +5 hari (+9,43%) |
| Milestone 3 | 24 April 2026 | **1 Mei 2026** | +5 hari |

Task yang bergeser:

| WBS | Task | Baseline 0 | Baseline 1 |
|---|---|---|---|
| 1.4.7 | Pengembangan Middleware & Adaptor API DCS | — | 2–8 April 2026 |
| 1.6.1 | Pengujian Seluruh Modul Sistem RFID | 2–9 April 2026 | 9–16 April 2026 |
| 1.6.2 | Laporan Hasil Pengujian Sistem (SIT) | 2–8 April 2026 | 9–15 April 2026 |
| 1.6.3 | Laporan UAT & Simulasi Bagasi Nyasar | 10–15 April 2026 | 17–22 April 2026 |
| 1.6.4 | Pelatihan Staf Ground Handling & Check-in | 16–21 April 2026 | 23–28 April 2026 |
| 1.6.5 | Dokumen Laporan Akhir & Serah Terima | 22–24 April 2026 | 29 April–1 Mei 2026 |
| 1.6.6 | Milestone 3: Sistem Siap Operasional | 24 April 2026 | 1 Mei 2026 |

Task 1.1–1.5 tidak terdampak, kecuali penambahan 1.4.7. Instalasi fisik (1.5) tetap selesai lebih awal dan tidak berada di jalur kritis.

**Jalur kritis setelah perubahan:** 1.4.6 → 1.4.7 → 1.6.1/1.6.2 → 1.6.3 → 1.6.4 → 1.6.5 → 1.6.6. Karena 1.6.1 dan 1.6.2 berada di dua cabang kritis paralel, penambahan 5 hari pada 1.4.7 langsung menggeser seluruh fase pengujian dan penutupan.

### 7.3 Dampak terhadap Biaya

| Item | Nilai |
|---|---:|
| Baseline 0 (BAC) | Rp219.678.233 |
| Biaya CR-001 | Rp15.000.000 |
| Baseline 1 (BAC) | **Rp234.678.233** |
| Variance | +Rp15.000.000 (+6,83%) |
| Pagu Charter | Rp285.000.000 |
| Sisa pagu setelah CR | **Rp50.321.767** |
| Contingency reserve proyek | Rp13.500.000 (tidak digunakan untuk CR) |
| Management reserve awal | Rp65.321.767 |
| Management reserve setelah CR | Rp50.321.767 |

Rincian estimasi biaya CR-001:

| Komponen | Volume | Tarif | Total |
|---|---:|---:|---:|
| Analisis dan desain adaptor | 2 hari | Rp3.500.000/hari | Rp7.000.000 |
| Implementasi dan unit test | 2 hari | Rp3.000.000/hari | Rp6.000.000 |
| Integrasi, dokumentasi, dan serah terima | 1 hari | Rp2.000.000/hari | Rp2.000.000 |
| **Total** | **5 hari** | | **Rp15.000.000** |

### 7.4 Dampak terhadap Resource

| Resource | Alokasi | Keterangan |
|---|---|---|
| System Analyst | 2 hari | Desain kontrak antarmuka dan pemetaan data |
| Software Developer | 2 hari | Implementasi adaptor dan unit test |
| QA / Tester | 1 hari | Integration test dan regresi |
| Project Manager | Parsial | Monitoring, CCB, dan pembaruan baseline |
| Hardware/vendor | Tidak ada | Tidak ada pengadaan baru |

Tidak diperlukan penambahan personel tetap. Beban tambahan diserap oleh tim yang sudah ada dengan penjadwalan 5 hari kerja.

### 7.5 Dampak terhadap Kualitas

Pengujian tambahan yang diperlukan:

- 12 skenario integrasi DCS (normal, timeout, duplikasi, retry, data invalid).
- 4 skenario gangguan koneksi dan sinkronisasi ulang.
- 2 skenario performa (respons <3 detik dan throughput puncak).
- Regresi seluruh modul yang terdampak.

Kriteria penerimaan:

- 100% skenario kritis lulus.
- Tidak ada kehilangan atau duplikasi data bagasi.
- Waktu respons dashboard tetap <3 detik.
- Audit log terbentuk untuk setiap transaksi.
- Tidak ada *critical defect* yang terbuka saat UAT.

### 7.6 Dampak terhadap Risiko

| Risiko | Sebelum | Setelah | Respons |
|---|---|---|---|
| Ketidakcocokan protokol DCS | Tinggi | Rendah | Middleware, contract test, simulator |
| Keterlambatan integrasi | Tinggi | Sedang | Jadwal 5 hari, monitoring harian |
| Duplikasi/kehilangan data | Sedang | Rendah | Idempotency, queue, retry, audit log |
| Ketergantungan vendor DCS | Sedang | Rendah | Koordinasi awal dan akses simulator |
| Overrun biaya CR | Rendah | Rendah | Cap Rp15.000.000, laporan biaya mingguan |
| Konflik resource | Sedang | Rendah | Alokasi SA/Developer/QA sejak awal |

### 7.7 Dampak terhadap Pengadaan dan Kontrak

Tidak ada pengadaan hardware baru. Middleware dikembangkan in-house dan menggunakan server lokal yang sudah ada. Tidak diperlukan amendemen kontrak vendor perangkat keras.

### 7.8 Manfaat Perubahan

- FR-10 terpenuhi dan integrasi DCS dapat diuji secara terkontrol.
- Risiko kegagalan SIT/UAT menurun.
- Data bagasi lebih akurat dan dapat diaudit.
- Proyek tetap di bawah pagu Charter.
- Baseline 1 memberikan pembanding yang jelas antara rencana awal dan rencana setelah perubahan.

---

## 8. Opsi yang Dipertimbangkan

| Opsi | Biaya | Durasi | Risiko | Evaluasi |
|---|---:|---:|---|---|
| A. Integrasi langsung tanpa middleware | Rp0 | 0 hari | Tinggi | Ditolak: protokol legacy, tidak ada retry/audit, berpotensi gagal SIT. |
| B. Lisensi middleware vendor | ±Rp25.000.000 | ±10 hari | Rendah | Ditolak: biaya dan lead time lebih besar; ketergantungan vendor. |
| C. Middleware/adaptor in-house | Rp15.000.000 | 5 hari | Sedang | **Dipilih**: biaya terkendali, sesuai kebutuhan, dapat dipelihara tim internal. |
| D. Menunda integrasi setelah go-live | Rp0 | 0 hari | Tinggi | Ditolak: FR-10 tidak terpenuhi saat serah terima. |

Keputusan CCB: **Opsi C**.

---

## 9. Notulen dan Keputusan CCB

### 9.1 Informasi Rapat

| Item | Keterangan |
|---|---|
| Tanggal | 24 Maret 2026 |
| Waktu | 10.00–11.30 WIB |
| Tempat | Ruang Rapat Divisi TI / hybrid |
| Agenda | Review CR-001 — Middleware & Adaptor API DCS |
| Ketua | Ir. H. Max Verstappen (Project Sponsor) |
| Sekretaris | Muhammad Hasbi Assidiqi (Change Administrator) |

### 9.2 Daftar Hadir

| Nama | Jabatan | Peran | Kehadiran |
|---|---|---|---|
| Ir. H. Max Verstappen | Direktur Operasional | Sponsor / Ketua CCB | Hadir |
| Ir. Primary Putri Ardiva | Kepala Divisi TI | Project Manager | Hadir |
| Muhammad Nabiel Lukman Hakim | System Analyst | Pemohon / analis teknis | Hadir |
| Muhammad Hasbi Assidiqi | Network/Hardware Engineer | Change Administrator | Hadir |
| Santosa | Software Developer | Implementasi | Hadir |
| Siska | QA/Tester | Verifikasi | Hadir |
| Rusdi | User Representative | Operasional | Hadir |

Kuorum terpenuhi (7 dari 7 anggota hadir).

### 9.3 Pokok Pembahasan

1. System Analyst memaparkan temuan protokol legacy DCS dan risiko integrasi langsung.
2. Project Manager menyampaikan analisis dampak: +5 hari kerja, +Rp15.000.000, Baseline 1 selesai 1 Mei 2026.
3. QA menyampaikan kebutuhan pengujian tambahan dan kriteria penerimaan.
4. User Representative memastikan perubahan tidak mengganggu jadwal operasional dan pelatihan.
5. Sponsor menegaskan proyek harus tetap di bawah pagu Rp285.000.000 dan tidak boleh mengurangi lingkup.

### 9.4 Keputusan

**CR-001 disetujui dengan syarat** sebagai berikut:

1. Biaya implementasi tidak melebihi Rp15.000.000.
2. Integration test dengan simulator DCS wajib lulus sebelum SIT.
3. Tidak ada perubahan pada sistem DCS inti; perubahan hanya pada sisi LUGGIO.
4. Baseline 1 ditetapkan setelah jadwal diperbarui; Baseline 0 tidak diubah.
5. Laporan status CR disampaikan pada rapat mingguan sampai CR ditutup.
6. Seluruh dokumen (desain, test report, runbook) diserahkan saat closing.

### 9.5 Action Items

| No | Action | PIC | Due date | Status |
|---|---|---|---|---|
| 1 | Perbarui jadwal dan set Baseline 1 | Project Manager | 25 Maret 2026 | Selesai |
| 2 | Finalisasi desain adaptor | System Analyst | 2 April 2026 | Selesai |
| 3 | Implementasi middleware | Software Developer | 6 April 2026 | Selesai |
| 4 | Integration test dengan simulator | Developer/QA | 8 April 2026 | Selesai |
| 5 | SIT dan regresi | QA | 15 April 2026 | Selesai |
| 6 | UAT | QA/User | 22 April 2026 | Selesai |
| 7 | Tutup CR dan serah terima | Project Manager | 1 Mei 2026 | Selesai |

---

## 10. Implementasi dan Verifikasi

### 10.1 Rencana Implementasi

| No | Aktivitas | PIC | Tanggal | Output |
|---|---|---|---|---|
| 1 | Finalisasi desain dan setup environment | System Analyst | 2 April 2026 | Desain adaptor, environment siap |
| 2 | Implementasi adaptor dan unit test | Software Developer | 3–6 April 2026 | Kode, unit test |
| 3 | Integration test dengan simulator DCS | Developer/QA | 7–8 April 2026 | Integration test report |
| 4 | SIT dan regresi | QA | 9–15 April 2026 | SIT report |
| 5 | UAT dan simulasi bagasi nyasar | QA/User | 17–22 April 2026 | UAT sign-off |
| 6 | Pelatihan dan sosialisasi | Trainer/PM | 23–28 April 2026 | Training report |
| 7 | Penutupan CR dan serah terima | Project Manager | 29 April–1 Mei 2026 | CR closed, closing report |

### 10.2 Hasil Verifikasi

| Verifikasi | Hasil | Status |
|---|---|---|
| Unit test middleware | 100% test case lulus | Lulus |
| Integration test DCS simulator | 12/12 skenario lulus | Lulus |
| Pengujian retry/idempotency | Tidak ada duplikasi data | Lulus |
| Performa respons | 1,8 detik (<3 detik) | Lulus |
| SIT | 100% skenario kritis lulus | Lulus |
| UAT | 98,4% test case lulus; 2 defect minor ditutup | Lulus |
| Regresi modul terdampak | Tidak ada regresi kritis | Lulus |

### 10.3 Pembaruan Baseline

| Baseline | Tanggal selesai | Durasi | BAC | Status |
|---|---|---|---|---|
| Baseline 0 | 24 April 2026 | 53 hari | Rp219.678.233 | Tidak diubah |
| Baseline 1 | 1 Mei 2026 | 58 hari | Rp234.678.233 | Ditetapkan 25 Maret 2026 |

Baseline 0 tetap menjadi dasar perbandingan Earned Value. Baseline 1 digunakan untuk menilai kinerja jadwal dan biaya setelah perubahan disetujui.

---

## 11. Change Request Log

| ID | Tanggal | Pemohon | Deskripsi | Kategori | Dampak biaya | Dampak jadwal | Keputusan | Status |
|---|---|---|---|---|---:|---:|---|---|
| CR-001 | 18 Mar 2026 | M. Nabiel L. H. | Middleware & Adaptor API DCS | Teknis/lingkup | +Rp15.000.000 | +5 hari | Disetujui CCB 24 Mar 2026 | Closed 1 Mei 2026 |

Tidak ada change request lain yang diajukan selama proyek.

---

## 12. Dampak terhadap Dokumen Proyek

| Dokumen | Perubahan |
|---|---|
| Project Charter | Tidak berubah; menjadi dasar pagu dan lingkup. |
| WBS / WBS Dictionary | Penambahan 1.4.7 Middleware & Adaptor API DCS. |
| Jadwal (MPP) | Baseline 1 dengan finish 1 Mei 2026. |
| Cost baseline | BAC berubah dari Rp219.678.233 menjadi Rp234.678.233. |
| Risk Register | Penambahan risiko integrasi DCS dan mitigasi middleware. |
| Test Plan | Penambahan 12 skenario integrasi, retry, dan idempotency. |
| Requirements Traceability | FR-10, FR-03, FR-12 diperbarui. |
| Closing Report | Memuat CR-001, dampak, dan hasil verifikasi. |

---

## 13. Lessons Learned dari Perubahan

1. **Validasi antarmuka eksternal sejak perencanaan.** Protokol DCS seharusnya diverifikasi sebelum baseline disetujui.
2. **Middleware perlu menjadi bagian eksplisit dalam WBS** jika sistem eksternal menggunakan teknologi legacy.
3. **CCB efektif mencegah perubahan liar.** Dampak biaya dan jadwal dianalisis sebelum implementasi.
4. **Baseline 0 dan Baseline 1 harus dipisahkan.** Pemisahan ini membuat dampak perubahan terukur dan tidak mengaburkan evaluasi kinerja.
5. **Koordinasi vendor DCS harus dimulai lebih awal** untuk mendapatkan akses simulator dan dokumentasi protokol.
6. **Buffer pengujian perlu dijaga.** CR-001 menghabiskan sebagian buffer jadwal, sehingga fase pengujian menjadi lebih ketat.

---

## 14. Lampiran

### Lampiran A — Form Ringkas CR-001

> Formulir lengkap tersedia di [`06-cr-form.md`](06-cr-form.md) dan log perubahan di [`07-cr-log.md`](07-cr-log.md).

| Field | Isi |
|---|---|
| ID | CR-001 |
| Judul | Pengembangan Middleware & Adaptor API DCS |
| Pemohon | Muhammad Nabiel Lukman Hakim |
| Tanggal | 18 Maret 2026 |
| Deskripsi | Menambahkan layanan middleware untuk menerjemahkan protokol LUGGIO ke DCS legacy, termasuk queue, retry, idempotency, audit log, dan monitoring. |
| Alasan | Memenuhi FR-10, mengurangi risiko SIT/UAT, menjaga akurasi data. |
| Dampak biaya | +Rp15.000.000 |
| Dampak jadwal | +5 hari kerja; finish 1 Mei 2026 |
| Alternatif | Integrasi langsung (ditolak), vendor middleware (ditolak), in-house (dipilih), defer (ditolak). |
| Keputusan | Disetujui dengan syarat, 24 Maret 2026 |
| Status | Closed 1 Mei 2026 |

### Lampiran B — Checklist Implementasi CR

- [x] CR dicatat dalam log.
- [x] Analisis dampak scope, schedule, cost, quality, risk selesai.
- [x] CCB review dan keputusan terdokumentasi.
- [x] Baseline 1 ditetapkan; Baseline 0 tidak diubah.
- [x] Middleware diimplementasikan dan diuji.
- [x] Integration test, SIT, UAT, dan regresi lulus.
- [x] Dokumen teknis dan runbook diserahkan.
- [x] CR ditutup dan dilaporkan dalam closing report.

### Lampiran C — Persetujuan

| Nama | Jabatan | Peran | Tanda tangan | Tanggal |
|---|---|---|---|---|
| Ir. H. Max Verstappen | Direktur Operasional | Project Sponsor |  | 24 Maret 2026 |
| Ir. Primary Putri Ardiva | Kepala Divisi TI | Project Manager |  | 24 Maret 2026 |
| Muhammad Nabiel Lukman Hakim | System Analyst | Pemohon CR |  | 1 Mei 2026 |
| Muhammad Hasbi Assidiqi | Network/Hardware Engineer | Change Administrator |  | 1 Mei 2026 |
| Rusdi | Koordinator Ground Handling & Check-In | User Representative |  | 1 Mei 2026 |

---

*Dokumen ini merupakan bagian dari deliverable CP3 Proyek LUGGIO dan disusun berdasarkan Project Charter v1.0, jadwal MPP, serta data Baseline 0 dan Baseline 1.*
