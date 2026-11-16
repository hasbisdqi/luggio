# Penjelasan Jalur Kritis (Critical Path Method)
## Proyek Implementasi RFID Pelacakan Bagasi Bandara Indo-Aero

Dokumen ini menyajikan penjelasan naratif dan teknis mengenai **Jalur Kritis (*Critical Path*)** pada Proyek Implementasi Sistem RFID Pelacakan Bagasi Bandara Indo-Aero berdasarkan keselarasan data antara jadwal Microsoft Project ([Projek Akhir MPTI_RFID pelacakan bagasi bandara.mpp](file:///c:/Users/administratorr/Desktop/semester%205/praktikum%20mpti/project%20akhir/luggio/Projek%20Akhir%20MPTI_RFID%20pelacakan%20bagasi%20bandara.mpp)) dan diagram jaringan kerja ([AON.xml](file:///c:/Users/administratorr/Desktop/semester%205/praktikum%20mpti/project%20akhir/luggio/AON.xml)).

---

## 1. Rangkaian Jalur Kritis dari Aktivitas A Sampai U

Rangkaian jalur kritis pada proyek ini diawali dari Aktivitas A (Dokumen Project Charter dan Rencana Proyek) selama 3 hari, yang menjadi prasyarat untuk memulai Aktivitas B (Survei Titik Pemasangan dan Peta Jalur Conveyor) selama 5 hari. Setelah hasil survei diperoleh, proyek dilanjutkan ke Aktivitas D (Spesifikasi Integrasi API dan DCS Penerbangan) selama 4 hari, yang kemudian membuka gerbang pengerjaan logika utama sistem pada Aktivitas I (Engine Pelacakan Real-Time dan Deteksi Rute Salah) selama 16 hari. Dari Aktivitas I, alur kritis terbagi menjadi dua cabang paralel yang berjalan serentak. 

Cabang pertama berfokus pada pengembangan antarmuka melalui Aktivitas J (Dashboard Visual dan Manajemen Hak Akses) selama 14 hari yang langsung diteruskan ke Aktivitas R (Laporan Pengujian Sistem Terintegrasi atau SIT) selama 5 hari. Di saat yang sama, cabang kedua mengembangkan fungsionalitas lapangan yang mencakup Aktivitas K (Aplikasi Handheld Scanner Mode Offline) selama 6 hari, Aktivitas L (Fitur Notifikasi Layar Carousel Kedatangan) selama 3 hari, Aktivitas M (Fitur Ekspor Laporan Statistik, Log, dan Backup) selama 4 hari, serta Aktivitas Q (Pengujian Seluruh Modul Sistem RFID) selama 6 hari. 

Kedua cabang paralel ini kemudian menyatu kembali pada tahap akhir proyek, yaitu Aktivitas S (Laporan User Acceptance Test dan Simulasi Bagasi Nyasar) selama 4 hari, dilanjutkan dengan Aktivitas T (Pelatihan Staf Ground Handling dan Check-in) selama 3 hari, dan diakhiri oleh Aktivitas U (Dokumen Laporan Akhir dan Serah Terima) selama 3 hari, menghasilkan total durasi proyek sebesar 57 hari kerja.

---

## 2. Alasan Mengapa Menjadi Jalur Kritis

Rangkaian aktivitas tersebut menjadi jalur kritis karena secara matematis seluruh aktivitas di sepanjang alur ini memiliki nilai kelonggaran waktu atau slack sebesar nol. Dalam metodologi jalur kritis, nilai slack nol menandakan bahwa waktu mulai paling cepat sama persis dengan batas waktu mulai paling lambat. Kondisi ini membuat setiap aktivitas di jalur tersebut tidak memiliki toleransi penundaan sama sekali. Apabila terjadi keterlambatan satu hari saja pada salah satu aktivitas kritis tersebut, maka tanggal serah terima akhir proyek secara otomatis akan ikut bergeser dan tertunda selama satu hari.

Selain itu, alur pengembangan perangkat lunak ini membentuk rangkaian ketergantungan terpanjang di dalam keseluruhan jadwal proyek. Berbeda dengan aktivitas pengadaan perangkat keras scanner dan server serta instalasi fisik kabel dan rak jaringan yang memiliki cadangan waktu senggang antara 13 hingga 19 hari, aktivitas pengembangan software inti dan pengujian memerlukan proses kerja berkesinambungan tanpa jeda. Jalur fisik dan pengadaan dapat selesai jauh lebih awal sebelum gerbang pengujian dibuka, sehingga keterlambatan pada pengiriman alat fisik tidak akan mengganggu jadwal proyek selama masih berada dalam batas kelonggaran waktunya.

Faktor penentu lainnya yang memperkuat status jalur kritis ini adalah terjadinya fenomena cabang kritis ganda yang berdurasi identik. Dari hari kerja ke-28 saat modul pelacakan utama selesai hingga hari kerja ke-47 saat pengujian penerimaan pengguna dimulai, cabang dashboard beserta uji integrasinya dan cabang aplikasi handheld beserta uji modulnya sama-sama membutuhkan waktu tepat 19 hari kerja untuk diselesaikan. Karena kedua cabang ini menjadi syarat mutlak yang harus tuntas bersamaan sebelum pengujian operasional oleh staf bandara dapat dilaksanakan, maka tidak ada satupun cabang yang memiliki waktu luang, sehingga keduanya secara bersamaan menyandang status kritis.

---

## 3. Tabel Ringkasan Aktivitas Jalur Kritis

| Kode | ID MPP | Nama Aktivitas | Durasi | ES | EF | LS | LF | Slack |
| :---: | :---: | :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **A** | 3 | Dokumen Project Charter & Rencana Proyek | 3 hari | 0 | 3 | 0 | 3 | 0 |
| **B** | 16 | Survei Titik Pemasangan & Peta Jalur Conveyor | 5 hari | 3 | 8 | 3 | 8 | 0 |
| **D** | 18 | Spesifikasi Integrasi API/DCS Penerbangan | 4 hari | 8 | 12 | 8 | 12 | 0 |
| **I** | 26 | Engine Pelacakan Real-Time & Mismatch Alert | 16 hari | 12 | 28 | 12 | 28 | 0 |
| **J** | 27 | Dashboard Visual & Manajemen Hak Akses | 14 hari | 28 | 42 | 28 | 42 | 0 |
| **K** | 28 | Aplikasi Handheld Scanner (Mode Offline) | 6 hari | 28 | 34 | 28 | 34 | 0 |
| **L** | 29 | Fitur Notifikasi Layar Carousel Kedatangan | 3 hari | 34 | 37 | 34 | 37 | 0 |
| **M** | 30 | Fitur Ekspor Laporan Statistik, Log & Backup | 4 hari | 37 | 41 | 37 | 41 | 0 |
| **Q** | 37 | Pengujian Seluruh Modul Sistem RFID | 6 hari | 41 | 47 | 41 | 47 | 0 |
| **R** | 38 | Laporan Hasil Pengujian Sistem (SIT) | 5 hari | 42 | 47 | 42 | 47 | 0 |
| **S** | 39 | Laporan UAT & Simulasi Bagasi Nyasar | 4 hari | 47 | 51 | 47 | 51 | 0 |
| **T** | 40 | Pelatihan Staf Ground Handling & Check-in | 3 hari | 51 | 54 | 51 | 54 | 0 |
| **U** | 41 | Dokumen Laporan Akhir & Serah Terima | 3 hari | 54 | 57 | 54 | 57 | 0 |
