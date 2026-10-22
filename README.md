# Booking Kos

Dokumentasi dari perancangan sistem informasi manajemen kos digital yang mentransformasikan proses manual menjadi arsitektur aplikasi web terintegrasi dan efisien.

---

## Disclaimer Privasi

> *Catatan:* Repositori ini murni menampilkan dokumentasi perancangan sistem dan analisis bisnis. Seluruh *source code*, konfigurasi server, serta kunci API tidak disematkan untuk mematuhi kebijakan privasi, hak kekayaan intelektual, serta perjanjian kerahasiaan dengan pihak mitra terkait.

## Latar Belakang & Analisis Masalah

* **Profil Studi Kasus:** **Kos Titik Kumpul** (berlokasi di Sedati, Sidoarjo) merupakan studi kasus nyata penyedia akomodasi kos yang membutuhkan modernisasi alur operasional bisnis sewa kamar.
* **Pain Points:**
  1. **Inefisiensi Waktu & Hambatan Jarak:** Proses survei manual yang membebani calon penyewa dari luar daerah karena ketiadaan media informasi digital terpusat.
  2. **Pengelolaan Keuangan & Pembukuan Konvensional:** Penggunaan pembukuan manual berbasis kertas yang rawan *human error* dan menyulitkan audit keuangan bulanan.
  3. **Manajemen Data & Kepatuhan Pelaporan:** Kompleksitas pemantauan ketersediaan kamar secara *real-time* serta pendataan penyewa yang kurang terstruktur untuk keperluan laporan administrasi.

## Panduan Navigasi Dokumen

Dokumen ini disusun secara sistematis untuk menunjukan alur kerja dan analisis bisnis menjadi spesifikasi teknis serta perancangan sistem. Dokumen ini dapat ditelusuri melalui urutan alur berikut:

1. **Business Requirement Document (BRD):** Meninjau batasan ruang lingkup proyek, objektif bisnis, dan alur kerja analitis dari sistem. ([Buka BRD](BRD.md))
2. **Functional Requirement Document (FRD):** Menilai daftar kebutuhan fungsional (FR) dan parameter non-fungsional (NFR) spesifikasi perangkat lunak. ([Buka FRD](FRD.md))
3. **Pemodelan Sistem (System Modeling):** Mempelajari perancangan alur proses (*Flowchart*), batasan sistem (Diagram Konteks), dekomposisi aliran data (DFD), hingga struktur basis data relasional (ERD). ([Buka System Modeling](system-modeling.md))

## Fitur Utama

* **Manajemen Kamar:** Pengelolaan inventaris kamar terpusat beserta filter status untuk mengatasi hambatan akses informasi jarak jauh bagi penyewa.
* **Pencatatan Reservasi & Pembayaran:** Digitalisasi alur pemesanan dan verifikasi pembayaran guna menggantikan pembukuan konvensional yang rentan kesalahan.
* **Notifikasi WhatsApp Bot:** Integrasi pesan otomatis untuk pengiriman *invoice* dan konfirmasi yang mempercepat siklus informasi transaksional.
* **Laporan Keuangan & Bulanan:** Modul rekapitulasi data finansial dan okupansi kamar untuk memudahkan analisis margin bagi pengelola.
* **Manajemen Pengguna:** Pembatasan akses berbasis peran antara pemilik (*Admin*) dan Penyewa (*User*) untuk menjaga keamanan data sistem.
