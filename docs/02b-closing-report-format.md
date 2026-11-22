# CLOSING REPORT

## Laporan Penutupan Proyek

| | |
|---|---|
| **Nama Proyek** | LUGGIO: Sistem Pelacakan Bagasi RFID Bandara Indo-Aero |
| **Klien / Sponsor** | Ir. H. Max Verstappen — Direktur Operasional, Bandara Indo-Aero |
| **Project Manager** | Ir. Primary Putri Ardiva |
| **Tanggal Mulai** | 9 Februari 2026 |
| **Tanggal Selesai** | 24 April 2026 |
| **Versi Dokumen** | 1.0 |

*Dokumen ini bersifat resmi dan merupakan bagian dari penutupan proyek.*

---

## 1. PROJECT OBJECTIVES

### 1.1 Tujuan Proyek

Proyek LUGGIO bertujuan menggantikan pemindaian barcode konvensional pada penanganan bagasi di Bandara Indo-Aero dengan sistem pelacakan bagasi berbasis **RFID** (*Radio Frequency Identification*), sehingga setiap perpindahan bagasi — mulai dari *check-in counter*, *baggage handling system*, hingga *carousel* pengambilan — dapat tercatat secara otomatis dan *real-time*. Tujuan ini dicapai dengan menyediakan 6 unit RFID *reader gate*, 5 unit *handheld scanner*, 5.000 *smart tag*, server lokal, dashboard pemantauan berbasis web, dan integrasi dengan *Departure Control System* (DCS) bandara. Manfaat yang diharapkan adalah penurunan *unreadable rate* dari 8% menjadi di bawah 0,5%, peningkatan akurasi pencatatan bagasi nyasar, percepatan proses *check-in*, dan penyediaan data operasional yang dapat diaudit bagi Divisi TI serta unit *Ground Handling* dan *Check-In* Bandara Indo-Aero.

### 1.2 Kriteria Keberhasilan Utama (Main Project Success Criteria)

| No | Kriteria Keberhasilan | Target | Status Pencapaian |
|---|---|---|---|
| 1 | *Unreadable rate* pembacaan bagasi | < 0,5% | Tercapai (0,42% pada pilot) |
| 2 | Waktu respons dashboard pemantauan | < 3 detik | Tercapai (1,8 detik) |
| 3 | Instalasi perangkat RFID | 6 *gate* + 5 *handheld* aktif | Tercapai (selesai 16 Maret 2026) |
| 4 | Integrasi dengan DCS bandara (FR-10) | Berjalan dan lulus SIT/UAT | Tercapai (melalui 01/CR/2026 Middleware API DCS) |
| 5 | Kesiapan sumber daya manusia | 50 personel lulus pelatihan | Tercapai (50 personel lulus 21 April 2026) |
| 6 | Jadwal penyelesaian proyek | 24 April 2026 | Tercapai (selesai 24 April 2026) |
| 7 | Anggaran proyek | ≤ Rp285.000.000 | Tercapai (Rp242.678.233) |
| 8 | Kualitas perangkat lunak | 100% skenario kritis lulus; 0 *critical defect* | Tercapai (SIT 100%, UAT 98,4%, 0 *critical defect*) |

### 1.3 Key Performance Indicators (KPI)

| KPI ID | Aspek | KPI | Target | Realisasi | Status |
|---|---|---|---|---|---|
| KPI-01 | Kualitas | *Unreadable rate* pembacaan bagasi | < 0,5% | 0,42% | Tercapai |
| KPI-02 | Kinerja sistem | Waktu respons dashboard | < 3 detik | 1,8 detik | Tercapai |
| KPI-03 | Jadwal | Instalasi 6 *gate* + 5 *handheld* | Sebelum 10 April 2026 | Selesai 16 Maret 2026 | Tercapai |
| KPI-04 | Sumber daya | Pelatihan 50 personel | Selesai 18 April 2026 | 50 personel selesai 21 April 2026 | Tercapai (terlambat 3 hari) |
| KPI-05 | Biaya | Total biaya proyek | ≤ Rp285.000.000 | Rp242.678.233 | Tercapai |
| KPI-06 | Ketersediaan | Ketersediaan sistem pada masa pilot | ≥ 99% | 99,5% | Tercapai |

