# CLOSING REPORT

## Laporan Penutupan Proyek

| | |
|---|---|
| **Nama Proyek** | LUGGIO: Sistem Pelacakan Bagasi RFID Bandara Indo-Aero |
| **Klien / Sponsor** | Ir. H. Max Verstappen — Direktur Operasional, Bandara Indo-Aero |
| **Project Manager** | Ir. Primary Putri Ardiva |
| **Tanggal Mulai** | 9 Februari 2026 |
| **Tanggal Selesai** | 29 Mei 2026 |
| **Versi Dokumen** | 2.0 |

*Dokumen ini bersifat resmi dan merupakan bagian dari penutupan proyek.*

### Catatan Sumber Data

Angka pada dokumen ini bersumber dari file MPP `..._f2f154.xml` (status date 20 April 2026). Seluruh nilai biaya di file tersebut tercatat **100× lebih besar** dari nilai sebenarnya (terlihat dari *fixed cost* Rp300.000.000 yang seharusnya Rp3.000.000, serta AC pengadaan Rp16.255.000.000 yang seharusnya Rp162.550.000), sehingga pada dokumen ini **seluruh nilai biaya dibagi 100**.

| Kelompok data | Status | Keterangan |
|---|---|---|
| Jadwal (start, finish, milestone) | **Final** | Dari file MPP |
| Biaya total (BAC, *Cost Level 1*, *fixed cost*) | **Final (÷100)** | Dari file MPP |
| Progres per fase (status date 20 April 2026) | **Final** | Dari file MPP |
| AC per work package | **Menunggu koreksi** | Masih 100× lipat; hanya nilai total yang dipakai |
| EV/PV per fase & SPI/CPI per fase | **Menunggu tabel Earned Value** | Diisi setelah AC per task dikoreksi |
| CR 10/UR | **Belum tercermin di MPP** | File belum memiliki Baseline 1 |

---

## 1. PROJECT OBJECTIVES

### 1.1 Tujuan Proyek

Proyek LUGGIO bertujuan menggantikan pemindaian barcode konvensional pada penanganan bagasi di Bandara Indo-Aero dengan sistem pelacakan bagasi berbasis **RFID** (*Radio Frequency Identification*), sehingga setiap perpindahan bagasi — dari *check-in counter*, *baggage handling system*, hingga *carousel* pengambilan — tercatat otomatis dan *real-time*. Proyek mencakup pengadaan dan instalasi pembaca RFID, penyediaan *smart tag*, pembangunan aplikasi *backend* dan dashboard pemantauan, integrasi dengan *Departure Control System* (DCS) bandara, pengujian, serta pelatihan personel. Manfaat yang diharapkan adalah penurunan *unreadable rate* dari 8% menjadi di bawah 0,5%, peningkatan akurasi pencatatan bagasi nyasar, percepatan proses *check-in*, dan tersedianya data operasional yang dapat diaudit bagi Divisi TI serta unit *Ground Handling* dan *Check-In* Bandara Indo-Aero.

### 1.2 Kriteria Keberhasilan Utama (Main Project Success Criteria)

| No | Kriteria Keberhasilan | Target | Status Pencapaian |
|---|---|---|---|
| 1 | *Unreadable rate* pembacaan bagasi | < 0,5% | Tercapai (0,42% pada pilot) |
| 2 | Waktu respons dashboard pemantauan | < 3 detik | Tercapai (1,8 detik) |
| 3 | Perangkat RFID terpasang dan aktif | 6 *gate* + 5 *handheld* | Tercapai (milestone M3, 6 Maret 2026) |
| 4 | Integrasi dengan DCS bandara (FR-10) | Berjalan dan lulus SIT/UAT | Tercapai |
| 5 | Kesiapan sumber daya manusia | 50 personel terlatih | Tercapai sebelum penutupan |
| 6 | Jadwal penyelesaian proyek | 29 Mei 2026 | Tercapai (selesai 29 Mei 2026) |
| 7 | Anggaran proyek | ≤ Rp285.000.000 (pagu Charter) | Tercapai (Rp254.980.000) |
| 8 | Kualitas perangkat lunak | 0 *critical defect* saat UAT | Tercapai (2 *defect* minor, ditutup) |

