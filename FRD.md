# Functional & Non-Functional Requirement

## Functional Requirement

| ID | Modul / Fitur | Perilaku Sistem |
| :--- | :--- | :--- |
| **FR-01** | Registrasi Akun | Sistem harus dapat memvalidasi dan merekam data diri calon penyewa ke dalam *database* untuk pembuatan akun baru secara otomatis ketika data terisi lengkap dan valid. |
| **FR-02** | Autentikasi Login | Sistem harus menyediakan gerbang validasi kredensial (*username & password*) yang aman serta mencocokkannya dengan hak akses (*role*) akun yang telah terdaftar. |
| **FR-03** | Manajemen Data Master | Admin dapat melakukan pengelolaan penuh (*CRUD*) terhadap data master kamar kos, kategori, fasilitas, serta memvalidasi status pesanan dan pembayaran dari penyewa. |
| **FR-04** | Modul Reservasi / Pemesanan | Sistem dapat menerima, memproses, mencatat, dan mengelola transaksi pemesanan atau *booking* kamar yang diajukan oleh penyewa. |
| **FR-05** | Filter & Manajemen Kamar | Sistem harus bisa menyediakan fungsi filter dan menampilkan opsi ketersediaan kamar kos berdasarkan status (tersedia/tersewa) serta fasilitas secara *real-time*. |
| **FR-06** | Penerbitan Invoice | Sistem harus bisa menghasilkan dan mencetak lembar tagihan atau *invoice* digital secara otomatis atas transaksi pemesanan yang berhasil divalidasi. |
| **FR-07** | Integrasi Bot WhatsApp | Sistem memicu dan mengirimkan pesan atau tautan *invoice* secara langsung ke nomor WhatsApp penyewa yang terdaftar setelah pembayaran berhasil divalidasi. |

---

## Non-Functional Requirement

| ID | Kategori | Parameter Kebutuhan Non-Fungsional |
| :--- | :--- | :--- |
| **NFR-01** | Usability (Kegunaan) | Antarmuka sistem (*pendaftaran, pencarian kamar, booking, dashboard*) harus responsif (*mobile & desktop friendly*) serta memiliki navigasi alur pemesanan yang intuitif dan mudah digunakan oleh pengguna. |
| **NFR-02** | Performance & Efficiency | Waktu muat (*load time*) halaman utama, registrasi, login, dan pencarian/filter kamar tidak boleh melebihi 2–3 detik. Pengiriman pesan via Bot WhatsApp harus terkirim dalam rentang waktu maksimal 10–15 detik setelah *invoice* diterbitkan dalam kondisi jaringan normal. |
| **NFR-03** | Security (Keamanan) | *Password* pengguna (*user* dan *admin*) serta nomor telepon wajib disimpan menggunakan teknik enkripsi *hashing* yang aman (tidak *plain text*), pembatasan hak akses berbasis *role*, serta komunikasi data wajib menggunakan protokol HTTPS/SSL/TLS. |
| **NFR-04** | Reliability & Availability | Sistem operasional harus memiliki tingkat ketersediaan (*uptime*) minimal 99.5% per bulan, serta dilengkapi mekanisme coba ulang otomatis (*auto-retry queue*) pada modul bot dan tautan unduh manual di dasbor jika terjadi gangguan eksternal. |
| **NFR-05** | Maintainability | Arsitektur kode program harus dibuat secara modular (memisahkan layanan Bot WhatsApp sebagai modul atau mikroservis tersendiri) serta mencatat log aktivitas penting (*audit logging*) untuk mempermudah pemeliharaan dan *debugging*. |
| **NFR-06** | Scalability (Skalabilitas) | Sistem harus mampu menangani setidaknya 100 hingga 500 pengguna secara bersamaan (*concurrent users*) tanpa mengalami penurunan kinerja, dan antrean pesan bot harus mampu memproses pengiriman secara simultan saat terjadi lonjakan. |
| **NFR-07** | Compatibility & Portability | Aplikasi web harus kompatibel dan berjalan optimal pada berbagai peramban modern (Google Chrome, Mozilla Firefox, Safari, Microsoft Edge) serta terintegrasi dengan standar API WhatsApp Gateway yang andal. |