### 1.4 Analisis Kriteria Keberhasilan Utama (Main Project Success Criteria)

Seluruh kriteria keberhasilan utama **tercapai**. Tidak ada kriteria yang gagal dipenuhi.

| No | Kriteria Keberhasilan | Keterangan |
|---|---|---|
| 1 | — | Tidak ada kriteria keberhasilan utama yang tidak tercapai. |

### 1.5 Analisis Key Performance Indicators (KPI)

Seluruh KPI tercapai. KPI-04 tercatat **terlambat 3 hari** dari target tanggal 18 April 2026 karena pelatihan baru dilaksanakan 16–21 April 2026 setelah modul validasi dan *retry* RFID (02/CR/2026) selesai diuji, namun tetap terpenuhi sebelum tanggal penutupan proyek 24 April 2026.

| KPI ID | Aspek | KPI | Keterangan |
|---|---|---|---|
| KPI-04 | Sumber daya | Pelatihan 50 personel | Realisasi 21 April 2026 (target 18 April 2026). Pelatihan menunggu penyelesaian pengujian 1.4.7 dan 1.4.8; seluruh 50 personel lulus sebelum penutupan. |

---

## 2. SUMMARY OF PROJECT RESULTS

### 2.1 Deskripsi Hasil Proyek

Proyek LUGGIO menghasilkan dan menyerahkan sistem pelacakan bagasi RFID yang beroperasi penuh di Bandara Indo-Aero, meliputi:

1. **Perangkat keras:** 6 unit RFID *Reader Gate*, 5 unit *handheld scanner*, 5.000 *smart tag*, printer RFID, server lokal, 2 *access point outdoor*, *switch* POE, UPS, dan kabel Cat6 — seluruhnya terpasang dan aktif.
2. **Perangkat lunak:** *backend*, basis data, dashboard web *real-time*, RBAC, sistem *alert*, modul laporan statistik, log dan *backup*, sinkronisasi *offline*, serta modul validasi dan *retry* pembacaan RFID.
3. **Integrasi:** *Middleware API DCS* sebagai penghubung LUGGIO dengan *Departure Control System* bandara, dan integrasi display *carousel*.
4. **Dokumentasi:** spesifikasi integrasi, desain adaptor, *runbook* integrasi dan *backup*, laporan SIT, UAT, dan *integration test*, buku panduan operasional, *admin guide*, serta *asset list*.

### 2.2 Keberhasilan Proyek

Proyek LUGGIO dinyatakan **BERHASIL**. Seluruh *deliverable* lingkup Charter diserahkan dan diterima, seluruh kriteria keberhasilan utama dan KPI terpenuhi sebelum penutupan, *unreadable rate* turun dari 8% menjadi 0,42%, integrasi DCS berjalan, proyek selesai tepat pada tanggal rencana 24 April 2026 (SPI akhir 1,00) dan berada di bawah pagu anggaran dengan CPI 1,00 serta VAC Rp0.

---

## 3. IDENTITAS DAN RINGKASAN PROYEK

### 3.1 Informasi Proyek

| | |
|---|---|
| **Nama Proyek** | LUGGIO: Sistem Pelacakan Bagasi RFID Bandara Indo-Aero |
| **Klien / Sponsor** | Ir. H. Max Verstappen — Direktur Operasional, Bandara Indo-Aero |
| **Project Manager** | Ir. Primary Putri Ardiva |
| **Tanggal Mulai (Rencana)** | 9 Februari 2026 |
| **Tanggal Mulai (Realisasi)** | 9 Februari 2026 |
| **Tanggal Selesai (Rencana)** | 24 April 2026 |
| **Tanggal Selesai (Realisasi)** | 24 April 2026 |

### 3.2 Anggota Tim

| Nama | Peran |
|---|---|
| Ir. Primary Putri Ardiva | Project Manager |
| Ir. H. Max Verstappen | Project Sponsor |
| Muhammad Hasbi Assidiqi | Network/Hardware Engineer — Change Administrator |
| Muhammad Nabiel Lukman Hakim | System Analyst |
| Santosa | Software Developer |
| Siska | QA / Tester |
| Rusdi | User Representative — Koordinator *Ground Handling & Check-In* |
| Tim *Ground Handling* Bandara Indo-Aero | Pengguna dan peserta pelatihan (50 personel) |

