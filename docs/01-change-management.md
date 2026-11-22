# Laporan Manajemen Perubahan (Change Management)

## Proyek LUGGIO — Sistem Pelacakan Bagasi RFID Bandara Indo-Aero

| Item | Keterangan |
|---|---|
| Nomor Dokumen | LUGGIO-CP3-M9-001 |
| Versi | 1.1 |
| Tanggal | 24 April 2026 |
| Status | Final |
| Proyek | LUGGIO: Sistem Pelacakan Bagasi RFID Bandara Indo-Aero |
| Baseline | Baseline 0 (finish tidak berubah; BAC diperbarui menjadi Rp242.678.233) |
| Penyusun | Muhammad Hasbi Assidiqi — Network/Hardware Engineer |
| Pemeriksa | Muhammad Nabiel Lukman Hakim — System Analyst |
| Persetujuan | Ir. Primary Putri Ardiva — Project Manager |
| Persetujuan | Ir. H. Max Verstappen — Project Sponsor |
| Dokumen terkait | Project Charter v1.0; MPP LUGGIO; Change Request Log; Closing Report |
| Form Change Request | **01/CR/2026** — Pengembangan Middleware API DCS; **02/CR/2026** — Pengembangan Validasi dan Retry RFID (terlampir) |

---

## 1. Ringkasan Eksekutif

Selama tahap perancangan dan pengujian integrasi, tim menemukan dua kesenjangan teknis: (1) *Departure Control System* (DCS) Bandara Indo-Aero masih menggunakan protokol dan format pesan legacy sehingga integrasi langsung dari LUGGIO berisiko gagal pada SIT/UAT, dan (2) pembacaan tag RFID berpotensi gagal karena posisi tag, gangguan sinyal, atau kondisi pembaca, sehingga data perpindahan bagasi dapat salah tercatat.

Kedua temuan diajukan sebagai **01/CR/2026 (Pengembangan Middleware API DCS)** pada 18 Maret 2026 dan **02/CR/2026 (Pengembangan Validasi dan Retry RFID)** pada 21 Maret 2026. *Change Control Board* (CCB) menyetujui keduanya pada **24 Maret 2026** dengan ketentuan **tanggal selesai proyek tetap 24 April 2026**; kedua pekerjaan dikerjakan paralel dengan fase pengujian 1.6. Ringkasan dampak:

| Item | Baseline 0 | 01/CR/2026 | 02/CR/2026 | Total CR | BAC Akhir |
|---|---:|---:|---:|---:|---:|
| Tanggal selesai | 24 April 2026 | Paralel | Paralel | 0 hari | **24 April 2026** |
| Durasi | 53 hari | +5 hari (dalam float) | +3 hari (dalam float) | +8 hari kerja | **53 hari** |
| Biaya (BAC) | Rp219.678.233 | +Rp15.000.000 | +Rp8.000.000 | +Rp23.000.000 | **Rp242.678.233** |

Kedua CR tidak mengurangi lingkup, tidak mengubah pagu Charter Rp285.000.000, dan dibiayai dari *management reserve* (sisa pagu setelah CR: Rp42.321.767). Karena tanggal selesai tidak bergeser, **Baseline 0 tetap berlaku** dan tidak perlu ditetapkan baseline baru; yang berubah hanya nilai biaya (BAC) dan **dua** *work package* baru di WBS 1.4 (1.4.7 dan 1.4.8). Kedua CR ditutup pada 24 April 2026 bersama penutupan proyek.

## 2. Latar Belakang

Proyek LUGGIO bertujuan menggantikan pemindaian barcode konvensional dengan RFID untuk mengurangi *unreadable rate* dari 8% menjadi di bawah 0,5%. Salah satu kebutuhan fungsional utama adalah **FR-10: integrasi dengan departure control system bandara untuk verifikasi data bagasi**.

Pada Project Charter v1.0, integrasi DCS tercantum sebagai bagian dari lingkup proyek, tetapi belum dirinci sebagai pekerjaan tersendiri di WBS. Saat spesifikasi integrasi disusun (WBS 1.2.3), tim menemukan bahwa:

1. DCS tidak menyediakan endpoint REST/JSON modern; komunikasi menggunakan protokol legacy.
2. Format pesan, kode penerbangan, dan struktur bagasi berbeda dari model data internal LUGGIO.
3. Diperlukan mekanisme antrean, *retry*, *idempotency*, dan *audit log* agar tidak terjadi duplikasi atau kehilangan data saat koneksi terputus.
4. Pengujian langsung tanpa lapisan adaptor berpotensi menggagalkan SIT dan UAT.

