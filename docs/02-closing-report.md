# Laporan Penutupan Proyek (Closing Report)

## Proyek LUGGIO — Sistem Pelacakan Bagasi RFID Bandara Indo-Aero

| Item | Keterangan |
|---|---|
| Nomor Dokumen | LUGGIO-CP3-M10-001 |
| Versi | 1.0 |
| Tanggal | 1 Mei 2026 |
| Status | Final |
| Proyek | LUGGIO: Sistem Pelacakan Bagasi RFID Bandara Indo-Aero |
| Baseline | Baseline 0 (24 April 2026) dan Baseline 1 (1 Mei 2026) |
| Penyusun | Muhammad Hasbi Assidiqi — Network/Hardware Engineer |
| Pemeriksa | Muhammad Nabiel Lukman Hakim — System Analyst |
| Persetujuan | Ir. Primary Putri Ardiva — Project Manager |
| Persetujuan | Ir. H. Max Verstappen — Project Sponsor |
| Penerimaan | Rusdi — User Representative |
| Dokumen terkait | Project Charter v1.0; MPP LUGGIO; M9 Change Management; Risk Register |

---

## A. Ringkasan Eksekutif

Proyek LUGGIO telah selesai dan diserahterimakan pada **1 Mei 2026**. Sistem pelacakan bagasi berbasis RFID telah terpasang, terintegrasi dengan DCS melalui middleware, diuji melalui SIT/UAT, dan digunakan oleh staf operasional bandara.

Proyek selesai **5 hari kerja setelah Baseline 0** karena perubahan yang disetujui, yaitu **CR-001: Pengembangan Middleware & Adaptor API DCS**. Perubahan ini menambah Rp15.000.000 dan 5 hari kerja, sehingga Baseline 1 menjadi 1 Mei 2026 dengan biaya Rp234.678.233.

| Indikator | Baseline 0 | Baseline 1 | Realisasi |
|---|---:|---:|---:|
| Tanggal selesai | 24 April 2026 | 1 Mei 2026 | **1 Mei 2026** |
| Durasi | 53 hari | 58 hari | **58 hari** |
| Biaya | Rp219.678.233 | Rp234.678.233 | **Rp234.678.233** |
| EV | — | — | **Rp219.678.233** |
| AC | — | — | **Rp234.678.233** |
| CPI | — | — | **0,936** |
| VAC | — | — | **−Rp15.000.000** |

Kinerja biaya berada di bawah pagu Charter Rp285.000.000. Varians biaya negatif Rp15.000.000 sepenuhnya berasal dari CR-001, bukan dari pembengkakan biaya pekerjaan dasar. Seluruh *deliverable* utama telah diterima; satu target KPI sumber daya manusia (pelatihan 50 personel sebelum 18 April) terlambat karena pergeseran jadwal CR-001, tetapi terpenuhi sebelum penutupan proyek.

---

## B. Verifikasi Lingkup dan Deliverable

### B.1 Lingkup yang Diserahkan

| Kelompok | Deliverable | Rencana | Realisasi | Status |
|---|---|---|---|---|
| Manajemen proyek | Charter, WBS, jadwal, risk register, laporan mingguan 1–10, closing report | Feb–Apr 2026 | Selesai | Diterima |
| Survei & desain | Survei titik pemasangan, peta jaringan, spesifikasi integrasi DCS | Feb 2026 | Selesai | Diterima |
| Hardware | 6 unit RFID Reader Gate, 5 unit handheld scanner, 5.000 smart tag, printer RFID, server lokal, access point outdoor, switch POE, kabel Cat6 | Mar 2026 | Terpasang/terpasang | Diterima |
| Software | Backend, database, dashboard web, RBAC, alert, laporan, backup, sinkronisasi offline | Feb–Apr 2026 | Selesai | Diterima |
| Integrasi | Middleware/adaptor DCS, integrasi display carousel | Apr 2026 | Selesai | Diterima |
| Instalasi fisik | Gerbang RFID, UPS, kabel data, access point | Mar 2026 | Selesai | Diterima |
| Pengujian | SIT, UAT, simulasi bagasi nyasar, regresi | Apr 2026 | Selesai | Diterima |
| Pelatihan | Pelatihan 50 personel ground handling dan check-in | Apr 2026 | Selesai | Diterima |
| Serah terima | Buku panduan operasional, admin guide, runbook, asset list | Apr–Mei 2026 | Selesai | Diterima |