### 3.3 Ringkasan Eksekutif

Proyek LUGGIO mengimplementasikan sistem pelacakan bagasi berbasis RFID untuk Bandara Indo-Aero guna menggantikan pemindaian barcode konvensional. Proyek dilaksanakan dalam 53 hari kerja (9 Februari–24 April 2026) dengan anggaran awal Rp219.678.233 dan pagu Charter Rp285.000.000. Teknologi yang digunakan meliputi RFID *reader gate* dan *handheld scanner*, 5.000 *smart tag*, server lokal, aplikasi *backend* dengan basis data relasional, dashboard web *real-time*, serta *Middleware API* untuk integrasi dengan DCS. Selama pelaksanaan, dua *change request* — 01/CR/2026 (Middleware API DCS) dan 02/CR/2026 (Validasi dan Retry RFID) — disetujui CCB pada 24 Maret 2026 dengan dampak biaya Rp23.000.000 tanpa menggeser tanggal selesai. **Tujuan utama proyek tercapai:** *unreadable rate* 0,42%, respons dashboard 1,8 detik, integrasi DCS berjalan, 50 personel terlatih, dan proyek selesai tepat waktu dengan biaya akhir Rp242.678.233.

### 3.4 Scorecard Kinerja Proyek

| Dimensi | Target | Realisasi | Status |
|---|---|---|---|
| Jadwal (SPI) | SPI = 1 | SPI = 1,00 | Tercapai |
| Biaya (CPI) | CPI = 1 | CPI = 1,00 | Tercapai |
| Scope | 100% selesai | 100% *deliverable* diserahkan | Tercapai |
| Risiko | Terkendali | 9 risiko teridentifikasi, 8 *closed*, 1 *monitoring*; 0 risiko tidak terduga | Tercapai |

---

## 4. REALISASI SCOPE

### 4.1 Perencanaan Deliverable Project

| No | Milestone / Deliverable | Tanggal Rencana | Status |
|---|---|---|---|
| 1 | M1 — Kebutuhan dan desain disetujui | 25 Februari 2026 | Tercapai |
| 2 | M2 — Pengadaan hardware selesai | 6 Maret 2026 | Tercapai |
| 3 | M3 — Instalasi fisik selesai | 16 Maret 2026 | Tercapai |
| 4 | Fase pengembangan software, integrasi DCS, validasi RFID | 2–8 April 2026 | Tercapai |
| 5 | Fase pengujian: SIT, UAT, simulasi bagasi nyasar | 2–15 April 2026 | Tercapai |
| 6 | Pelatihan 50 personel | 16–21 April 2026 | Tercapai |
| 7 | M4 — Sistem siap operasional dan serah terima | 24 April 2026 | Tercapai |

### 4.2 Work Breakdown Structure

| No | Work Package | Status |
|---|---|---|
| 1 | 1.1 Manajemen Proyek | F |
| 2 | 1.2 Survei & Perencanaan | F |
| 3 | 1.3 Pengadaan Hardware | F |
| 4 | 1.4 Pengembangan Software (termasuk 1.4.7 *Middleware API DCS* dan 1.4.8 Validasi & *Retry* RFID) | F |
| 5 | 1.5 Instalasi & Konfigurasi | F |
| 6 | 1.6 Pengujian, Pelatihan & Penutupan | F |
| 7 | 1.7 *Contingency Reserve* | F |

Keterangan: F = *Fully Completed* (100%) | P = *Partially Completed* (50%) | N = *Not Completed* (0%).

### 4.3 Analisis Status Work Package

Seluruh *work package* berada pada status **F (*Fully Completed*)**. Tidak ada *work package* yang *partially* atau *not completed*.

| No | Work Package | Keterangan |
|---|---|---|
| 1 | — | Tidak ada *work package* yang belum selesai. |

---

## 5. REALISASI JADWAL

### 5.1 Activity on Node Jadwal Proyek

**Jalur kritis proyek:** 1.1 → 1.2 → 1.3 → 1.4 → 1.6 → M4 (1.6.6)