Temuan ini memenuhi kriteria perubahan karena memengaruhi **lingkup teknis, jadwal, biaya, dan risiko integrasi**. Sesuai prosedur manajemen perubahan, tim mengajukan 02/CR/2026 kepada CCB sebelum pekerjaan tambahan dilaksanakan.

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
| System Analyst | Muhammad Nabiel Lukman Hakim | Menganalisis dampak teknis dan kebutuhan integrasi; pemohon 02/CR/2026. |
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

Tanggal selesai Baseline 0 tidak diubah. Setelah CR disetujui, nilai biaya (BAC) dan WBS diperbarui di dalam baseline yang sama, lalu *cost baseline* baru dipakai sebagai acuan *Earned Value*. Seluruh dokumen perubahan diarsipkan bersama laporan penutupan proyek.

---

## 6. Change Request yang Diajukan

Terdapat dua CR yang diajukan dan disetujui selama proyek. Keduanya berjenis **Corrective Action** karena lahir dari temuan pada tahap perancangan/pengujian integrasi.

### 6.1 Identitas CR

| Field | 01/CR/2026 | 02/CR/2026 |
|---|---|---|
| ID Request | **CR-001/LUGGIO/2026** | **CR-002/LUGGIO/2026** |
| Nama Pengajuan | Pengembangan Middleware API DCS | Pengembangan Validasi dan Retry RFID |
| Tanggal pengajuan | 18 Maret 2026 | 21 Maret 2026 |
| Pemohon | Muhammad Nabiel Lukman Hakim — System Analyst | Muhammad Nabiel Lukman Hakim — System Analyst |
| Tipe CR | Corrective Action (Scope, Schedule, Cost) | Corrective Action (Scope, Schedule, Cost) |
| Prioritas | High | Medium |
| WBS | 1.4.7 (baru) | 1.4.8 (baru) |
| Requirement terkait | FR-10, FR-03, FR-12 | FR-03, FR-12 (akurasi pembacaan) |
| Biaya | +Rp15.000.000 | +Rp8.000.000 |
| Durasi | +5 hari kerja (paralel, dalam *float*) | +3 hari kerja (paralel, dalam *float*) |
| Keputusan CCB | Disetujui, 24 Maret 2026 | Disetujui, 24 Maret 2026 |
| Status | Closed 24 April 2026 | Closed 24 April 2026 |

### 6.2 Deskripsi Perubahan 01/CR/2026 — Middleware API DCS

Menambahkan **Pengembangan Middleware API DCS** sebagai pekerjaan baru **WBS 1.4.7**, setelah 1.4.6 (Fitur Ekspor Laporan Statistik, Log, dan Backup). Middleware berfungsi untuk:

1. Menerjemahkan pesan internal LUGGIO (REST/JSON) ke format legacy DCS dan sebaliknya.
2. Menangani antrean pesan, *retry*, dan *idempotency* agar data bagasi tidak duplikat.
3. Mencatat audit log setiap transaksi integrasi.
4. Menyediakan monitoring koneksi dan alert jika DCS tidak merespons.
5. Menyediakan mekanisme *fallback* dan sinkronisasi ulang setelah gangguan koneksi.

### 6.3 Deskripsi Perubahan 02/CR/2026 — Validasi dan Retry RFID

Menambahkan **Pengembangan Validasi dan Retry RFID** sebagai pekerjaan baru **WBS 1.4.8**, dikerjakan paralel dengan 1.4.7. Fitur berfungsi untuk:

1. Memvalidasi pembacaan tag (format EPC, duplikasi dalam jendela waktu singkat, dan kondisi tepi pembaca).
2. Melakukan *retry* otomatis dengan jumlah percobaan dan jeda yang dapat dikonfigurasi saat pembacaan gagal.
3. Mencatat kejadian gagal baca ke log untuk analisis kualitas pembaca dan penempatan tag.
4. Menyediakan ringkasan *read success rate* per gerbang untuk evaluasi UAT.

### 6.4 Justifikasi Bisnis