### B.2 Perbandingan dengan Charter

| Area | Charter | Hasil |
|---|---|---|
| 6 RFID Reader Gate | 6 unit terpasang dan aktif | 6 unit terpasang dan aktif |
| 5 Handheld Scanner | 5 unit terpasang dan terhubung | 5 unit terpasang dan terhubung |
| 5.000 Smart Tag | Tersedia untuk uji coba | 5.000 unit diterima dan digunakan |
| Dashboard real-time | Respons <3 detik | 1,8 detik |
| Unreadable rate | <0,5% | 0,42% pada pilot |
| Integrasi DCS | FR-10 terpenuhi | Terpenuhi melalui middleware |
| Pelatihan | 50 personel | 50 personel |
| Pagu biaya | ≤Rp285.000.000 | Rp234.678.233 |

### B.3 Perubahan Lingkup

Satu-satunya perubahan lingkup adalah **CR-001** (middleware/adaptor API DCS). Tidak ada pekerjaan di luar *out of scope* Charter, tidak ada pengurangan *deliverable*, dan tidak ada perubahan pada conveyor belt maupun aplikasi mobile penumpang.

---

## C. Kinerja Jadwal

### C.1 Ringkasan Jadwal

| Item | Baseline 0 | Baseline 1 | Aktual |
|---|---|---|---|
| Mulai | 9 Februari 2026 | 9 Februari 2026 | 9 Februari 2026 |
| Selesai | 24 April 2026 | 1 Mei 2026 | **1 Mei 2026** |
| Durasi | 53 hari | 58 hari | **58 hari** |
| Variance terhadap Baseline 0 | — | +5 hari | **+5 hari** |
| Variance terhadap Baseline 1 | — | — | **0 hari** |

### C.2 Milestone

| Milestone | Baseline 0 | Baseline 1 | Aktual | Status |
|---|---|---|---|---|
| M1 — Kebutuhan dan desain disetujui | 25 Feb 2026 | 25 Feb 2026 | 25 Feb 2026 | Tercapai |
| M2 — Pengadaan selesai | 6 Mar 2026 | 6 Mar 2026 | 6 Mar 2026 | Tercapai |
| M3 — Instalasi fisik selesai | 16 Mar 2026 | 16 Mar 2026 | 16 Mar 2026 | Tercapai |
| M4 — Sistem siap operasional | 24 Apr 2026 | 1 Mei 2026 | 1 Mei 2026 | Tercapai |

### C.3 Analisis Jalur Kritis

Jalur kritis proyek berada pada rangkaian pengembangan software dan pengujian:

**1.4.6 → 1.4.7 (CR-001) → 1.6.1/1.6.2 → 1.6.3 → 1.6.4 → 1.6.5 → 1.6.6**

Pekerjaan pengadaan dan instalasi fisik memiliki kelonggaran 13–19 hari, sehingga tidak menjadi penentu tanggal akhir. Sebaliknya, penambahan 5 hari pada 1.4.7 langsung menggeser dua cabang pengujian paralel (1.6.1 dan 1.6.2), lalu UAT, pelatihan, dan penutupan.

### C.4 Varians Jadwal

- Terhadap Baseline 0: **+5 hari kerja**, seluruhnya disebabkan CR-001.
- Terhadap Baseline 1: **0 hari**; proyek selesai sesuai baseline yang telah disetujui.
- SPI saat selesai: **1,00** terhadap Baseline 1, karena seluruh lingkup baseline telah diselesaikan. Keterlambatan 5 hari tetap terlihat dari perbandingan tanggal Baseline 0 dan Baseline 1, bukan dari SPI akhir.

---

## D. Kinerja Biaya

### D.1 Ringkasan Earned Value

| Indikator | Nilai |
|---|---:|
| BAC (Baseline 0) | Rp219.678.233 |
| EV | Rp219.678.233 |
| AC | Rp234.678.233 |
| CV | **−Rp15.000.000** |
| CPI | **0,936** |
| EAC | **Rp234.678.233** |
| ETC | Rp0 |
| VAC | **−Rp15.000.000** |
| TCPI | 1,00 |

