# Laporan Work Package Data dan Earned Value (WPD/EVM)

## Proyek LUGGIO — Sistem Pelacakan Bagasi RFID Bandara Indo-Aero

| Item | Keterangan |
|---|---|
| Nomor Dokumen | LUGGIO-CP3-M8-001 |
| Versi | 1.1 |
| Tanggal | 24 Maret 2026 |
| Status | Final |
| Status Date | 20 Maret 2026 |
| Baseline | Baseline 0 (BAC diperbarui setelah CCB 24 Maret 2026) |
| Penyusun | Muhammad Nabiel Lukman Hakim — System Analyst |
| Sumber data | Ir. Primary Putri Ardiva — Project Manager (MS Project) |
| Persetujuan | Ir. Primary Putri Ardiva — Project Manager |
| Dokumen terkait | Project Charter v1.0; MPP LUGGIO; M9 Change Management; M10 Closing Report |

---

> **CATATAN DATA.** Angka pada dokumen ini dihitung pada status date 20 Maret 2026. MPP terbaru (`..._f2f154.xml`) memakai status date **20 April 2026** dengan finish 29 Mei 2026; nilai biaya pada MPP masih tercatat 100× lipat sehingga AC per *work package* belum dapat dipakai. Dokumen ini perlu dihitung ulang setelah AC per *task* dikoreksi.

## 1. Ringkasan Status

Per 20 Maret 2026, proyek berada pada kondisi **on budget, behind schedule**:

| Indikator | Nilai |
|---|---:|
| BAC (work packages) | Rp239.678.233 |
| BAC (total proyek, termasuk fixed cost) | Rp242.678.233 |
| PV | ±Rp149.897.333 |
| EV | Rp122.578.233 |
| AC | Rp122.578.233 |
| CV | Rp0 |
| SV | **−Rp27.319.100** |
| CPI | **1,00** |
| SPI | **0,818** |
| EAC | Rp239.678.233 |
| ETC | Rp117.100.000 |
| VAC | Rp0 |
| TCPI | 1,00 |

Dengan memasukkan fixed cost proyek Rp3.000.000 yang dialokasikan secara proporsional, EV dan AC total proyek adalah **Rp124.388.145**, CPI tetap **1,00**, dan SPI tetap sekitar **0,82**.

Catatan revisi: nilai BAC di atas sudah memasukkan penambahan **01/CR/2026 (Middleware API DCS, +Rp15.000.000)** dan **02/CR/2026 (Validasi dan Retry RFID, +Rp8.000.000)** yang disetujui CCB pada 24 Maret 2026, sesuai keputusan evaluasi ulang EV setelah CCB. Tanggal selesai baseline tidak berubah, sehingga PV, EV, AC, SV, dan SPI tidak berubah; yang berubah hanya BAC, EAC, ETC, dan TCPI.

Kesimpulan singkat: biaya berjalan sesuai anggaran, tetapi pekerjaan tertinggal dari jadwal terutama karena fase instalasi fisik (1.5) belum dimulai dan fase pengembangan software (1.4) baru mencapai sekitar 50%. Keterlambatan ini masih dapat dipulihkan karena instalasi fisik memiliki kelonggaran dan fase pengujian baru dimulai awal April.

---

## 2. Metode dan Sumber Data

### 2.1 Metode

Dokumen ini menggunakan **Earned Value Management (EVM)** dengan rumus:

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

### 2.2 Sumber Data