- **01/CR/2026:** memenuhi FR-10 tanpa mengubah sistem DCS milik bandara, mengurangi risiko kegagalan SIT/UAT akibat perbedaan protokol, dan menyediakan jejak audit transaksi integrasi.
- **02/CR/2026:** menurunkan *unreadable rate* di lapangan, mencegah pencatatan perpindahan bagasi yang hilang/duplikat, dan memperkuat bukti uji pada UAT simulasi bagasi nyasar.
- Keduanya menjaga lingkup Charter, jadwal selesai 24 April 2026, dan total biaya di bawah pagu Rp285.000.000.

### 6.5 Lingkup yang Berubah

| Aspek | Sebelum CR | Setelah 01/CR/2026 | Setelah 02/CR/2026 |
|---|---|---|---|
| Integrasi DCS | Diasumsikan langsung dari backend | Melalui middleware/adaptor khusus | Tidak berubah |
| Pembacaan RFID | Satu kali baca, tanpa validasi | Tidak berubah | Validasi + retry otomatis |
| WBS | Tanpa task tambahan | Task 1.4.7, 5 hari | Task 1.4.8, 3 hari |
| Pengujian | SIT/UAT tanpa skenario middleware & retry | +12 skenario integrasi, idempotency | +6 skenario gagal baca, retry, read rate |
| Dokumen | Spesifikasi integrasi saja | Desain adaptor, runbook, integration test report | Aturan validasi, konfigurasi retry, laporan read rate |
| Hardware / lingkup bisnis | — | Tidak berubah | Tidak berubah |

---

## 7. Analisis Dampak

### 7.1 Dampak terhadap Lingkup

Kedua CR menambah *deliverable* teknis (middleware/adaptor dan modul validasi/retry RFID) serta memperluas pengujian. Tidak ada *deliverable* yang dihapus atau dikurangi, dan seluruh FR dalam Charter tetap berlaku.

### 7.2 Dampak terhadap Jadwal

| Item | Baseline 0 | Setelah 01/CR/2026 | Setelah 02/CR/2026 |
|---|---|---|---|
| Tanggal mulai | 9 Februari 2026 | 9 Februari 2026 | 9 Februari 2026 |
| Tanggal selesai | 24 April 2026 | 24 April 2026 | **24 April 2026** |
| Durasi proyek | 53 hari | 53 hari | **53 hari** |
| Milestone 3 | 24 April 2026 | 24 April 2026 | **24 April 2026** |
| Tambahan usaha | — | +5 hari kerja (1.4.7) | +3 hari kerja (1.4.8) |

Task tambahan dan penempatan paralelnya:

| WBS | Task | Periode | Catatan |
|---|---|---|---|
| 1.4.7 | Pengembangan Middleware API DCS | 2–8 April 2026 | Paralel; *float* 1.4 terserap |
| 1.4.8 | Pengembangan Validasi dan Retry RFID | 2–6 April 2026 | Paralel dengan 1.4.7 |
| 1.6.1 | Pengujian Seluruh Modul Sistem RFID | 2–9 April 2026 | Tetap sesuai Baseline 0 |
| 1.6.2 | Laporan Hasil Pengujian Sistem (SIT) | 2–8 April 2026 | Tetap sesuai Baseline 0 |
| 1.6.3 | Laporan UAT & Simulasi Bagasi Nyasar | 10–15 April 2026 | Tetap sesuai Baseline 0 |
| 1.6.4 | Pelatihan Staf Ground Handling & Check-in | 16–21 April 2026 | Tetap sesuai Baseline 0 |
| 1.6.5 | Dokumen Laporan Akhir & Serah Terima | 22–24 April 2026 | Tetap sesuai Baseline 0 |
| 1.6.6 | Milestone 3: Sistem Siap Operasional | 24 April 2026 | Tidak bergeser |

Kedua task dikerjakan oleh tim yang sama secara paralel sehingga tidak menambah lintasan kritis baru. Risikonya adalah beban kerja berlebih pada 2–9 April, sehingga CCB mensyaratkan monitoring harian dan kesiapan *fast-tracking*.

### 7.3 Dampak terhadap Biaya

| Item | Nilai |
|---|---:|
| BAC Baseline 0 | Rp219.678.233 |
| Biaya 01/CR/2026 | +Rp15.000.000 |
| Biaya 02/CR/2026 | +Rp8.000.000 |
| **BAC setelah kedua CR** | **Rp242.678.233** |
| Variance | +Rp23.000.000 (+10,47%) |
| Pagu Charter | Rp285.000.000 |
| Sisa pagu setelah CR | **Rp42.321.767** |
| Contingency reserve proyek | Rp13.500.000 (tidak digunakan untuk CR) |
| Management reserve awal | Rp65.321.767 |
| Management reserve setelah CR | Rp42.321.767 |