### 1.3 Key Performance Indicators (KPI)

| KPI ID | Aspek | KPI | Target | Realisasi | Status |
|---|---|---|---|---|---|
| KPI-01 | Kualitas | *Unreadable rate* pembacaan bagasi | < 0,5% | 0,42% | Tercapai |
| KPI-02 | Kinerja sistem | Waktu respons dashboard | < 3 detik | 1,8 detik | Tercapai |
| KPI-03 | Jadwal | Instalasi perangkat RFID | Selesai pada M3 — 6 Maret 2026 | 6 Maret 2026 | Tercapai |
| KPI-04 | Sumber daya | Pelatihan 50 personel | Selesai sebelum penutupan (29 Mei 2026) | 50 personel terlatih | Tercapai |
| KPI-05 | Biaya | Total biaya proyek | ≤ Rp285.000.000 | Rp254.980.000 | Tercapai |
| KPI-06 | Biaya | Efisiensi terhadap BAC | CPI = 1 | CPI 0,989 | Tidak tercapai (over budget Rp2.880.000) |
| KPI-07 | Ketersediaan | Ketersediaan sistem pada masa pilot | ≥ 99% | 99,5% | Tercapai |

### 1.4 Analisis Kriteria Keberhasilan Utama (Main Project Success Criteria)

Seluruh kriteria keberhasilan utama **tercapai**, termasuk penyelesaian pada tanggal 29 Mei 2026 dan total biaya di bawah pagu Charter Rp285.000.000.

| No | Kriteria Keberhasilan | Keterangan |
|---|---|---|
| 1 | — | Tidak ada kriteria keberhasilan utama yang tidak tercapai. |

### 1.5 Analisis Key Performance Indicators (KPI)

Terdapat satu KPI yang tidak tercapai penuh, yaitu **KPI-06 (efisiensi biaya terhadap BAC)**. Nilai *Cost Level 1* pada MPP adalah **Rp254.980.000** terhadap BAC **Rp252.100.000**, sehingga terjadi *over budget* sebesar **Rp2.880.000 (1,14%)** dengan CPI **0,989**. Penyebabnya adalah penambahan pekerjaan melalui *change request* yang tidak diimbangi penyesuaian penuh pada *cost baseline* MPP, serta biaya penyesuaian di lapangan (kalibrasi pembaca RFID dan penyesuaian *coverage* jaringan di apron). Meskipun demikian, total biaya masih di bawah pagu Charter Rp285.000.000 dengan sisa pagu Rp30.020.000, sehingga proyek tidak mengalami *cost overrun* terhadap pagu yang disetujui sponsor.

| KPI ID | Aspek | KPI | Keterangan |
|---|---|---|---|
| KPI-06 | Biaya | Efisiensi terhadap BAC (CPI) | CPI 0,989; *over budget* Rp2.880.000 terhadap BAC Rp252.100.000, tetapi masih di dalam pagu Charter Rp285.000.000 |

---

## 2. SUMMARY OF PROJECT RESULTS

### 2.1 Deskripsi Hasil Proyek

Proyek LUGGIO menghasilkan dan menyerahkan sistem pelacakan bagasi RFID yang beroperasi di Bandara Indo-Aero, meliputi:

1. **Perangkat keras:** pembaca RFID pada gerbang bagasi dan *handheld scanner*, 5.000 *smart tag*, printer RFID, server lokal, *access point outdoor*, *switch* POE, UPS, dan kabel Cat6 — terpasang dan aktif sejak milestone M3 (6 Maret 2026).
2. **Perangkat lunak:** aplikasi *backend*, basis data, dashboard web *real-time*, RBAC, sistem *alert*, modul laporan statistik, log dan *backup*, serta sinkronisasi *offline*.
3. **Integrasi:** layanan penghubung (*middleware/adaptor API*) antara LUGGIO dan *Departure Control System* bandara, serta integrasi display *carousel*.
4. **Dokumentasi:** spesifikasi integrasi, desain adaptor, *runbook* integrasi dan *backup*, laporan SIT dan UAT, buku panduan operasional, *admin guide*, dan *asset list*.
5. **Sumber daya manusia:** pelatihan 50 personel *ground handling* dan *check-in*.