```
[1.1 Manajemen Proyek]──┐
                        │
[1.2 Survei &           │
 Perencanaan]───────────┼──►[1.3 Pengadaan Hardware]──►[1.4 Pengembangan
                        │                              Software]*──►[1.6 Pengujian,
[1.5 Instalasi &        │                                               Pelatihan &
 Konfigurasi]───────────┘                                               Penutupan]──►[M4 Sistem
                                                                                     Siap Operasional
                                                                                     24 Apr 2026]
```

\* 1.4 mencakup 1.4.1–1.4.6 serta 1.4.7 (*Middleware API DCS*, 5 hari) dan 1.4.8 (Validasi & *Retry* RFID, 3 hari) yang dijadwalkan paralel pada 2–8 April 2026 tanpa menambah panjang jalur kritis.

> **[Placeholder: tempel gambar AON final dari MS Project di sini.]**

### 5.2 Perbandingan Jadwal per Fase Proyek

Fase proyek ditentukan berdasarkan WBS level 2.

| No | Fase Proyek | Start Rencana | Start Realisasi | Selisih (Hari) | Finish Rencana | Finish Realisasi | Selisih (Hari) |
|---|---|---|---|---|---|---|---|
| 1 | 1.1 Manajemen Proyek | 9 Feb 2026 | 9 Feb 2026 | 0 | 24 Apr 2026 | 24 Apr 2026 | 0 |
| 2 | 1.2 Survei & Perencanaan | 9 Feb 2026 | 9 Feb 2026 | 0 | 25 Feb 2026 | 25 Feb 2026 | 0 |
| 3 | 1.3 Pengadaan Hardware | 12 Feb 2026 | 12 Feb 2026 | 0 | 6 Mar 2026 | 6 Mar 2026 | 0 |
| 4 | 1.4 Pengembangan Software | 12 Feb 2026 | 12 Feb 2026 | 0 | 8 Apr 2026 | 8 Apr 2026 | 0 |
| 5 | 1.5 Instalasi & Konfigurasi | 2 Mar 2026 | 2 Mar 2026 | 0 | 16 Mar 2026 | 16 Mar 2026 | 0 |
| 6 | 1.6 Pengujian, Pelatihan & Penutupan | 2 Apr 2026 | 2 Apr 2026 | 0 | 24 Apr 2026 | 24 Apr 2026 | 0 |
| 7 | 1.7 *Contingency Reserve* | — | — | 0 | 24 Apr 2026 | 24 Apr 2026 | 0 |

### 5.3 Nilai Schedule Performance Index (SPI)

Nilai EV dan PV di bawah adalah nilai saat status date M8 (20 Maret 2026), ketika SPI proyek masih 0,818. Nilai EV dan PV pada saat penutupan tidak lagi bermakna sebagai indikator keterlambatan, karena seluruh pekerjaan dan milestone telah 100% selesai pada tanggal rencana 24 April 2026 — **SPI akhir = 1,00**.

| Fase Proyek | Earned Value (EV) | Planned Value (PV) | SPI (EV / PV) |
|---|---|---|---|
| 1.1 Manajemen Proyek | Rp12.480.000 | Rp8.640.000 | 1,44 |
| 1.2 Survei & Perencanaan | Rp13.320.000 | Rp13.320.000 | 1,00 |
| 1.3 Pengadaan Hardware | Rp75.058.233 | Rp75.058.233 | 1,00 |
| 1.4 Pengembangan Software | Rp21.720.000 | Rp33.810.000 | 0,64 |
| 1.5 Instalasi & Konfigurasi | Rp0 | Rp11.680.000 | 0,00 |
| 1.6 Pengujian, Pelatihan & Penutupan | Rp0 | Rp0 | — |
| 1.7 *Contingency Reserve* | Rp0 | Rp7.390.000 | 0,00 |
| **Total (work packages)** | **Rp122.578.233** | **Rp149.898.233** | **0,818** |

SPI total saat penutupan (24 April 2026): **1,00**.