Rincian estimasi biaya:

| CR | Komponen | Volume | Tarif | Total |
|---|---|---:|---:|---:|
| 01/CR/2026 | Analisis dan desain adaptor | 2 hari | Rp3.500.000/hari | Rp7.000.000 |
| 01/CR/2026 | Implementasi dan unit test | 2 hari | Rp3.000.000/hari | Rp6.000.000 |
| 01/CR/2026 | Integrasi, dokumentasi, serah terima | 1 hari | Rp2.000.000/hari | Rp2.000.000 |
| | **Subtotal 01/CR/2026** | **5 hari** | | **Rp15.000.000** |
| 02/CR/2026 | Analisis aturan validasi dan desain retry | 1 hari | Rp3.000.000/hari | Rp3.000.000 |
| 02/CR/2026 | Implementasi dan unit test | 1 hari | Rp3.000.000/hari | Rp3.000.000 |
| 02/CR/2026 | Integration test dan tuning pembaca RFID | 1 hari | Rp2.000.000/hari | Rp2.000.000 |
| | **Subtotal 02/CR/2026** | **3 hari** | | **Rp8.000.000** |
| | **Total kedua CR** | **8 hari** | | **Rp23.000.000** |

### 7.4 Dampak terhadap Resource

| Resource | Alokasi | Keterangan |
|---|---|---|
| System Analyst | 3 hari | Desain kontrak antarmuka (CR-001) dan aturan validasi (CR-002) |
| Software Developer | 3 hari | Implementasi adaptor dan modul retry |
| QA / Tester | 2 hari | Integration test, simulasi gagal baca, regresi |
| Network/Hardware Engineer | Parsial | Pengujian pembaca RFID dan tuning antena |
| Project Manager | Parsial | Monitoring, CCB, pembaruan BAC |
| Hardware/vendor | Tidak ada | Tidak ada pengadaan baru |

Tidak diperlukan penambahan personel tetap; beban diserap tim yang ada dengan penjadwalan paralel 2–9 April.

### 7.5 Dampak terhadap Kualitas

Pengujian tambahan:

- 12 skenario integrasi DCS (normal, timeout, duplikasi, retry, data tidak valid) — 01/CR/2026.
- 4 skenario gangguan koneksi dan sinkronisasi ulang — 01/CR/2026.
- 6 skenario pembacaan RFID gagal (posisi tag, interferensi, pembaca sibuk) dan retry — 02/CR/2026.
- 2 skenario performa (respons <3 detik dan throughput puncak).

Kriteria penerimaan:

- 100% skenario kritis lulus; tidak ada *critical defect* terbuka saat UAT.
- Tidak ada kehilangan atau duplikasi data bagasi.
- *Read success rate* di gerbang uji minimal 99,5%.
- Waktu respons dashboard tetap <3 detik.

### 7.6 Dampak terhadap Risiko

| Risiko | Sebelum | Setelah | Respons |
|---|---|---|---|
| Ketidakcocokan protokol DCS | Tinggi | Rendah | Middleware, contract test, simulator |
| Pembacaan RFID gagal / data hilang | Sedang | Rendah | Validasi, retry, log gagal baca |
| Jadwal uji terdampak | Sedang | Sedang | Kerja paralel, monitoring harian, fast-tracking |
| Beban kerja tim berlebih (2–9 April) | Sedang | Sedang | Prioritas tugas, lembur terjadwal |
| Duplikasi data bagasi | Sedang | Rendah | Idempotency, queue, validasi |
| Overrun biaya CR | Rendah | Rendah | Cap Rp15.000.000 dan Rp8.000.000, laporan biaya mingguan |

### 7.7 Dampak terhadap Pengadaan dan Kontrak

Tidak ada pengadaan hardware baru; kedua pekerjaan dikembangkan in-house menggunakan server dan pembaca RFID yang sudah ada. Tidak diperlukan amendemen kontrak vendor.

### 7.8 Manfaat Perubahan

- FR-10 terpenuhi dan integrasi DCS dapat diuji secara terkontrol.
- Keandalan pembacaan RFID meningkat sehingga akurasi data perpindahan bagasi lebih baik.
- Risiko kegagalan SIT/UAT menurun tanpa menggeser tanggal selesai proyek.
- Proyek tetap di bawah pagu Charter (Rp242.678.233 dari Rp285.000.000).