- **MS Project** file `M8_PROGRESS.mpp`, status date 20 Maret 2026.
- Baseline 0: 9 Februari–24 April 2026, 53 hari kerja (tanggal tidak berubah setelah dua CR).
- BAC diperbarui setelah CCB 24 Maret 2026: +Rp15.000.000 (01/CR/2026) dan +Rp8.000.000 (02/CR/2026).
- % Complete: 1.1–1.3 = 100%; 1.4 = 50% untuk task yang telah dimulai; 1.5–1.7 = 0%.
- Actual cost: mengikuti biaya rencana untuk pekerjaan yang telah dimulai; tidak ada varians biaya pada status date.
- PV dihitung dari distribusi baseline per task. Angka PV dapat berbeda tipis dari tabel MS Project karena pembulatan dan alokasi fixed cost; angka final untuk laporan adalah angka yang muncul di **Project → Statistics** dan tabel **Earned Value**.

---

## 3. Work Package Data (WPD)

Nilai dalam **Rp juta**.

### 3.1 Kinerja Biaya per Work Package

| Kode | Work Package | BAC | EV | AC | CV | % Complete | Status |
|---|---|---:|---:|---:|---:|---:|---|
| 1.1 | Manajemen Proyek | 12,48 | 12,48 | 12,48 | 0 | 100% | Selesai |
| 1.2 | Survei & Perencanaan | 13,32 | 13,32 | 13,32 | 0 | 100% | Selesai |
| 1.3 | Pengadaan Hardware | 75,06 | 75,06 | 75,06 | 0 | 100% | Selesai |
| 1.4 | Pengembangan Software | 72,04 | 21,72 | 21,72 | 0 | ±34% | Berjalan |
| 1.5 | Instalasi & Konfigurasi | 11,68 | 0 | 0 | 0 | 0% | Belum mulai |
| 1.6 | Pengujian, Pelatihan & Penutupan | 41,60 | 0 | 0 | 0 | 0% | Belum mulai |
| 1.7 | Contingency Reserve | 13,50 | 0 | 0 | 0 | 0% | Reserve |
| **Total WPD** | | **239,68** | **122,58** | **122,58** | **0** | **51,1%** | |
| — | Fixed cost proyek (alokasi) | 3,00 | 1,81 | 1,81 | 0 | ±60,3% | |
| **Total proyek** | | **242,68** | **124,39** | **124,39** | **0** | **51%** | |

Catatan: % Complete 1.4 adalah 50% untuk task yang sudah dimulai (1.4.1–1.4.4); task 1.4.5–1.4.8 belum mulai sehingga ringkasan biaya 1.4 sekitar 30%. Angka % proyek 51% adalah pembulatan dari perhitungan MS Project. BAC 1.4 sudah mencakup 1.4.7 (Rp15.000.000) dan 1.4.8 (Rp8.000.000).

### 3.2 Kinerja Jadwal per Work Package

| Kode | Work Package | PV | EV | SV | Status jadwal |
|---|---|---:|---:|---:|---|
| 1.1 | Manajemen Proyek | 8,64 | 12,48 | +3,84 | Laporan mingguan 1–10 diasumsikan selesai pada status date |
| 1.2 | Survei & Perencanaan | 13,32 | 13,32 | 0 | Sesuai jadwal |
| 1.3 | Pengadaan Hardware | 75,06 | 75,06 | 0 | Sesuai jadwal |
| 1.4 | Pengembangan Software | 33,81 | 21,72 | −12,09 | Berjalan; 1.4.5–1.4.8 belum mulai |
| 1.5 | Instalasi & Konfigurasi | 11,68 | 0 | −11,68 | Terlambat; rencana selesai 16 Mar |
| 1.6 | Pengujian, Pelatihan & Penutupan | 0 | 0 | 0 | Belum masuk periode PV |
| 1.7 | Contingency Reserve | 7,39 | 0 | −7,39 | Reserve belum digunakan |
| **Total WPD** | | **149,90** | **122,58** | **−27,32** | **Tertinggal** |

`SPI = 122,58 / 149,90 = 0,818`.

---

## 4. Analisis Varians Biaya