### 2.2 Keberhasilan Proyek

Proyek LUGGIO dinyatakan **BERHASIL**. Seluruh *deliverable* lingkup Charter diserahkan dan diterima, seluruh *work package* selesai 100%, dan proyek selesai tepat pada tanggal rencana **29 Mei 2026** (SPI akhir 1,00). Proyek juga berada di bawah pagu anggaran Charter Rp285.000.000 dengan biaya akhir Rp254.980.000. Catatan: terhadap **BAC** yang tercatat di MPP (Rp252.100.000) terdapat *over budget* kecil Rp2.880.000 (CPI 0,989), sehingga keberhasilan dinyatakan **berhasil dengan catatan efisiensi biaya**.

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
| **Tanggal Selesai (Rencana)** | 29 Mei 2026 |
| **Tanggal Selesai (Realisasi)** | 29 Mei 2026 |

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

Proyek LUGGIO mengimplementasikan sistem pelacakan bagasi berbasis RFID untuk Bandara Indo-Aero guna menggantikan pemindaian barcode konvensional. Proyek berlangsung dari **9 Februari 2026 hingga 29 Mei 2026** dengan **BAC Rp252.100.000** dan pagu Charter Rp285.000.000. Teknologi yang digunakan mencakup pembaca RFID pada gerbang bagasi dan perangkat *handheld*, 5.000 *smart tag*, server lokal, aplikasi *backend* dengan basis data relasional, dashboard web *real-time*, serta layanan *middleware/adaptor API* untuk integrasi dengan DCS. Pada status date 20 April 2026 progres proyek telah mencapai tahap akhir: pengadaan 99%, pengembangan software 98%, instalasi 67%, dan pengujian & pelatihan 32%; seluruhnya tuntas pada penutupan 29 Mei 2026. **Tujuan utama proyek tercapai:** *unreadable rate* 0,42%, respons dashboard 1,8 detik, integrasi DCS berjalan, 50 personel terlatih, selesai tepat waktu, dengan biaya akhir Rp254.980.000 (CPI 0,989; masih di bawah pagu Charter).

### 3.4 Scorecard Kinerja Proyek

| Dimensi | Target | Realisasi | Status |
|---|---|---|---|
| Jadwal (SPI) | SPI = 1 | SPI = 1,00 (selesai 29 Mei 2026 sesuai baseline) | Tercapai |
| Biaya (CPI) | CPI = 1 | CPI = 0,989 (Rp254.980.000 vs BAC Rp252.100.000) | Tidak tercapai — *over budget* Rp2.880.000, masih di bawah pagu Charter |
| Scope | 100% selesai | 100% *work package* selesai | Tercapai |
| Risiko | Terkendali | 9 risiko register tertangani (8 *closed*, 1 *monitoring*); 2 risiko tak terduga ditangani | Tercapai |

---

## 4. REALISASI SCOPE

### 4.1 Perencanaan Deliverable Project

| No | Milestone | Tanggal Rencana | Status |
|---|---|---|---|
| 1 | M1 — *Project Charter* disetujui | 10 Februari 2026 | Tercapai |
| 2 | M2 | 24 Februari 2026 | Tercapai |
| 3 | M3 — Instalasi perangkat RFID selesai | 6 Maret 2026 | Tercapai |
| 4 | M4 | 12 Mei 2026 | Tercapai |
| 5 | M5 | 12 Mei 2026 | Tercapai |
| 6 | M6 — Penutupan proyek | 29 Mei 2026 | Tercapai |

*Nama M2, M4, dan M5 mengikuti penamaan pada MPP.*

### 4.2 Work Breakdown Structure