---

## 8. Opsi yang Dipertimbangkan

| Opsi | Biaya | Durasi | Risiko | Evaluasi |
|---|---:|---:|---|---|
| A. Integrasi langsung tanpa middleware | Rp0 | 0 hari | Tinggi | Ditolak: protokol legacy, tidak ada retry/audit, berpotensi gagal SIT. |
| B. Lisensi middleware vendor | ±Rp25.000.000 | ±10 hari | Rendah | Ditolak: biaya dan lead time lebih besar; ketergantungan vendor. |
| C. Middleware/adaptor in-house | Rp15.000.000 | 5 hari | Sedang | **Dipilih**: biaya terkendali, sesuai kebutuhan, dapat dipelihara tim internal. |
| D. Menunda integrasi setelah go-live | Rp0 | 0 hari | Tinggi | Ditolak: FR-10 tidak terpenuhi saat serah terima. |

Keputusan CCB: **Opsi C**. Untuk 02/CR/2026, opsi yang dievaluasi adalah: (A) tanpa retry — ditolak karena data bagasi tetap berisiko hilang; (B) retry penuh di pembaca RFID (firmware) — ditolak karena ketergantungan vendor perangkat; (C) **validasi + retry di aplikasi LUGGIO — dipilih** (Rp8.000.000, 3 hari, dapat dikonfigurasi tanpa menyentuh firmware).

---

## 9. Notulen dan Keputusan CCB

### 9.1 Informasi Rapat

| Item | Keterangan |
|---|---|
| Tanggal | 24 Maret 2026 |
| Waktu | 10.00–11.30 WIB |
| Tempat | Ruang Rapat Divisi TI / hybrid |
| Agenda | Review 01/CR/2026 — Middleware API DCS; Review 02/CR/2026 — Validasi dan Retry RFID |
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

1. System Analyst memaparkan temuan protokol legacy DCS (pengajuan 18 Maret 2026) dan hasil pengujian pembaca RFID berupa risiko gagal baca (pengajuan 21 Maret 2026).
2. Project Manager menyampaikan analisis dampak kedua CR: +8 hari kerja yang dikerjakan paralel sehingga **tanggal selesai tetap 24 April 2026**, dengan tambahan biaya Rp23.000.000.
3. QA menyampaikan kebutuhan pengujian tambahan (integrasi DCS dan simulasi gagal baca RFID) serta kriteria penerimaan.
4. User Representative memastikan pekerjaan paralel tidak mengganggu jadwal operasional dan pelatihan.
5. Sponsor menegaskan proyek harus tetap di bawah pagu Rp285.000.000, tidak boleh mengurangi lingkup, dan tanggal selesai tidak boleh melewati 24 April 2026.

### 9.4 Keputusan

**01/CR/2026 dan 02/CR/2026 disetujui dengan syarat** sebagai berikut:

1. Biaya tidak melebihi Rp15.000.000 (01/CR/2026) dan Rp8.000.000 (02/CR/2026).
2. Kedua pekerjaan dikerjakan paralel sehingga **tanggal selesai proyek tetap 24 April 2026**; jika ada indikasi keterlambatan, PM wajib melakukan *fast-tracking*.
3. Integration test dengan simulator DCS wajib lulus sebelum SIT; skenario gagal baca RFID diuji sebelum UAT.
4. Tidak ada perubahan pada sistem DCS inti maupun firmware pembaca RFID; perubahan hanya pada sisi LUGGIO.
5. BAC diperbarui menjadi Rp242.678.233 (Baseline 0, tanggal tidak berubah); Baseline 0 tidak diganti.
6. Laporan status CR disampaikan pada rapat mingguan sampai CR ditutup.
7. Seluruh dokumen (desain, test report, runbook) diserahkan saat closing.

### 9.5 Action Items

| No | Action | PIC | Due date | Status |
|---|---|---|---|---|
| 1 | Perbarui BAC dan jadwal 1.4.7/1.4.8 (finish tetap 24 April) | Project Manager | 25 Maret 2026 | Selesai |
| 2 | Finalisasi desain adaptor dan aturan validasi RFID | System Analyst | 2 April 2026 | Selesai |
| 3 | Implementasi middleware dan modul retry | Software Developer | 6 April 2026 | Selesai |
| 4 | Integration test (simulator DCS + gagal baca RFID) | Developer/QA | 8 April 2026 | Selesai |
| 5 | SIT dan regresi | QA | 9–15 April 2026 | Selesai |
| 6 | UAT | QA/User | 10–15 April 2026 | Selesai |
| 7 | Tutup kedua CR dan serah terima | Project Manager | 24 April 2026 | Selesai |

