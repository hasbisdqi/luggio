# Laporan Penutupan Proyek (Closing Report)

## Proyek LUGGIO — Sistem Pelacakan Bagasi RFID Bandara Indo-Aero

| Item | Keterangan |
|---|---|
| Nomor Dokumen | LUGGIO-CP3-M10-001 |
| Versi | 1.0 |
| Tanggal | 24 April 2026 |
| Status | Final |
| Proyek | LUGGIO: Sistem Pelacakan Bagasi RFID Bandara Indo-Aero |
| Baseline | Baseline 0 — 24 April 2026, 53 hari (BAC diperbarui menjadi Rp242.678.233 setelah dua CR) |
| Penyusun | Muhammad Hasbi Assidiqi — Network/Hardware Engineer |
| Pemeriksa | Muhammad Nabiel Lukman Hakim — System Analyst |
| Persetujuan | Ir. Primary Putri Ardiva — Project Manager |
| Persetujuan | Ir. H. Max Verstappen — Project Sponsor |
| Penerimaan | Rusdi — User Representative |
| Dokumen terkait | Project Charter v1.0; MPP LUGGIO; M9 Change Management; Risk Register |

---

## A. Ringkasan Eksekutif

Proyek LUGGIO telah selesai dan diserahterimakan pada **24 April 2026**, sesuai tanggal selesai Baseline 0. Sistem pelacakan bagasi berbasis RFID telah terpasang, terintegrasi dengan DCS melalui middleware, dilengkapi validasi dan retry pembacaan RFID, diuji melalui SIT/UAT, dan digunakan oleh staf operasional bandara.

Selama pelaksanaan terdapat dua perubahan yang disetujui CCB pada 24 Maret 2026, yaitu **01/CR/2026: Pengembangan Middleware API DCS** dan **02/CR/2026: Pengembangan Validasi dan Retry RFID**. Keduanya dikerjakan secara paralel sehingga **tanggal selesai proyek tidak berubah**, tetapi menambah biaya Rp23.000.000 ke dalam BAC.

| Indikator | Baseline 0 (awal) | Setelah 2 CR | Realisasi |
|---|---:|---:|---:|
| Tanggal selesai | 24 April 2026 | 24 April 2026 | **24 April 2026** |
| Durasi | 53 hari | 53 hari | **53 hari** |
| BAC | Rp219.678.233 | Rp242.678.233 | **Rp242.678.233** |
| EV | — | — | **Rp242.678.233** |
| AC | — | — | **Rp242.678.233** |
| CPI | — | — | **1,00** |
| VAC | — | — | **Rp0** |

Kinerja biaya berada di bawah pagu Charter Rp285.000.000 (sisa Rp42.321.767) dan tidak ada *cost overrun*: CPI akhir 1,00 karena seluruh biaya yang dikeluarkan adalah biaya yang dianggarkan, termasuk biaya dua CR yang disetujui. Seluruh *deliverable* utama telah diterima dan seluruh KPI terpenuhi sebelum penutupan.

---

## B. Verifikasi Lingkup dan Deliverable

### B.1 Lingkup yang Diserahkan

| Kelompok | Deliverable | Rencana | Realisasi | Status |
|---|---|---|---|---|
| Manajemen proyek | Charter, WBS, jadwal, risk register, laporan mingguan 1–10, closing report | Feb–Apr 2026 | Selesai | Diterima |
| Survei & desain | Survei titik pemasangan, peta jaringan, spesifikasi integrasi DCS | Feb 2026 | Selesai | Diterima |
| Hardware | 6 unit RFID Reader Gate, 5 unit handheld scanner, 5.000 smart tag, printer RFID, server lokal, access point outdoor, switch POE, kabel Cat6 | Mar 2026 | Terpasang/terpasang | Diterima |
| Software | Backend, database, dashboard web, RBAC, alert, laporan, backup, sinkronisasi offline, validasi & retry RFID | Feb–Apr 2026 | Selesai | Diterima |
| Integrasi | Middleware API DCS, integrasi display carousel | Apr 2026 | Selesai | Diterima |
| Instalasi fisik | Gerbang RFID, UPS, kabel data, access point | Mar 2026 | Selesai | Diterima |
| Pengujian | SIT, UAT, simulasi bagasi nyasar, regresi | Apr 2026 | Selesai | Diterima |
| Pelatihan | Pelatihan 50 personel ground handling dan check-in | Apr 2026 | Selesai | Diterima |
| Serah terima | Buku panduan operasional, admin guide, runbook, asset list | Apr 2026 | Selesai | Diterima |

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
| Pagu biaya | ≤Rp285.000.000 | Rp242.678.233 |