1. **CV = Rp0** dan **CPI = 1,00** menunjukkan bahwa biaya aktual sama dengan nilai pekerjaan yang diperoleh. Tidak ada pembengkakan biaya pada status date.
2. Seluruh work package yang telah selesai (1.1–1.3) memiliki EV = AC. Pekerjaan 1.4 yang berjalan juga memiliki EV = AC karena actual cost diisi proporsional terhadap progress.
3. Contingency reserve Rp13,50 juta belum digunakan. Perubahan biaya yang disetujui CCB (01/CR/2026 dan 02/CR/2026, total Rp23,00 juta) dibiayai dari *management reserve* dan sudah masuk BAC, sehingga tidak menimbulkan varians terhadap anggaran.
4. Fixed cost proyek Rp3,00 juta dialokasikan proporsional terhadap progress; kontribusinya sekitar Rp1,81 juta pada EV/AC.
5. Karena CPI = 1,00, **EAC = BAC** dan **VAC = Rp0** untuk pekerjaan dasar (EAC Rp239,68 juta untuk work packages atau Rp242,68 juta termasuk fixed cost).

---

## 5. Analisis Varians Jadwal

1. **SV = −Rp27,32 juta** dan **SPI = 0,818** menunjukkan proyek tertinggal sekitar 18% dari nilai pekerjaan yang seharusnya sudah diselesaikan.
2. Penyebab utama:
   - **1.5 Instalasi & Konfigurasi** seharusnya selesai 16 Maret, tetapi belum dimulai (SV −Rp11,68 juta).
   - **1.4 Pengembangan Software** baru sekitar 50%; task 1.4.5 dan 1.4.6 belum mulai (SV −Rp12,09 juta).
   - **1.7 Contingency Reserve** memiliki PV Rp7,39 juta tetapi belum digunakan; ini bukan pekerjaan fisik, sehingga sebagian SV berasal dari cara reserve dijadwalkan.
3. **1.1 Manajemen Proyek** memiliki SV positif karena laporan mingguan 1–10 diasumsikan selesai pada status date; ini bukan percepatan pekerjaan teknis.
4. **1.6 Pengujian** belum masuk periode PV karena baru dijadwalkan mulai 2 April. Keterlambatan 1.5 dan 1.4 harus dipulihkan sebelum tanggal tersebut agar SIT tidak ikut mundur.
5. **Jalur kritis** proyek berada di pengembangan software dan pengujian. Instalasi fisik (1.5) memiliki kelonggaran 13–19 hari, sehingga keterlambatan 1.5 belum tentu menggeser finish proyek jika diselesaikan sebelum April. Namun, jika 1.5 melewati kelonggaran tersebut, fase pengujian dan penutupan akan terdampak.

---

## 6. Forecast dan To-Complete Performance

| Indikator | Nilai | Interpretasi |
|---|---:|---|
| EAC | Rp239.678.233 | Proyeksi biaya akhir sama dengan BAC (setelah dua CR) jika CPI bertahan 1,00. |
| ETC | Rp117.100.000 | Biaya untuk menyelesaikan sisa pekerjaan, termasuk dua *work package* perubahan. |
| VAC | Rp0 | Tidak ada proyeksi over/under budget untuk pekerjaan dasar. |
| TCPI | 1,00 | Sisa pekerjaan dapat diselesaikan dengan efisiensi biaya yang sama. |

Risiko utama bukan biaya, melainkan **jadwal**. Jika keterlambatan 1.5 dan 1.4 berlanjut, proyek dapat melewati 24 April 2026. Karena itu, tindakan percepatan dan monitoring mingguan diperlukan.

---

## 7. Interpretasi S-Curve

> **[Placeholder: tempel screenshot Earned Value Over Time / S-Curve dari MS Project di sini.]**

Interpretasi yang diharapkan:

1. Kurva **PV** berada di atas kurva **EV** sejak pertengahan Maret, menunjukkan keterlambatan kumulatif.
2. Selisih PV–EV sekitar **Rp27,3 juta** pada status date.
3. Kurva **AC** mengikuti EV karena CPI = 1,00; tidak ada biaya berlebih.
4. Jika percepatan 1.5 dan 1.4 berhasil, kurva EV akan mengejar PV pada April. Jika tidak, gap akan melebar dan finish proyek bergeser.
5. Perhatikan titik mulai 1.6 (2 April): keterlambatan yang belum dipulihkan sebelum tanggal itu akan langsung mengurangi waktu pengujian.

---

## 8. Corrective Actions dan Rekomendasi

| No | Tindakan | PIC | Target | Alasan |
|---|---|---|---|---|
| 1 | Percepat instalasi fisik 1.5 (tambah tim/lembur, koordinasi window malam) | Network/Hardware Engineer | 27 Maret 2026 | 1.5 belum mulai dan sudah melewati rencana 16 Maret |
| 2 | Siapkan test script, environment, dan data uji SIT secara paralel | QA/Tester | 31 Maret 2026 | Agar 1.6 tidak menunggu 1.5/1.4 selesai |
| 3 | Monitor 1.4.1–1.4.6; pastikan 1.4.5 dan 1.4.6 mulai sesuai jadwal | System Analyst/Developer | Mingguan | 1.4 baru 50%; 1.4.5–1.4.6 belum mulai |
| 4 | Review EVM setiap minggu dan update % Complete aktual | Project Manager | Mingguan | Menjaga akurasi CPI/SPI |
| 5 | Review keputusan CCB atas 01/CR/2026 dan 02/CR/2026 | System Analyst/CCB | 24 Maret 2026 | Risiko integrasi DCS dan kegagalan baca RFID perlu keputusan sebelum SIT |
| 6 | Jika 1.5 melewati 31 Maret, lakukan schedule compression/fast-tracking | Project Manager | Kondisional | Menjaga finish 24 April 2026 |

---

## 9. Kesimpulan

1. **Biaya:** proyek on budget; CPI 1,00; CV Rp0; EAC = BAC = Rp239.678.233 (work packages) atau Rp242.678.233 termasuk fixed cost, sudah mencakup dua CR.
2. **Jadwal:** proyek tertinggal; SPI 0,818; SV −Rp27,32 juta. Penyebab utama adalah 1.5 yang belum mulai dan 1.4 yang baru 50%.
3. **Risiko:** keterlambatan masih dapat dipulihkan karena 1.5 memiliki float dan 1.6 belum dimulai. Namun, waktu pemulihan terbatas sampai awal April.
4. **Tindakan:** percepat 1.5, siapkan pengujian secara paralel, monitor 1.4, dan jalankan 1.4.7/1.4.8 secara paralel sesuai keputusan CCB.
5. **Proyeksi:** jika tindakan dilakukan, biaya akhir tetap di bawah pagu Charter (Rp242.678.233 dari Rp285.000.000) dan jadwal dapat kembali ke 24 April 2026. Jika tidak, finish proyek berpotensi mundur.

---

## Lampiran A — Checklist Data M8

- [x] Baseline 0 tersedia dan tidak diubah.
- [x] Status date 20 Maret 2026.
- [x] % Complete per work package diisi.
- [x] Actual cost diisi untuk pekerjaan yang berjalan.
- [x] Tabel Earned Value tersedia.
- [x] S-Curve/Earned Value Over Time tersedia.
- [x] Analisis CPI/SPI dan corrective actions disusun.

## Lampiran B — Placeholder Screenshot

> **[Placeholder 1: Screenshot tabel Earned Value dari MS Project.]**

> **[Placeholder 2: Screenshot Earned Value Over Time / S-Curve.]**

> **[Placeholder 3: Screenshot Gantt dengan % Complete dan status date 20 Maret 2026.]**

---

*Dokumen ini merupakan deliverable CP3 Proyek LUGGIO. Angka PV merupakan estimasi dari distribusi baseline; angka final mengikuti tabel Earned Value MS Project.*