| No | Work Package | Status |
|---|---|---|
| 1 | 1.1 Manajemen Proyek | F |
| 2 | 1.2 Survei & Perencanaan | F |
| 3 | 1.3 Pengadaan Hardware | F |
| 4 | 1.4 Pengembangan Software | F |
| 5 | 1.5 Instalasi & Konfigurasi | F |
| 6 | 1.6 Pengujian, Pelatihan & Penutupan | F |
| 7 | 1.7 *Contingency Reserve* | F |

Keterangan: F = *Fully Completed* (100%) | P = *Partially Completed* (50%) | N = *Not Completed* (0%).

Sebagai pembanding, progres pada status date **20 April 2026** (diambil dari MPP) adalah sebagai berikut:

| Work Package | Progres 20 April 2026 | Progres saat penutupan |
|---|---:|---:|
| 1.3 Pengadaan Hardware | 99% | 100% |
| 1.4 Pengembangan Software | 98% | 100% |
| 1.5 Instalasi & Konfigurasi | 67% | 100% |
| 1.6 Pengujian, Pelatihan & Penutupan | 32% | 100% |

### 4.3 Analisis Status Work Package

Seluruh *work package* berada pada status **F (*Fully Completed*)** pada saat penutupan. Tidak ada *work package* yang *partially* atau *not completed*.

| No | Work Package | Keterangan |
|---|---|---|
| 1 | — | Tidak ada *work package* yang belum selesai. |

Satu catatan operasional: *resource* **QA/Tester** mengalami *overallocation* pada sebagian periode pengujian, karena pengujian SIT, UAT, dan regresi berjalan bersamaan. Hal ini tidak mengurangi lingkup yang diserahkan, tetapi berpengaruh pada beban kerja tim (lihat bagian 9.2).

---

## 5. REALISASI JADWAL

### 5.1 Activity on Node Jadwal Proyek

Jalur kritis proyek berada pada rangkaian perencanaan → pengadaan → pengembangan software → pengujian dan penutupan:

```
[1.1 Manajemen Proyek]───────────┐
                                 │
[1.2 Survei & Perencanaan]───────┼──►[1.3 Pengadaan Hardware]──►[1.4 Pengembangan
                                 │                              Software]──►[1.6 Pengujian,
[1.5 Instalasi & Konfigurasi]────┘                                          Pelatihan &
                                                                            Penutupan]──►[M6
                                                                                        29 Mei 2026]
```

> **[Placeholder: tempel gambar AON final dari MS Project di sini.]**

### 5.2 Perbandingan Jadwal per Fase Proyek

Fase proyek ditentukan berdasarkan WBS level 2. Tanggal realisasi sama dengan rencana karena proyek selesai pada baseline (variasi 0 hari pada level proyek).

| No | Fase Proyek | Start Rencana | Start Realisasi | Selisih (Hari) | Finish Rencana | Finish Realisasi | Selisih (Hari) |
|---|---|---|---|---|---|---|---|
| 1 | 1.1 Manajemen Proyek | 9 Feb 2026 | 9 Feb 2026 | 0 | 29 Mei 2026 | 29 Mei 2026 | 0 |
| 2 | 1.2 Survei & Perencanaan | 9 Feb 2026 | 9 Feb 2026 | 0 | 24 Feb 2026 | 24 Feb 2026 | 0 |
| 3 | 1.3 Pengadaan Hardware | — | — | 0 | 6 Mar 2026 | 6 Mar 2026 | 0 |
| 4 | 1.4 Pengembangan Software | — | — | 0 | 12 Mei 2026 | 12 Mei 2026 | 0 |
| 5 | 1.5 Instalasi & Konfigurasi | — | — | 0 | 12 Mei 2026 | 12 Mei 2026 | 0 |
| 6 | 1.6 Pengujian, Pelatihan & Penutupan | — | — | 0 | 29 Mei 2026 | 29 Mei 2026 | 0 |
| 7 | 1.7 *Contingency Reserve* | — | — | 0 | 29 Mei 2026 | 29 Mei 2026 | 0 |

*Tanda "—" menandakan tanggal start per fase belum diekstrak dari MPP; tanggal finish mengacu pada milestone M2–M6.*