### B.3 Perubahan Lingkup

Perubahan lingkup yang disetujui terdiri atas **01/CR/2026** (Middleware API DCS, WBS 1.4.7) dan **02/CR/2026** (Validasi dan Retry RFID, WBS 1.4.8). Tidak ada pekerjaan di luar *out of scope* Charter, tidak ada pengurangan *deliverable*, dan tidak ada perubahan pada conveyor belt maupun aplikasi mobile penumpang.

---

## C. Kinerja Jadwal

### C.1 Ringkasan Jadwal

| Item | Baseline 0 | Setelah 2 CR | Aktual |
|---|---|---|---|
| Mulai | 9 Februari 2026 | 9 Februari 2026 | 9 Februari 2026 |
| Selesai | 24 April 2026 | 24 April 2026 | **24 April 2026** |
| Durasi | 53 hari | 53 hari | **53 hari** |
| Variance | — | 0 hari | **0 hari** |

### C.2 Milestone

| Milestone | Baseline 0 | Aktual | Status |
|---|---|---|---|
| M1 — Kebutuhan dan desain disetujui | 25 Feb 2026 | 25 Feb 2026 | Tercapai |
| M2 — Pengadaan selesai | 6 Mar 2026 | 6 Mar 2026 | Tercapai |
| M3 — Instalasi fisik selesai | 16 Mar 2026 | 16 Mar 2026 | Tercapai |
| M4 — Sistem siap operasional | 24 Apr 2026 | 24 Apr 2026 | Tercapai |

### C.3 Analisis Jalur Kritis

Jalur kritis proyek berada pada rangkaian pengembangan software dan pengujian:

**1.4.6 → 1.6.1/1.6.2 → 1.6.3 → 1.6.4 → 1.6.5 → 1.6.6**

Task tambahan **1.4.7 (Middleware API DCS)** dan **1.4.8 (Validasi dan Retry RFID)** dijadwalkan paralel pada 2–8 April 2026, di dalam *float* fase pengembangan, sehingga tidak menambah panjang jalur kritis. Pekerjaan pengadaan dan instalasi fisik memiliki kelonggaran 13–19 hari dan tidak menjadi penentu tanggal akhir.

### C.4 Varians Jadwal

- Variance tanggal selesai: **0 hari**; proyek selesai 24 April 2026 sesuai baseline.
- SPI saat selesai: **1,00**, karena seluruh lingkup (termasuk dua *work package* tambahan) telah diselesaikan pada tanggal rencana.
- Risiko beban kerja pada 2–9 April dimitigasi dengan monitoring harian dan kesiapan *fast-tracking*, dan tidak berdampak pada milestone M4.

---

## D. Kinerja Biaya

### D.1 Ringkasan Earned Value

| Indikator | Nilai |
|---|---:|
| BAC (Baseline 0 setelah dua CR) | Rp242.678.233 |
| EV | Rp242.678.233 |
| AC | Rp242.678.233 |
| CV | **Rp0** |
| CPI | **1,00** |
| EAC | **Rp242.678.233** |
| ETC | Rp0 |
| VAC | **Rp0** |
| TCPI | 1,00 |

### D.2 Rincian Biaya per Fase

| WBS | Fase | Baseline 0 (awal) | 01/CR/2026 | 02/CR/2026 | Final |
|---|---|---:|---:|---:|---:|
| 1.1 | Manajemen Proyek | Rp12.480.000 | — | — | Rp12.480.000 |
| 1.2 | Survei & Perencanaan | Rp13.320.000 | — | — | Rp13.320.000 |
| 1.3 | Pengadaan Hardware | Rp75.058.233 | — | — | Rp75.058.233 |
| 1.4 | Pengembangan Software | Rp49.040.000 | Rp15.000.000 | Rp8.000.000 | Rp72.040.000 |
| 1.5 | Instalasi & Konfigurasi | Rp11.680.000 | — | — | Rp11.680.000 |
| 1.6 | Pengujian, Pelatihan & Penutupan | Rp41.600.000 | — | — | Rp41.600.000 |
| 1.7 | Contingency Reserve | Rp13.500.000 | — | — | Rp13.500.000 |
| — | Fixed cost proyek | Rp3.000.000 | — | — | Rp3.000.000 |
| **Total** | | **Rp219.678.233** | **Rp15.000.000** | **Rp8.000.000** | **Rp242.678.233** |