Selama proyek berlangsung, SPI pernah berada di bawah 1 (**0,818 pada 20 Maret 2026**) dengan SV −Rp27.319.100. Penyebabnya adalah dua hal. Pertama, **fase instalasi & konfigurasi (1.5)** yang direncanakan selesai 16 Maret 2026 belum dimulai pada status date — tertunda karena menunggu penjadwalan *window* kerja sama dengan pihak bandara dan penyesuaian posisi *access point outdoor* di area apron, sehingga memberikan kontribusi SV −Rp11.680.000. Kedua, **fase pengembangan software (1.4)** baru mencapai 50% pada task yang sudah dimulai (1.4.1–1.4.4), sementara 1.4.5 dan 1.4.6 belum dimulai, sehingga SV −Rp12.090.000. Selain itu, *contingency reserve* (1.7) yang dijadwalkan pada periode tersebut turut memperbesar SV secara statistik (Rp7.390.000) meskipun bukan pekerjaan fisik. Keterlambatan ini dipulihkan melalui tindakan korektif: instalasi fisik dipercepat dan selesai 16 Maret, pengujian disiapkan secara paralel, serta *work package* perubahan 1.4.7 dan 1.4.8 dikerjakan paralel di dalam *float* fase pengembangan. Hasilnya, seluruh milestone tercapai dan proyek selesai tepat pada 24 April 2026.

---

## 6. REALISASI BIAYA

### 6.1 Perbandingan Anggaran

| No | Fase Proyek | BAC (Rencana) | Actual Cost | Selisih |
|---|---|---|---|---|
| 1 | 1.1 Manajemen Proyek | Rp12.480.000 | Rp12.480.000 | Rp0 |
| 2 | 1.2 Survei & Perencanaan | Rp13.320.000 | Rp13.320.000 | Rp0 |
| 3 | 1.3 Pengadaan Hardware | Rp75.058.233 | Rp75.058.233 | Rp0 |
| 4 | 1.4 Pengembangan Software (termasuk 1.4.7 Rp15.000.000 dan 1.4.8 Rp8.000.000) | Rp72.040.000 | Rp72.040.000 | Rp0 |
| 5 | 1.5 Instalasi & Konfigurasi | Rp11.680.000 | Rp11.680.000 | Rp0 |
| 6 | 1.6 Pengujian, Pelatihan & Penutupan | Rp41.600.000 | Rp41.600.000 | Rp0 |
| 7 | 1.7 *Contingency Reserve* | Rp13.500.000 | Rp13.500.000 | Rp0 |
| — | *Fixed cost* proyek | Rp3.000.000 | Rp3.000.000 | Rp0 |
| **Total** | | **Rp242.678.233** | **Rp242.678.233** | **Rp0** |

### 6.2 Nilai Cost Performance Index (CPI)

| Fase Proyek | Earned Value (EV) | Actual Cost (AC) | CPI (EV / AC) |
|---|---|---|---|
| 1.1 Manajemen Proyek | Rp12.480.000 | Rp12.480.000 | 1,00 |
| 1.2 Survei & Perencanaan | Rp13.320.000 | Rp13.320.000 | 1,00 |
| 1.3 Pengadaan Hardware | Rp75.058.233 | Rp75.058.233 | 1,00 |
| 1.4 Pengembangan Software | Rp72.040.000 | Rp72.040.000 | 1,00 |
| 1.5 Instalasi & Konfigurasi | Rp11.680.000 | Rp11.680.000 | 1,00 |
| 1.6 Pengujian, Pelatihan & Penutupan | Rp41.600.000 | Rp41.600.000 | 1,00 |
| 1.7 *Contingency Reserve* | Rp13.500.000 | Rp13.500.000 | 1,00 |
| *Fixed cost* proyek | Rp3.000.000 | Rp3.000.000 | 1,00 |
| **Total** | **Rp242.678.233** | **Rp242.678.233** | **1,00** |

**Interpretasi:** CPI = 1 → **sesuai anggaran** (*on budget*). Seluruh pekerjaan diselesaikan sebesar anggaran yang direncanakan, termasuk anggaran tambahan dari dua *change request* (01/CR/2026 sebesar Rp15.000.000 dan 02/CR/2026 sebesar Rp8.000.000) yang telah dimasukkan ke BAC melalui *cost baseline* pada 25 Maret 2026. Tidak ada pembengkakan biaya; total biaya akhir Rp242.678.233 masih di bawah pagu Charter Rp285.000.000 dengan sisa pagu Rp42.321.767.