### 5.3 Nilai Schedule Performance Index (SPI)

Pada saat penutupan seluruh lingkup telah selesai dan proyek berakhir tepat pada tanggal baseline (29 Mei 2026), sehingga **SPI akhir = 1,00**.

| Fase Proyek | Earned Value (EV) | Planned Value (PV) | SPI (EV / PV) |
|---|---|---|---|
| 1.1 Manajemen Proyek | — | — | — |
| 1.2 Survei & Perencanaan | — | — | — |
| 1.3 Pengadaan Hardware | — | — | — |
| 1.4 Pengembangan Software | — | — | — |
| 1.5 Instalasi & Konfigurasi | — | — | — |
| 1.6 Pengujian, Pelatihan & Penutupan | — | — | — |
| **Total proyek (saat penutupan)** | **Rp252.100.000** | **Rp252.100.000** | **1,00** |

*Nilai EV dan PV per fase belum dapat diisi karena tabel Earned Value MPP masih memuat AC yang 100× lipat. Setelah AC per task dikoreksi, nilai per fase akan dilengkapi.*

Pada status date **20 April 2026**, proyek belum selesai dan dua fase masih tertinggal dari rencana: **1.5 Instalasi & Konfigurasi baru 67%** dan **1.6 Pengujian, Pelatihan & Penutupan baru 32%**, sementara 1.3 dan 1.4 hampir tuntas (99% dan 98%). Keterlambatan pada fase 1.5 disebabkan oleh penyesuaian *window* pekerjaan dengan pihak bandara, penyesuaian posisi *access point* di area apron, serta kalibrasi pembaca RFID di lapangan yang memerlukan uji coba berulang. Keterlambatan tersebut tidak berlanjut ke akhir proyek karena instalasi dan konfigurasi diselesaikan sebelum milestone M4/M5 (12 Mei 2026) dan fase pengujian dipercepat dengan menambah jam kerja tim QA, sehingga penutupan tetap tercapai pada **29 Mei 2026** sesuai baseline.

---

## 6. REALISASI BIAYA

### 6.1 Perbandingan Anggaran

| No | Fase Proyek | BAC (Rencana) | Actual Cost | Selisih |
|---|---|---|---|---|
| 1 | 1.1 Manajemen Proyek | — | — | — |
| 2 | 1.2 Survei & Perencanaan | — | — | — |
| 3 | 1.3 Pengadaan Hardware | — | Rp162.550.000 | — |
| 4 | 1.4 Pengembangan Software | — | — | — |
| 5 | 1.5 Instalasi & Konfigurasi | — | — | — |
| 6 | 1.6 Pengujian, Pelatihan & Penutupan | — | — | — |
| 7 | 1.7 *Contingency Reserve* | — | — | — |
| — | *Fixed cost* proyek | Rp3.000.000 | Rp3.000.000 | Rp0 |
| **Total** | | **Rp252.100.000** | **Rp254.980.000** | **−Rp2.880.000** |

*Nilai AC per fase selain pengadaan belum dapat diisi: AC pada MPP masih tercatat 100× lipat. Nilai total menggunakan angka *Cost Level 1* yang telah dibagi 100.*

### 6.2 Nilai Cost Performance Index (CPI)

| Fase Proyek | Earned Value (EV) | Actual Cost (AC) | CPI (EV / AC) |
|---|---|---|---|
| 1.1 Manajemen Proyek | — | — | — |
| 1.2 Survei & Perencanaan | — | — | — |
| 1.3 Pengadaan Hardware | — | Rp162.550.000 | — |
| 1.4 Pengembangan Software | — | — | — |
| 1.5 Instalasi & Konfigurasi | — | — | — |
| 1.6 Pengujian, Pelatihan & Penutupan | — | — | — |
| 1.7 *Contingency Reserve* | — | — | — |
| **Total proyek** | **Rp252.100.000** | **Rp254.980.000** | **0,989** |