### D.3 Analisis Varians Biaya

1. **CPI 1,00** dan **CV Rp0** menunjukkan seluruh pekerjaan (termasuk dua *work package* perubahan) diselesaikan sesuai anggaran yang telah diperbarui; tidak ada pekerjaan yang melebihi anggarannya.
2. Tanpa dua CR, BAC tetap Rp219.678.233. Kedua CR menambah Rp23.000.000 yang **sudah dianggarkan** melalui update BAC pada 25 Maret 2026, bukan biaya di luar rencana.
3. **Contingency reserve Rp13.500.000 tetap tercatat sebagai bagian BAC** dan tidak ditarik. Kedua CR dibiayai dari *management reserve* di dalam pagu Charter; tidak ada penggunaan contingency reserve.
4. Pagu Charter Rp285.000.000 tidak terlampaui. Sisa pagu setelah proyek adalah **Rp42.321.767**.
5. EAC sama dengan AC karena seluruh pekerjaan telah selesai (ETC = 0). VAC Rp0 menunjukkan proyek selesai tepat pada BAC final.

---

## E. Kualitas, Risiko, dan KPI

### E.1 Hasil KPI

| KPI | Target | Hasil | Status |
|---|---|---|---|
| KPI-01 — Unreadable rate | <5% | **0,42%** | Tercapai |
| KPI-02 — Respons dashboard | <3 detik | **1,8 detik** | Tercapai |
| KPI-03 — Instalasi fisik | 6 gate + 5 handheld aktif sebelum 10 Apr 2026 | **16 Mar 2026** | Tercapai |
| KPI-04 — Kesiapan SDM | 50 personel lulus pelatihan pada 18 Apr 2026 | **50 personel selesai 21 Apr 2026** | Terlambat 3 hari; terpenuhi sebelum closing |
| KPI-05 — Efisiensi biaya | ≤Rp285.000.000 | **Rp242.678.233** | Tercapai |

Catatan KPI-04: karena 1.4.7 dan 1.4.8 dikerjakan paralel, pelatihan tetap dijadwalkan 16–21 April 2026. Pelatihan selesai 21 April 2026, tiga hari setelah target 18 April, namun seluruh 50 personel lulus sebelum penutupan proyek 24 April 2026.

### E.2 Kualitas Pengujian

| Aktivitas | Hasil |
|---|---|
| Unit test modul utama | 100% test case lulus |
| Integration test DCS | 12/12 skenario lulus |
| Simulasi gagal baca RFID dan retry | 6/6 skenario lulus; read success rate 99,7% |
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
| R-02 | 01/CR/2026 Middleware API DCS, contract test, simulator |
| R-03 | Koordinasi slot, tim siaga, pekerjaan per zona |
| R-04 | Site survey, penempatan tag, pilot, kalibrasi, 02/CR/2026 validasi dan retry |
| R-05 | AP outdoor, survey coverage, uji roaming |
| R-06 | Pelatihan dua batch, jadwal shift, refresher |
| R-07 | CCB, 01/CR/2026 dan 02/CR/2026, pembaruan BAC |
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

| Item | 01/CR/2026 | 02/CR/2026 |
|---|---|---|
| Nama Pengajuan | Pengembangan Middleware API DCS | Pengembangan Validasi dan Retry RFID |
| Tanggal pengajuan | 18 Maret 2026 | 21 Maret 2026 |
| Keputusan CCB | Disetujui, 24 Maret 2026 | Disetujui, 24 Maret 2026 |
| Tipe CR / Prioritas | Corrective Action / High | Corrective Action / Medium |
| Dampak biaya | +Rp15.000.000 | +Rp8.000.000 |
| Dampak jadwal | 0 hari (dikerjakan paralel) | 0 hari (dikerjakan paralel) |
| Status | Closed 24 April 2026 | Closed 24 April 2026 |
| **Total** | **+Rp23.000.000; BAC Rp219.678.233 → Rp242.678.233; tanggal selesai tetap 24 April 2026** | |