### 6.3 Realisasi Contingency Reserve

| Item | Nilai |
|---|---|
| *Contingency Reserve* Awal | Rp13.500.000 |
| *Contingency Reserve* Terpakai | Rp0 |
| Sisa *Contingency Reserve* | Rp13.500.000 |

*Contingency Reserve* **tidak terpakai**. Kedua *change request* dibiayai dari ***management reserve*** di dalam pagu Charter (awal Rp65.321.767, tersisa Rp42.321.767 setelah dua CR), sesuai keputusan CCB 24 Maret 2026, sehingga *contingency reserve* tetap utuh sebagai cadangan untuk risiko yang sudah teridentifikasi.

| No | Deskripsi | Biaya |
|---|---|---|
| 1 | — (tidak ada penggunaan *contingency reserve*) | Rp0 |
| **Total** | | **Rp0** |

---

## 7. REALISASI RISIKO

### 7.1 Tabel Realisasi Risiko

| ID | Risiko | Realisasi | Respons |
|---|---|---|---|
| R-01 | Keterlambatan pengadaan hardware | Tidak terjadi; pengadaan selesai 6 Maret 2026 | Pemesanan awal, monitoring vendor, *buffer* pengiriman |
| R-02 | Ketidakcocokan protokol DCS | Terjadi; DCS menggunakan protokol *legacy* | 01/CR/2026 *Middleware API DCS*, *contract test*, simulator DCS |
| R-03 | *Window* instalasi malam terbatas | Terjadi sebagian; jadwal instalasi menyesuaikan *window* bandara | Koordinasi slot, tim siaga, pekerjaan per zona |
| R-04 | *Read rate* RFID rendah | Terjadi pada pengujian; pembacaan tag kadang gagal | Site survey, penempatan tag, kalibrasi, 02/CR/2026 validasi & *retry* |
| R-05 | *Wi-Fi dead spot* di apron | Terjadi; coverage apron tidak merata | *Access point outdoor*, survey coverage, uji roaming |
| R-06 | Ketersediaan staf untuk pelatihan | Terjadi; pelatihan mundur 3 hari dari target | Pelatihan dua batch, jadwal *shift*, *refresher* |
| R-07 | Perubahan lingkup | Terjadi; dua CR diajukan | CCB, 01/CR/2026 dan 02/CR/2026, pembaruan BAC |
| R-08 | Cuaca saat instalasi *outdoor* | Tidak berdampak signifikan | Penjadwalan fleksibel, pekerjaan dalam ruang |
| R-09 | Pembaruan protokol DCS dari vendor | Tidak terjadi selama proyek | Monitoring vendor, *regression test*, *documented interface* |

### 7.2 Unidentified Risk

Selain risiko yang tercatat pada *risk register*, muncul satu risiko baru selama pelaksanaan, yaitu beban kerja tim yang meningkat akibat pekerjaan 1.4.7 dan 1.4.8 dikerjakan paralel pada 2–9 April 2026.

| ID | Work Package | Risiko | Level Risiko | Respons |
|---|---|---|---|---|
| R-10 | 1.4 / 1.6 | Beban kerja berlebih pada tim pengembangan dan QA akibat kerja paralel CR | Sedang | Prioritas tugas, lembur terjadwal, monitoring harian PM, kesiapan *fast-tracking*; tidak berdampak pada milestone 24 April 2026 |

---

## 8. RINGKASAN PERUBAHAN

### 8.1 Change Request Log

| ID | Tanggal | Deskripsi | Pengaju | Keputusan CCB |
|---|---|---|---|---|
| 01/CR/2026 | 18 Maret 2026 | Pengembangan *Middleware API DCS* (WBS 1.4.7) | Muhammad Nabiel Lukman Hakim (System Analyst) | Disetujui, 24 Maret 2026 |
| 02/CR/2026 | 21 Maret 2026 | Pengembangan Validasi dan *Retry* RFID (WBS 1.4.8) | Muhammad Nabiel Lukman Hakim (System Analyst) | Disetujui, 24 Maret 2026 |