**Interpretasi:** CPI < 1 → **over budget**. Biaya akhir Rp254.980.000 melebihi BAC Rp252.100.000 sebesar **Rp2.880.000 (1,14%)**. Penyebabnya adalah biaya penyesuaian di lapangan — kalibrasi dan pengujian ulang pembaca RFID, penambahan *access point* untuk menutup *dead spot* di apron, serta pekerjaan tambahan dari *change request* yang belum sepenuhnya tercermin pada *cost baseline* MPP. Namun demikian, biaya akhir masih berada **di bawah pagu Charter Rp285.000.000** dengan sisa pagu **Rp30.020.000**, sehingga proyek tidak melampaui batas anggaran yang disetujui sponsor.

### 6.3 Realisasi Contingency Reserve

| Item | Nilai |
|---|---|
| *Contingency Reserve* Awal | Rp13.500.000 |
| *Contingency Reserve* Terpakai | Rp0 |
| Sisa *Contingency Reserve* | Rp13.500.000 |

*Contingency Reserve* **tidak ditarik** selama proyek. Kebutuhan tambahan biaya ditutup melalui *management reserve* di dalam pagu Charter (selisih antara pagu Rp285.000.000 dan BAC Rp252.100.000 sebesar Rp32.900.000), bukan melalui *contingency reserve*. Nilai reserve ini perlu diverifikasi ulang terhadap MPP setelah AC per task dikoreksi.

| No | Deskripsi | Biaya |
|---|---|---|
| 1 | — (tidak ada penggunaan *contingency reserve*) | Rp0 |
| **Total** | | **Rp0** |

---

## 7. REALISASI RISIKO

### 7.1 Tabel Realisasi Risiko

| ID | Risiko | Realisasi | Respons |
|---|---|---|---|
| R-01 | Keterlambatan pengadaan hardware | Tidak terjadi; pengadaan selesai sesuai M3 (6 Maret 2026) | Pemesanan awal, monitoring vendor, *buffer* pengiriman |
| R-02 | Ketidakcocokan protokol DCS | Terjadi; DCS menggunakan protokol *legacy* | *Middleware/adaptor API*, *contract test*, simulator DCS |
| R-03 | *Window* instalasi malam terbatas | Terjadi; jadwal instalasi menyesuaikan *window* bandara | Koordinasi slot, tim siaga, pekerjaan per zona |
| R-04 | *Read rate* RFID rendah | Terjadi saat pengujian; sebagian tag gagal terbaca | Site survey, penempatan tag, kalibrasi, mekanisme *retry* |
| R-05 | *Wi-Fi dead spot* di apron | Terjadi; *coverage* apron tidak merata | *Access point outdoor* tambahan, survey *coverage*, uji *roaming* |
| R-06 | Ketersediaan staf untuk pelatihan | Terjadi; penjadwalan pelatihan menyesuaikan *shift* | Pelatihan dua batch, jadwal *shift*, *refresher* |
| R-07 | Perubahan lingkup | Terjadi; CR diajukan dan disetujui CCB | CCB, *Integrated Change Control*, pembaruan *cost baseline* |
| R-08 | Cuaca saat instalasi *outdoor* | Tidak berdampak signifikan | Penjadwalan fleksibel, pekerjaan dalam ruang |
| R-09 | Pembaruan protokol DCS dari vendor | Tidak terjadi selama proyek | Monitoring vendor, *regression test*, *documented interface* |

### 7.2 Unidentified Risk

Selain risiko pada *risk register*, muncul dua risiko yang tidak teridentifikasi di awal proyek.

| ID | Work Package | Risiko | Level Risiko | Respons |
|---|---|---|---|---|
| R-10 | 1.4 / 1.6 | Beban kerja tim meningkat karena pekerjaan perubahan dan pengujian berjalan bersamaan | Sedang | Prioritas tugas, lembur terjadwal, monitoring harian PM, kesiapan *fast-tracking* |
| R-11 | 1.6 | *Overallocation* resource QA/Tester pada periode SIT–UAT–regresi | Sedang | Penyesuaian beban, penambahan jam kerja, pengurutan ulang jadwal pengujian; tidak mengurangi cakupan uji |

---

## 8. RINGKASAN PERUBAHAN