Kedua CR tidak mengurangi lingkup, tidak mengubah pagu Charter, dan tidak menggunakan contingency reserve. Detail analisis dampak, notulen CCB, dan log perubahan tersedia dalam dokumen **M9 — Laporan Manajemen Perubahan**.

---

## G. Lessons Learned

1. **Validasi antarmuka eksternal harus dilakukan sebelum baseline disetujui.** Protokol DCS yang legacy seharusnya teridentifikasi pada tahap perencanaan, bukan saat desain integrasi.
2. **Middleware perlu dimasukkan sebagai pekerjaan eksplisit dalam WBS** ketika sistem eksternal menggunakan teknologi lama.
3. **Update BAC tanpa menggeser tanggal memberi gambaran biaya yang jujur.** Perubahan tercatat sebagai tambahan BAC, sehingga CPI tetap mencerminkan realisasi.
4. **Pengadaan dan instalasi fisik berjalan baik.** Pemesanan awal dan koordinasi window malam membuat instalasi selesai 16 Maret, jauh sebelum batas 10 April.
5. **Kerja paralel efektif, tetapi membebani tim.** 1.4.7 dan 1.4.8 berhasil diserap tanpa menggeser jadwal; beban pada 2–9 April perlu diantisipasi lebih awal.
6. **Pelatihan sebaiknya dijadwalkan lebih awal atau modular.** Target 18 April baru tercapai 21 April; model dua batch dapat dipertahankan untuk proyek berikutnya.
7. **Pengujian perangkat RFID di lapangan perlu dilakukan sebelum baseline disetujui** agar kebutuhan validasi/retry tidak muncul di tengah pelaksanaan.
8. **Dokumentasi perubahan dan closing harus disiapkan paralel dengan eksekusi**, bukan di akhir proyek.

---

## H. Serah Terima dan Sign-Off

### H.1 Serah Terima

Tanggal serah terima: **24 April 2026**

Dokumen dan aset yang diserahkan:

- Sistem LUGGIO yang beroperasi (backend, database, dashboard, middleware DCS, modul validasi & retry RFID).
- 6 unit RFID Reader Gate, 5 unit handheld scanner, 5.000 smart tag, printer RFID, server lokal, access point, switch POE, dan kabel.
- Buku panduan operasional dan admin guide.
- Runbook integrasi DCS dan prosedur backup.
- Aturan validasi, konfigurasi retry RFID, dan laporan *read success rate*.
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
| Ir. H. Max Verstappen | Direktur Operasional | Project Sponsor |  | 24 April 2026 |
| Ir. Primary Putri Ardiva | Kepala Divisi TI | Project Manager |  | 24 April 2026 |
| Rusdi | Koordinator Ground Handling & Check-In | User Representative |  | 24 April 2026 |
| Muhammad Nabiel Lukman Hakim | System Analyst | Pemeriksa teknis |  | 24 April 2026 |
| Muhammad Hasbi Assidiqi | Network/Hardware Engineer | Penyusun |  | 24 April 2026 |

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
- [x] Middleware API DCS dan modul validasi/retry RFID.
- [x] SIT, UAT, dan regresi.
- [x] Pelatihan 50 personel.
- [x] Buku panduan, runbook, dan asset list.
- [x] Closing report dan sign-off.

## Lampiran C — Daftar Dokumen Proyek

1. Project Charter v1.0.
2. WBS dan WBS Dictionary.
3. Jadwal MPP (Baseline 0 dengan BAC yang telah diperbarui).
4. Risk Register.
5. Laporan mingguan 1–10.
6. Spesifikasi integrasi dan desain middleware.
7. Laporan SIT dan UAT.
8. Laporan integration test DCS dan pengujian gagal baca/retry RFID.
9. Buku panduan operasional dan admin guide.
10. Runbook integrasi dan backup.
11. M9 Change Management.
12. M10 Closing Report (dokumen ini).

---

*Dokumen ini merupakan deliverable CP3 Proyek LUGGIO dan disusun berdasarkan data Baseline 0 (BAC diperbarui setelah 01/CR/2026 dan 02/CR/2026) serta hasil verifikasi SIT/UAT.*