### D.2 Rincian Biaya per Fase

| WBS | Fase | Baseline 0 | CR-001 | Final |
|---|---|---:|---:|---:|
| 1.1 | Manajemen Proyek | Rp12.480.000 | — | Rp12.480.000 |
| 1.2 | Survei & Perencanaan | Rp13.320.000 | — | Rp13.320.000 |
| 1.3 | Pengadaan Hardware | Rp75.058.233 | — | Rp75.058.233 |
| 1.4 | Pengembangan Software | Rp49.040.000 | Rp15.000.000 | Rp64.040.000 |
| 1.5 | Instalasi & Konfigurasi | Rp11.680.000 | — | Rp11.680.000 |
| 1.6 | Pengujian, Pelatihan & Penutupan | Rp41.600.000 | — | Rp41.600.000 |
| 1.7 | Contingency Reserve | Rp13.500.000 | — | Rp13.500.000 |
| — | Fixed cost proyek | Rp3.000.000 | — | Rp3.000.000 |
| **Total** | | **Rp219.678.233** | **Rp15.000.000** | **Rp234.678.233** |

### D.3 Analisis Varians Biaya

1. **CPI 0,936** berarti setiap Rp1 yang dianggarkan menghasilkan Rp0,936 nilai pekerjaan. Varians negatif Rp15.000.000 berasal dari CR-001 yang disetujui, bukan dari inefisiensi pekerjaan dasar.
2. Tanpa CR-001, proyek berada tepat pada anggaran: EV = AC = Rp219.678.233 dan CPI = 1,00.
3. **Contingency reserve Rp13.500.000 tetap tercatat sebagai bagian BAC** dan tidak ditarik sebagai tambahan biaya di luar baseline. CR-001 didanai dari *management reserve* yang tersedia di dalam pagu Charter; tidak ada penggunaan contingency reserve khusus untuk CR-001.
4. Pagu Charter Rp285.000.000 tidak terlampaui. Sisa pagu setelah proyek adalah **Rp50.321.767**.
5. EAC sama dengan AC karena seluruh pekerjaan telah selesai (ETC = 0). VAC negatif Rp15.000.000 mencerminkan tambahan biaya perubahan, bukan pemborosan.

---

## E. Kualitas, Risiko, dan KPI

### E.1 Hasil KPI

| KPI | Target | Hasil | Status |
|---|---|---|---|
| KPI-01 — Unreadable rate | <5% | **0,42%** | Tercapai |
| KPI-02 — Respons dashboard | <3 detik | **1,8 detik** | Tercapai |
| KPI-03 — Instalasi fisik | 6 gate + 5 handheld aktif sebelum 10 Apr 2026 | **16 Mar 2026** | Tercapai |
| KPI-04 — Kesiapan SDM | 50 personel lulus pelatihan pada 18 Apr 2026 | **50 personel selesai 28 Apr 2026** | Terlambat 10 hari; terpenuhi sebelum closing |
| KPI-05 — Efisiensi biaya | ≤Rp285.000.000 | **Rp234.678.233** | Tercapai |

Catatan KPI-04: pergeseran 5 hari akibat CR-001 menggeser pelatihan dari 16–21 April menjadi 23–28 April. Seluruh 50 personel telah lulus sebelum penutupan proyek 1 Mei 2026, tetapi target tanggal 18 April tidak terpenuhi.

### E.2 Kualitas Pengujian

| Aktivitas | Hasil |
|---|---|
| Unit test modul utama | 100% test case lulus |
| Integration test DCS | 12/12 skenario lulus |
| SIT | 100% skenario kritis lulus |
| UAT | 98,4% test case lulus |
| Defect | 2 defect minor, ditutup; 0 critical |
| Regresi | Tidak ada regresi kritis |
| Unreadable rate pilot | 0,42% |
| Respons dashboard | 1,8 detik |
| Ketersediaan sistem pilot | 99,5% |

### E.3 Ringkasan Risiko