---

## 10. Implementasi dan Verifikasi

### 10.1 Rencana Implementasi

| No | Aktivitas | PIC | Tanggal | Output |
|---|---|---|---|---|
| 1 | Finalisasi desain adaptor dan aturan validasi/retry | System Analyst | 2 April 2026 | Desain adaptor & aturan validasi |
| 2 | Implementasi middleware dan modul retry | Software Developer | 3–6 April 2026 | Kode, unit test |
| 3 | Integration test (simulator DCS, gagal baca RFID) | Developer/QA | 7–8 April 2026 | Integration test report |
| 4 | SIT dan regresi | QA | 9–15 April 2026 | SIT report |
| 5 | UAT dan simulasi bagasi nyasar | QA/User | 10–15 April 2026 | UAT sign-off |
| 6 | Pelatihan dan sosialisasi | Trainer/PM | 16–21 April 2026 | Training report |
| 7 | Penutupan CR dan serah terima | Project Manager | 22–24 April 2026 | CR closed, closing report |

### 10.2 Hasil Verifikasi

| Verifikasi | Hasil | Status |
|---|---|---|
| Unit test middleware dan modul retry | 100% test case lulus | Lulus |
| Integration test DCS simulator | 12/12 skenario lulus | Lulus |
| Pengujian retry/idempotency | Tidak ada duplikasi data | Lulus |
| Simulasi gagal baca RFID | 6/6 skenario lulus; *read success rate* 99,7% | Lulus |
| Performa respons | 1,8 detik (<3 detik) | Lulus |
| SIT | 100% skenario kritis lulus | Lulus |
| UAT | 98,4% test case lulus; 2 defect minor ditutup | Lulus |
| Regresi modul terdampak | Tidak ada regresi kritis | Lulus |
| Tanggal selesai proyek | 24 April 2026 (sesuai Baseline 0) | Sesuai |

### 10.3 Pembaruan Baseline

| Baseline | Tanggal selesai | Durasi | BAC | Status |
|---|---|---|---|---|
| Baseline 0 (awal) | 24 April 2026 | 53 hari | Rp219.678.233 | Tidak diubah tanggalnya |
| Baseline 0 setelah CR (biaya) | 24 April 2026 | 53 hari | **Rp242.678.233** | BAC diperbarui 25 Maret 2026 |

Karena tanggal selesai tidak bergeser, **tidak ada Baseline 1**: yang diperbarui hanya nilai biaya (BAC) dan penambahan WBS 1.4.7–1.4.8. Baseline 0 tetap menjadi dasar tunggal perbandingan *Earned Value*.

---

## 11. Change Request Log

| ID CR | Tanggal | Pengaju | Nama Pengajuan | Tipe CR | Prioritas | Dampak biaya | Dampak jadwal | Status | Keputusan |
|---|---|---|---|---|---|---:|---|---|---|
| 01/CR/2026 | 18/03/2026 | M. Nabiel L. H. | Pengembangan Middleware API DCS (WBS 1.4.7) | Corrective Action | High | +Rp15.000.000 | Paralel (0 hari) | Approved | 24/03/2026 |
| 02/CR/2026 | 21/03/2026 | M. Nabiel L. H. | Pengembangan Validasi dan Retry RFID (WBS 1.4.8) | Corrective Action | Medium | +Rp8.000.000 | Paralel (0 hari) | Approved | 24/03/2026 |
| **Total** | | | **2 CR** | | | **+Rp23.000.000** | **0 hari** | **2 disetujui** | |

Log lengkap tersedia di [`07-cr-log.md`](07-cr-log.md).

---

## 12. Dampak terhadap Dokumen Proyek