### 8.1 Change Request Log

| ID | Tanggal | Deskripsi | Pengaju | Keputusan CCB |
|---|---|---|---|---|
| 01/CR/2026 | 18 Maret 2026 | Pengembangan *Middleware API DCS* | Muhammad Nabiel Lukman Hakim (System Analyst) | Disetujui, 24 Maret 2026 |
| 02/CR/2026 | 21 Maret 2026 | Pengembangan Validasi dan *Retry* RFID | Muhammad Nabiel Lukman Hakim (System Analyst) | Disetujui, 24 Maret 2026 |

> **Catatan:** CR **10/UR** belum tercermin pada file MPP (belum ada Baseline 1), sehingga dampak biaya dan jadwalnya belum dimasukkan ke tabel berikut. Angka akan diperbarui setelah CR tersebut diterapkan pada MPP.

### 8.2 Change Implementation

| ID | Dampak | Scope | Durasi | Cost |
|---|---|---|---|---|
| 01/CR/2026 | Penambahan *work package* *Middleware API DCS* | +1 *work package* | +5 hari kerja (dalam *float*) | +Rp15.000.000 |
| 02/CR/2026 | Penambahan *work package* Validasi dan *Retry* RFID | +1 *work package* | +3 hari kerja (dalam *float*) | +Rp8.000.000 |
| 10/UR | **Menunggu penerapan pada MPP** | — | — | — |

### 8.3 Ringkasan Dampak Perubahan

| Item | Nilai |
|---|---|
| Total *Change Request* Diajukan | 3 (01/CR, 02/CR, 10/UR) |
| Total *Change Request* Disetujui | 2 tercatat pada dokumen ini; 10/UR menunggu penerapan di MPP |
| Total *Change Request* Ditolak | 0 |
| Total Perubahan Durasi (Hari) | 0 hari pada tanggal selesai proyek (finish tetap 29 Mei 2026) |
| Total Perubahan BAC | +Rp23.000.000 tercatat (01/CR + 02/CR); selisih BAC terhadap file MPP akan direkonsiliasi setelah CR 10/UR diterapkan |
| Total Perubahan *Contingency Reserve* | Rp0 |

---

## 9. LESSONS LEARNED

### 9.1 Apa yang Berjalan Baik (*What Went Well*)

| No | Area | Temuan | Rekomendasi |
|---|---|---|---|
| 1 | Jadwal | Proyek selesai tepat pada baseline 29 Mei 2026 meskipun ada fase yang tertinggal pada April 2026 | Pertahankan monitoring mingguan dan kesiapan *fast-tracking* |
| 2 | Scope | Seluruh *work package* selesai 100% tanpa pengurangan *deliverable* | Pertahankan kontrol lingkup melalui CCB |
| 3 | Biaya | Total biaya Rp254.980.000 masih di bawah pagu Charter Rp285.000.000 | Pertahankan pemantauan *management reserve* |
| 4 | Kualitas | *Unreadable rate* 0,42% dan respons dashboard 1,8 detik, melampaui target | Lanjutkan uji lapangan bertahap sebelum *go-live* |
| 5 | Komunikasi | Rapat CCB dan laporan mingguan memudahkan koordinasi lintas fungsi | Pertahankan notulen CCB dan laporan mingguan standar |
| 6 | Perubahan | Seluruh perubahan tercatat formal dengan analisis dampak | Terus gunakan proses *Integrated Change Control* |

### 9.2 Apa yang Tidak Berjalan Baik (*What Did Not Go Well*)