### 8.2 Change Implementation

| ID | Dampak | Scope | Durasi | Cost |
|---|---|---|---|---|
| 01/CR/2026 | Penambahan *work package* 1.4.7 | +1 *work package*: *Middleware API DCS* | +5 hari kerja (paralel, selesai proyek tetap 24 April 2026) | +Rp15.000.000 |
| 02/CR/2026 | Penambahan *work package* 1.4.8 | +1 *work package*: Validasi dan *Retry* RFID | +3 hari kerja (paralel, selesai proyek tetap 24 April 2026) | +Rp8.000.000 |

### 8.3 Ringkasan Dampak Perubahan

| Item | Nilai |
|---|---|
| Total *Change Request* Diajukan | 2 |
| Total *Change Request* Disetujui | 2 |
| Total *Change Request* Ditolak | 0 |
| Total Perubahan Durasi (Hari) | 0 hari pada tanggal selesai proyek (+8 hari kerja usaha yang diserap dalam *float*) |
| Total Perubahan BAC | +Rp23.000.000 (Rp219.678.233 → Rp242.678.233) |
| Total Perubahan *Contingency Reserve* | Rp0 (dibiayai dari *management reserve*) |

---

## 9. LESSONS LEARNED

### 9.1 Apa yang Berjalan Baik (*What Went Well*)

| No | Area | Temuan | Rekomendasi |
|---|---|---|---|
| 1 | Biaya | Seluruh pekerjaan selesai sesuai anggaran; CPI 1,00 dan VAC Rp0, termasuk dua CR | Pertahankan disiplin *cost baseline* dan pembaruan BAC setiap kali CR disetujui |
| 2 | Jadwal | Dua *work package* tambahan diserap dalam *float* sehingga tanggal selesai tetap 24 April 2026 | Identifikasi *float* pada setiap fase sebelum menyetujui CR baru |
| 3 | Risiko | 8 dari 9 risiko tertutup, termasuk risiko protokol DCS dan *read rate* RFID | Lanjutkan *risk review* mingguan dan pemantauan risiko residual |
| 4 | Komunikasi | Rapat CCB dan laporan mingguan memudahkan koordinasi antara PM, System Analyst, QA, dan *user* | Pertahankan format laporan mingguan dan notulen CCB standar |
| 5 | Sumber Daya | Tim internal menyerap beban pekerjaan tambahan tanpa menambah personel | Petakan kapasitas tim sejak fase perencanaan untuk mengantisipasi CR |
| 6 | Perubahan | Seluruh perubahan tercatat formal dalam CR Log dengan keputusan CCB | Terus gunakan proses *Integrated Change Control* yang sama |

### 9.2 Apa yang Tidak Berjalan Baik (*What Did Not Go Well*)

| No | Area | Temuan | Penyebab |
|---|---|---|---|
| 1 | Sumber Daya | Pelatihan 50 personel selesai 21 April 2026, 3 hari setelah target 18 April 2026 | Pelatihan menunggu penyelesaian pengujian 1.4.7 dan 1.4.8; penjadwalan *shift* staf *ground handling* terbatas |
| 2 | Scope | Dua CR muncul di tengah pelaksanaan untuk kebutuhan yang seharusnya sudah teridentifikasi | Protokol *legacy* DCS dan karakteristik pembacaan RFID belum diverifikasi menyeluruh saat perencanaan |
| 3 | Jadwal | SPI turun ke 0,818 pada 20 Maret 2026 (SV −Rp27.319.100) | Instalasi fisik (1.5) belum dimulai sesuai rencana 16 Maret; pengembangan software (1.4) baru 50% |
| 4 | Sumber Daya | Beban kerja tim meningkat pada 2–9 April 2026 (risiko R-10) | Pekerjaan 1.4.7 dan 1.4.8 dikerjakan paralel di dalam jadwal yang sama |

### 9.3 Rekomendasi