| Dokumen | Perubahan |
|---|---|
| Project Charter | Tidak berubah; menjadi dasar pagu dan lingkup. |
| WBS / WBS Dictionary | Penambahan 1.4.7 Middleware API DCS dan 1.4.8 Validasi dan Retry RFID. |
| Jadwal (MPP) | Finish tetap 24 April 2026; task 1.4.7–1.4.8 dijadwalkan paralel. |
| Cost baseline | BAC berubah dari Rp219.678.233 menjadi Rp242.678.233. |
| Risk Register | Penambahan risiko integrasi DCS serta gagal baca RFID dan mitigasinya. |
| Test Plan | Penambahan 12 skenario integrasi/idempotency dan 6 skenario gagal baca RFID. |
| Requirements Traceability | FR-10, FR-03, FR-12 diperbarui. |
| Closing Report | Memuat 01/CR/2026 dan 02/CR/2026, dampak, dan hasil verifikasi. |

---

## 13. Lessons Learned dari Perubahan

1. **Validasi antarmuka eksternal sejak perencanaan.** Protokol DCS seharusnya diverifikasi sebelum baseline disetujui.
2. **Middleware perlu menjadi bagian eksplisit dalam WBS** jika sistem eksternal menggunakan teknologi legacy.
3. **CCB efektif mencegah perubahan liar.** Dampak biaya dan jadwal dianalisis sebelum implementasi.
4. **Perubahan dapat diserap tanpa menggeser jadwal** jika dikerjakan paralel di dalam *float*; dampaknya tetap tercatat sebagai tambahan biaya pada BAC.
5. **Koordinasi vendor DCS harus dimulai lebih awal** untuk mendapatkan akses simulator dan dokumentasi protokol.
6. **Pengujian pembaca RFID di lapangan harus dilakukan sebelum baseline disetujui** agar kebutuhan retry tidak muncul di tengah pelaksanaan.

---

## 14. Lampiran

### Lampiran A — Form Ringkas 01/CR/2026 dan 02/CR/2026

> Formulir lengkap: [`06-cr-form.md`](06-cr-form.md) (01/CR/2026) dan [`06b-cr-form-002.md`](06b-cr-form-002.md) (02/CR/2026). Log perubahan: [`07-cr-log.md`](07-cr-log.md).

| Field | 01/CR/2026 | 02/CR/2026 |
|---|---|---|
| ID Request | CR-001/LUGGIO/2026 | CR-002/LUGGIO/2026 |
| Nama Pengajuan | Pengembangan Middleware API DCS | Pengembangan Validasi dan Retry RFID |
| Pemohon | Muhammad Nabiel Lukman Hakim — System Analyst | Muhammad Nabiel Lukman Hakim — System Analyst |
| Tanggal | 18/03/2026 | 21/03/2026 |
| Tipe / Prioritas | Corrective Action / High | Corrective Action / Medium |
| WBS | 1.4.7 (baru) | 1.4.8 (baru) |
| Dampak biaya | +Rp15.000.000 | +Rp8.000.000 |
| Dampak jadwal | Paralel; finish tetap 24 April 2026 | Paralel; finish tetap 24 April 2026 |
| Keputusan | Disetujui, 24/03/2026 | Disetujui, 24/03/2026 |
| Status | Closed 24 April 2026 | Closed 24 April 2026 |

### Lampiran B — Checklist Implementasi CR

- [x] CR dicatat dalam log.
- [x] Analisis dampak scope, schedule, cost, quality, risk selesai.
- [x] CCB review dan keputusan terdokumentasi.
- [x] BAC diperbarui; tanggal selesai tetap 24 April 2026.
- [x] Middleware serta modul validasi/retry RFID diimplementasikan dan diuji.
- [x] Integration test, SIT, UAT, dan regresi lulus.
- [x] Dokumen teknis dan runbook diserahkan.
- [x] CR ditutup dan dilaporkan dalam closing report.

### Lampiran C — Persetujuan

| Nama | Jabatan | Peran | Tanda tangan | Tanggal |
|---|---|---|---|---|
| Ir. H. Max Verstappen | Direktur Operasional | Project Sponsor |  | 24 Maret 2026 |
| Ir. Primary Putri Ardiva | Kepala Divisi TI | Project Manager |  | 24 Maret 2026 |
| Muhammad Nabiel Lukman Hakim | System Analyst | Pemohon CR |  | 24 April 2026 |
| Muhammad Hasbi Assidiqi | Network/Hardware Engineer | Change Administrator |  | 24 April 2026 |
| Rusdi | Koordinator Ground Handling & Check-In | User Representative |  | 24 April 2026 |

---

*Dokumen ini merupakan bagian dari deliverable CP3 Proyek LUGGIO dan disusun berdasarkan Project Charter v1.0, jadwal MPP, serta data Baseline 0 yang diperbarui biayanya.*