| ID | Risiko | Kategori | P | I | Skor | Status |
|---|---|---|---:|---:|---:|---|
| R-01 | Keterlambatan pengadaan hardware | Supply | 3 | 4 | 12 | Closed |
| R-02 | Ketidakcocokan protokol DCS | Teknis | 4 | 5 | 20 | Closed |
| R-03 | Window instalasi malam terbatas | Operasional | 3 | 3 | 9 | Closed |
| R-04 | Read rate RFID rendah | Kualitas | 3 | 4 | 12 | Closed |
| R-05 | Wi-Fi dead spot di apron | Teknis | 3 | 3 | 9 | Closed |
| R-06 | Ketersediaan staf untuk pelatihan | Resource | 3 | 3 | 9 | Residual |
| R-07 | Perubahan lingkup | Scope | 3 | 3 | 9 | Closed |
| R-08 | Cuaca saat instalasi outdoor | Eksternal | 2 | 3 | 6 | Closed |
| R-09 | Pembaruan protokol DCS dari vendor | Teknis | 2 | 4 | 8 | Open — monitoring |

### E.4 Respons Risiko

| ID | Respons |
|---|---|
| R-01 | Pemesanan awal, monitoring vendor, buffer pengiriman |
| R-02 | CR-001 middleware/adaptor, contract test, simulator |
| R-03 | Koordinasi slot, tim siaga, pekerjaan per zona |
| R-04 | Site survey, penempatan tag, pilot, kalibrasi |
| R-05 | AP outdoor, survey coverage, uji roaming |
| R-06 | Pelatihan dua batch, jadwal shift, refresher |
| R-07 | CCB, CR-001, baseline 1 |
| R-08 | Penjadwalan fleksibel, pekerjaan dalam ruang |
| R-09 | Monitoring vendor, regression test, documented interface |

Register lengkap dengan skor, penyebab, owner, dan residual tersedia dalam **Risk Register Proyek LUGGIO** (`docs/05-risk-register.md`).

### E.5 Risiko Residual

1. **Perubahan protokol DCS dari vendor.** Middleware perlu dipantau dan diuji ulang jika vendor melakukan pembaruan.
2. **Kualitas tag RFID.** Perlu audit berkala terhadap tag yang rusak atau tidak terbaca.
3. **Adopsi operasional.** Perlu pendampingan dan refresher training bagi personel baru.
4. **Ketergantungan koneksi jaringan.** Prosedur offline dan sinkronisasi harus diuji berkala.

---

## F. Manajemen Perubahan

| Item | Keterangan |
|---|---|
| CR | CR-001 — Pengembangan Middleware & Adaptor API DCS |
| Tanggal pengajuan | 18 Maret 2026 |
| Keputusan CCB | Disetujui dengan syarat, 24 Maret 2026 |
| Dampak biaya | +Rp15.000.000 |
| Dampak jadwal | +5 hari kerja |
| Baseline 0 | 24 April 2026; Rp219.678.233 |
| Baseline 1 | 1 Mei 2026; Rp234.678.233 |
| Status | Closed 1 Mei 2026 |
| CR lain | Tidak ada |

CR-001 tidak mengurangi lingkup, tidak mengubah pagu Charter, dan tidak menggunakan contingency reserve. Detail analisis dampak, notulen CCB, dan log perubahan tersedia dalam dokumen **M9 — Laporan Manajemen Perubahan**.

---

## G. Lessons Learned

1. **Validasi antarmuka eksternal harus dilakukan sebelum baseline disetujui.** Protokol DCS yang legacy seharusnya teridentifikasi pada tahap perencanaan, bukan saat desain integrasi.
2. **Middleware perlu dimasukkan sebagai pekerjaan eksplisit dalam WBS** ketika sistem eksternal menggunakan teknologi lama.
3. **Pemisahan Baseline 0 dan Baseline 1 sangat membantu.** Dampak perubahan menjadi transparan dan evaluasi kinerja tidak tercampur.
4. **Pengadaan dan instalasi fisik berjalan baik.** Pemesanan awal dan koordinasi window malam membuat instalasi selesai 16 Maret, jauh sebelum batas 10 April.
5. **Buffer pengujian perlu dijaga.** CR-001 menghabiskan sebagian buffer, sehingga fase SIT/UAT menjadi lebih ketat.
6. **Pelatihan sebaiknya dijadwalkan lebih awal atau modular.** Target 18 April tidak tercapai karena pergeseran jadwal; model dua batch dapat dipertahankan untuk proyek berikutnya.
7. **Data baseline biaya harus konsisten sebelum EVM dijalankan.** Perbaikan baseline cost pada MPP memastikan BAC dan CPI dapat dipercaya.
8. **Dokumentasi perubahan dan closing harus disiapkan paralel dengan eksekusi**, bukan di akhir proyek.