1. Lakukan **validasi antarmuka sistem eksternal** (protokol DCS) dan **pengujian perangkat RFID di lapangan** pada tahap perencanaan, sebelum baseline disetujui.
2. Jadwalkan pelatihan staf secara **modular dan lebih awal**, serta koordinasikan jadwal *shift* sejak awal agar tidak bergantung pada selesainya pengujian terakhir.
3. Pertahankan **proses CCB dan CR Log** sebagai kontrol perubahan formal; setiap CR wajib dilengkapi analisis dampak scope, jadwal, dan biaya.
4. Pantau **risiko residual** pasca-serah terima: pembaruan protokol DCS oleh vendor, kualitas tag RFID, dan adopsi operasional personel baru.
5. Siapkan **kapasitas tim cadangan** untuk mengantisipasi pekerjaan paralel akibat perubahan lingkup.

---

## 10. PENUTUP

| No | Deliverable | Status Penerimaan | Catatan |
|---|---|---|---|
| 1 | 6 unit RFID *Reader Gate* dan 5 unit *handheld scanner* terpasang dan aktif | Diterima | Verifikasi fungsi selesai 16 Maret 2026 |
| 2 | 5.000 *smart tag* dan printer RFID | Diterima | Seluruh unit diterima dan digunakan |
| 3 | *Backend*, basis data, dan dashboard web *real-time* | Diterima | Respons 1,8 detik |
| 4 | *Middleware API DCS* (01/CR/2026) | Diterima | Lulus *integration test* 12/12 skenario |
| 5 | Modul validasi dan *retry* RFID (02/CR/2026) | Diterima | Lulus 6/6 skenario; *read success rate* 99,7% |
| 6 | Laporan SIT, UAT, dan *integration test* | Diterima | UAT 98,4% lulus, 2 *defect* minor ditutup |
| 7 | Buku panduan operasional, *admin guide*, dan *runbook* | Diterima | Diserahkan bersama serah terima |
| 8 | *Asset list* dan informasi garansi vendor | Diterima | Diserahkan ke Divisi TI |
| 9 | Pelatihan 50 personel | Diterima | Selesai 21 April 2026 |

Dengan ditandatanganinya dokumen ini, klien/sponsor menyatakan bahwa seluruh *deliverable* yang tercantum di atas telah diterima dan diverifikasi.

### Persetujuan Dokumen

Dengan ditandatanganinya dokumen ini, seluruh pihak menyatakan bahwa proyek telah ditutup secara resmi dan seluruh kewajiban telah terpenuhi.

**Project Manager** — Ir. Primary Putri Ardiva

Nama & Tanda Tangan: _______________________________________________

Tanggal: _______________________________________________

**Sponsor / Klien** — Ir. H. Max Verstappen

Nama & Tanda Tangan: _______________________________________________

Tanggal: _______________________________________________

---

## LAMPIRAN (ATTACHMENTS)

Dokumen-dokumen berikut dilampirkan sebagai bagian dari laporan penutupan proyek ini. Centang dokumen yang telah tersedia dan dilampirkan.

### A. *Project Management Documentation*

- [x] Project Charter — Project Charter Kelompok 1_SI-B_Milestone 1.pdf
- [x] WBS Code dan Diagram
- [x] Activity List
- [x] Resource Breakdown Structure
- [x] Resource Requirement
- [x] Risk Register — `docs/05-risk-register.md`
- [x] Baseline dan actual Gantt chart — `Projek Akhir MPTI_RFID pelacakan bagasi bandara_M9_M10_FINAL.xml`
- [x] Work Performance Data — `docs/03-wpd-earned-value.md`
- [x] Formulir Change Request — `docs/06-cr-form.md` (01/CR/2026) dan `docs/06b-cr-form-002.md` (02/CR/2026)

### B. *Product-Related Documentation*

- [x] Spesifikasi integrasi DCS dan desain *Middleware API*
- [x] Aturan validasi dan konfigurasi *retry* pembacaan RFID
- [x] Laporan *integration test* DCS dan pengujian gagal baca RFID
- [x] Laporan SIT
- [x] Laporan UAT dan simulasi bagasi nyasar
- [x] Buku panduan operasional dan *admin guide*
- [x] *Runbook* integrasi dan prosedur *backup*
- [x] *Asset list* dan informasi garansi vendor

---

*Dokumen ini merupakan lampiran CP3 Proyek LUGGIO dan disusun mengikuti format Closing Report (Laporan Penutupan Proyek).*