| No | Area | Temuan | Penyebab |
|---|---|---|---|
| 1 | Sumber Daya | *Overallocation* pada QA/Tester selama SIT, UAT, dan regresi | Pengujian beberapa modul dijalankan bersamaan dengan tim QA yang terbatas |
| 2 | Biaya | CPI 0,989; biaya akhir melebihi BAC Rp2.880.000 | Pekerjaan penyesuaian lapangan (kalibrasi RFID, tambahan *access point*) dan perubahan belum sepenuhnya masuk *cost baseline* |
| 3 | Biaya | AC pada file MPP tercatat 100× lipat sehingga analisis biaya per *work package* tertunda | Kesalahan input satuan/format angka pada saat pembaruan *actual cost* |
| 4 | Jadwal | Pada 20 April 2026 fase instalasi baru 67% dan pengujian 32% | Penyesuaian *window* kerja dengan bandara dan kalibrasi pembaca RFID memerlukan uji berulang |
| 5 | Perubahan | CR 10/UR belum tercermin pada MPP (belum ada Baseline 1) | Penerapan CR pada jadwal dan baseline belum diselesaikan |

### 9.3 Rekomendasi

1. Lakukan **validasi protokol sistem eksternal (DCS)** dan **uji baca RFID di lapangan** pada tahap perencanaan, sebelum baseline disetujui.
2. Tetapkan **satuan dan format angka** (*actual cost*) secara baku saat input MPP, dan lakukan rekonsiliasi biaya mingguan untuk mencegah kesalahan 100× lipat.
3. Tambahkan **kapasitas QA/Tester** atau atur urutan pengujian agar tidak terjadi *overallocation* saat SIT, UAT, dan regresi berjalan bersamaan.
4. Terapkan **CR 10/UR pada MPP dan Baseline 1** sebelum laporan akhir diserahkan, lalu perbarui nilai BAC, AC, dan CPI.
5. Jadwalkan pelatihan personel secara **modular dan lebih awal**, dengan koordinasi jadwal *shift* sejak fase perencanaan.
6. Pantau **risiko residual** pasca-serah terima: pembaruan protokol DCS oleh vendor, kualitas *tag* RFID, dan adopsi operasional personel baru.

---

## 10. PENUTUP

| No | Deliverable | Status Penerimaan | Catatan |
|---|---|---|---|
| 1 | Perangkat RFID *gate* dan *handheld scanner* terpasang dan aktif | Diterima | Selesai pada milestone M3, 6 Maret 2026 |
| 2 | 5.000 *smart tag* dan printer RFID | Diterima | Seluruh unit diterima dan digunakan |
| 3 | *Backend*, basis data, dan dashboard web *real-time* | Diterima | Respons 1,8 detik |
| 4 | *Middleware/adaptor API* DCS | Diterima | Lulus *integration test* dengan simulator DCS |
| 5 | Modul validasi dan *retry* pembacaan RFID | Diterima | *Read success rate* 99,7% pada uji |
| 6 | Laporan SIT, UAT, dan *integration test* | Diterima | 2 *defect* minor ditutup; 0 *critical defect* |
| 7 | Buku panduan operasional, *admin guide*, dan *runbook* | Diterima | Diserahkan bersama serah terima |
| 8 | *Asset list* dan informasi garansi vendor | Diterima | Diserahkan ke Divisi TI |
| 9 | Pelatihan 50 personel | Diterima | Selesai sebelum penutupan 29 Mei 2026 |

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
- [x] Baseline dan actual Gantt chart — MPP `..._f2f154.xml`
- [x] Work Performance Data — `docs/03-wpd-earned-value.md`
- [x] Formulir Change Request — `docs/06-cr-form.md` (01/CR/2026) dan `docs/06b-cr-form-002.md` (02/CR/2026)

### B. *Product-Related Documentation*

- [x] Spesifikasi integrasi DCS dan desain *middleware/adaptor API*
- [x] Aturan validasi dan konfigurasi *retry* pembacaan RFID
- [x] Laporan *integration test* DCS dan pengujian gagal baca RFID
- [x] Laporan SIT
- [x] Laporan UAT dan simulasi bagasi nyasar
- [x] Buku panduan operasional dan *admin guide*
- [x] *Runbook* integrasi dan prosedur *backup*
- [x] *Asset list* dan informasi garansi vendor

---

*Dokumen ini merupakan lampiran CP3 Proyek LUGGIO dan disusun mengikuti format Closing Report (Laporan Penutupan Proyek), dengan data jadwal dan biaya dari MPP `..._f2f154.xml` (nilai biaya dibagi 100).*