# Risk Register Proyek LUGGIO

## Proyek LUGGIO — Sistem Pelacakan Bagasi RFID Bandara Indo-Aero

| Item | Keterangan |
|---|---|
| Nomor Dokumen | LUGGIO-CP3-RR-001 |
| Versi | 1.0 |
| Tanggal | 24 April 2026 |
| Status | Final — ringkasan untuk CP3 |
| Proyek | LUGGIO: Sistem Pelacakan Bagasi RFID Bandara Indo-Aero |
| Penyusun | Muhammad Hasbi Assidiqi — Network/Hardware Engineer |
| Persetujuan | Ir. Primary Putri Ardiva — Project Manager |
| Catatan | Register ini disusun dari data proyek dan catatan rapat. Jika tersedia file Risk Register asli, gunakan file tersebut sebagai lampiran utama dan dokumen ini sebagai ringkasan. |

---

## 1. Tujuan

Dokumen ini mencatat risiko proyek, skor risiko, respons, pemilik, dan status akhir. Register digunakan sebagai lampiran **M10 Closing Report** dan menjadi dasar evaluasi risiko residual setelah serah terima.

---

## 2. Skala Penilaian

| Skor | Probabilitas (P) | Dampak (I) |
|---|---|---|
| 1 | Sangat rendah | Sangat rendah |
| 2 | Rendah | Rendah |
| 3 | Sedang | Sedang |
| 4 | Tinggi | Tinggi |
| 5 | Sangat tinggi | Sangat tinggi |

**Skor risiko = P × I.** Prioritas: 1–4 rendah, 5–9 sedang, 10–16 tinggi, 17–25 sangat tinggi.

---

## 3. Risk Register

### 3.1 Identifikasi dan Penilaian Risiko

| ID | Risiko | Kategori | Penyebab dan dampak | P | I | Skor |
|---|---|---|---:|---:|---:|
| R-01 | Keterlambatan pengadaan hardware | Supply | Lead time vendor dan jumlah unit banyak; instalasi mundur | 3 | 4 | 12 |
| R-02 | Ketidakcocokan protokol DCS | Teknis | DCS legacy dan format pesan berbeda; integrasi gagal, FR-10 tidak terpenuhi | 4 | 5 | 20 |
| R-03 | Window instalasi malam terbatas | Operasional | Operasi bandara 24 jam; instalasi tertunda | 3 | 3 | 9 |
| R-04 | Read rate RFID rendah | Kualitas | Penempatan tag/reader tidak optimal; unreadable rate >0,5% | 3 | 4 | 12 |
| R-05 | Wi-Fi dead spot di apron | Teknis | Cakupan AP terbatas; handheld tidak sinkron | 3 | 3 | 9 |
| R-06 | Ketersediaan staf untuk pelatihan | Resource | Shift operasional dan jadwal padat; KPI-04 terlambat | 3 | 3 | 9 |
| R-07 | Perubahan lingkup | Scope | Kebutuhan integrasi baru; biaya/jadwal bertambah | 3 | 3 | 9 |
| R-08 | Cuaca saat instalasi outdoor | Eksternal | Hujan/angin; instalasi tertunda | 2 | 3 | 6 |
| R-09 | Pembaruan protokol DCS dari vendor | Teknis | Vendor mengubah versi/protokol; middleware perlu penyesuaian | 2 | 4 | 8 |

### 3.2 Respons, Pemilik, Status, dan Residual

| ID | Respons | Owner | Status | Residual |
|---|---|---|---|---|
| R-01 | Pemesanan awal, monitoring vendor, buffer pengiriman | PM | Closed | Rendah |
| R-02 | 01/CR/2026 Middleware API DCS, contract test, simulator | System Analyst | Closed | Rendah |
| R-03 | Koordinasi slot, tim siaga, pekerjaan per zona | Network Engineer | Closed | Rendah |
| R-04 | Site survey, penempatan tag, pilot, kalibrasi, 02/CR/2026 validasi & retry | QA/Network | Closed | Rendah |
| R-05 | AP outdoor, survey coverage, uji roaming | Network Engineer | Closed | Rendah |
| R-06 | Pelatihan dua batch, jadwal shift, refresher | PM | Residual | Sedang |
| R-07 | CCB, 01/CR/2026 dan 02/CR/2026, pembaruan BAC | PM | Closed | Rendah |
| R-08 | Penjadwalan fleksibel, pekerjaan dalam ruang | Network Engineer | Closed | Rendah |
| R-09 | Monitoring vendor, regression test, documented interface | System Analyst | Open — monitoring | Sedang |

---

## 4. Ringkasan Respons

| ID | Tipe respons | Ringkasan tindakan |
|---|---|---|
| R-01 | Mitigasi | Pemesanan awal, vendor monitoring, buffer jadwal. |
| R-02 | Mitigasi | 01/CR/2026 Middleware API DCS, contract test, integration test dengan simulator. |
| R-03 | Mitigasi | Koordinasi window malam dan tim siaga. |
| R-04 | Mitigasi | Survey, penempatan tag, pilot, kalibrasi reader, dan 02/CR/2026 (validasi + retry otomatis). |
| R-05 | Mitigasi | Penambahan AP outdoor dan uji coverage. |
| R-06 | Mitigasi + acceptance | Dua batch pelatihan; sisa risiko diterima dan dimonitor. |
| R-07 | Mitigasi | CCB dan baseline 1. |
| R-08 | Mitigasi | Jadwal fleksibel dan pekerjaan indoor. |
| R-09 | Monitoring | Pantau pembaruan vendor; uji regresi jika ada perubahan. |

---

## 5. Risiko Residual dan Monitoring

1. **R-06 Ketersediaan staf pelatihan** — residual sedang. Tindakan: refresher training dan pendampingan personel baru.
2. **R-09 Pembaruan protokol DCS** — residual sedang. Tindakan: monitoring vendor, dokumentasi antarmuka, regression test berkala.
3. **Kualitas tag RFID** — risiko operasional jangka panjang. Tindakan: audit tag dan reader setiap bulan.
4. **Adopsi pengguna** — risiko perubahan proses. Tindakan: monitoring KPI dan umpan balik pengguna selama 3 bulan.

---

## 6. Review

Risk register ditinjau pada rapat mingguan proyek dan pada saat CCB. Setelah proyek ditutup, risiko residual diserahkan kepada Divisi TI Bandara Indo-Aero untuk dipantau dalam proses manajemen layanan.

---

*Dokumen ini merupakan lampiran CP3 Proyek LUGGIO dan disusun berdasarkan data proyek, notulen CCB, serta hasil SIT/UAT.*