---

## H. Serah Terima dan Sign-Off

### H.1 Serah Terima

Tanggal serah terima: **1 Mei 2026**

Dokumen dan aset yang diserahkan:

- Sistem LUGGIO yang beroperasi (backend, database, dashboard, middleware DCS).
- 6 unit RFID Reader Gate, 5 unit handheld scanner, 5.000 smart tag, printer RFID, server lokal, access point, switch POE, dan kabel.
- Buku panduan operasional dan admin guide.
- Runbook integrasi DCS dan prosedur backup.
- Laporan SIT, UAT, dan integration test.
- Asset list dan informasi garansi vendor.
- Laporan penutupan proyek (dokumen ini).

### H.2 Rekomendasi Pasca-Serah Terima

1. Pantau KPI unreadable rate dan respons dashboard selama 3 bulan pertama.
2. Lakukan backup database sesuai jadwal dan uji restore berkala.
3. Audit kualitas tag RFID dan perangkat reader setiap bulan.
4. Pantau pembaruan protokol DCS dari vendor; uji ulang middleware jika ada perubahan.
5. Berikan refresher training bagi personel baru.
6. Perbarui risk register operasional dan masukkan risiko residual ke proses manajemen layanan.

### H.3 Sign-Off

| Nama | Jabatan | Peran | Tanda tangan | Tanggal |
|---|---|---|---|---|
| Ir. H. Max Verstappen | Direktur Operasional | Project Sponsor |  | 1 Mei 2026 |
| Ir. Primary Putri Ardiva | Kepala Divisi TI | Project Manager |  | 1 Mei 2026 |
| Rusdi | Koordinator Ground Handling & Check-In | User Representative |  | 1 Mei 2026 |
| Muhammad Nabiel Lukman Hakim | System Analyst | Pemeriksa teknis |  | 1 Mei 2026 |
| Muhammad Hasbi Assidiqi | Network/Hardware Engineer | Penyusun |  | 1 Mei 2026 |

---

## Lampiran A — Rumus Earned Value

| Indikator | Rumus |
|---|---|
| CV | EV − AC |
| SV | EV − PV |
| CPI | EV / AC |
| SPI | EV / PV |
| EAC | AC + (BAC − EV) / CPI |
| ETC | EAC − AC |
| VAC | BAC − EAC |
| TCPI | (BAC − EV) / (BAC − AC) |

## Lampiran B — Checklist Deliverable

- [x] Project Charter dan dokumen perencanaan.
- [x] WBS, jadwal, dan baseline.
- [x] Risk register dan laporan mingguan.
- [x] Survei, desain jaringan, dan spesifikasi integrasi.
- [x] Pengadaan dan instalasi hardware.
- [x] Pengembangan software dan dashboard.
- [x] Middleware/adaptor DCS.
- [x] SIT, UAT, dan regresi.
- [x] Pelatihan 50 personel.
- [x] Buku panduan, runbook, dan asset list.
- [x] Closing report dan sign-off.

## Lampiran C — Daftar Dokumen Proyek

1. Project Charter v1.0.
2. WBS dan WBS Dictionary.
3. Jadwal MPP (Baseline 0 dan Baseline 1).
4. Risk Register.
5. Laporan mingguan 1–10.
6. Spesifikasi integrasi dan desain middleware.
7. Laporan SIT dan UAT.
8. Laporan integration test DCS.
9. Buku panduan operasional dan admin guide.
10. Runbook integrasi dan backup.
11. M9 Change Management.
12. M10 Closing Report (dokumen ini).

---

*Dokumen ini merupakan deliverable CP3 Proyek LUGGIO dan disusun berdasarkan data Baseline 0, Baseline 1, serta hasil verifikasi SIT/UAT.*
