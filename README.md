# Skrip Auto-Installer LAMP

## Deskripsi
Repository ini berisi skrip Bash yang kuat dan efisien yang dirancang untuk mengotomatisasi instalasi stack LAMP (Linux, Apache, MySQL, PHP) pada berbagai distribusi Linux. Skrip ini bertujuan untuk menyederhanakan proses pengaturan lingkungan server web, membuatnya dapat diakses oleh pemula dan administrator sistem berpengalaman.

Skrip ini secara cerdas mendeteksi sistem operasi dan menjalankan perintah yang sesuai menggunakan manajer paket sistem. Skrip ini memastikan instalasi lengkap Apache, MySQL (atau MariaDB pada CentOS dan Fedora), dan PHP, bersama dengan konfigurasi yang diperlukan untuk membuat server web Anda berjalan dengan lancar.

## Fitur
- **Deteksi OS Otomatis**: Skrip secara otomatis mendeteksi distribusi Linux Anda dan menyesuaikan proses instalasi sesuai.
- **Instalasi Komprehensif**: 
  - Menginstal Apache, perangkat lunak server web yang paling banyak digunakan di dunia.
  - Menginstal MySQL atau MariaDB, sistem manajemen basis data yang kuat.
  - Menginstal PHP, bahasa scripting sisi server yang populer.
- **Manajemen Layanan**: 
  - Memulai layanan Apache dan MySQL.
  - Mengaktifkan layanan ini untuk memulai secara otomatis saat boot sistem.
- **Mudah Digunakan**: 
  - Membutuhkan input pengguna yang minimal.
  - Pesan yang jelas dan informatif sepanjang proses instalasi.
- **Dukungan Multi-Distribusi**: Mendukung distribusi Linux utama termasuk Ubuntu, Debian, CentOS, RHEL, dan Fedora.

## Distribusi yang Didukung
- **Ubuntu**: Distribusi yang populer dan ramah pengguna berdasarkan Debian.
- **Debian**: Dikenal karena stabilitas dan keandalannya.
- **CentOS**: Alternatif gratis dan sumber terbuka untuk RHEL, banyak digunakan di lingkungan perusahaan.
- **RHEL (Red Hat Enterprise Linux)**: Platform Linux perusahaan terkemuka.
- **Fedora**: Distribusi mutakhir yang berfungsi sebagai tempat pengujian untuk RHEL.

## Prasyarat
- Sistem operasi berbasis Linux (Ubuntu, Debian, CentOS, RHEL, atau Fedora).
- Hak akses root atau sudo.

## Penggunaan

1. Klon Repository
   ```bash
   git clone https://github.com/asepsupriatna90/lamp-installer.git
   cd lamp-installer
   ```

2. **Unduh Skrip**
   Sebagai alternatif, Anda dapat mengunduh skrip secara langsung:
   ```bash
   wget https://raw.githubusercontent.com/asepsupriatna90/lamp-installer/main/install_lamp.sh
   ```

3. **Buat Skrip Dapat Dieksekusi**
   ```bash
   chmod +x install_lamp.sh
   ```

4. **Jalankan Skrip**
   ```bash
   sudo ./install_lamp.sh
   ```

Skrip ini akan memandu Anda melalui proses instalasi dengan prompt dan pesan yang jelas. Duduklah dan biarkan skrip menangani proses instalasi untuk Anda.

## Pemecahan Masalah
Jika Anda mengalami masalah selama instalasi, periksa hal-hal berikut:
- Pastikan Anda memiliki koneksi internet aktif untuk mengunduh paket.
- Verifikasi bahwa Anda memiliki ruang disk yang cukup.
- Periksa keluaran skrip untuk pesan kesalahan spesifik dan atasi sesuai dengan pesan tersebut.

Jika masalah berlanjut, jangan ragu untuk membuka issue di repository ini untuk bantuan lebih lanjut.

## Kontribusi
Kontribusi sangat diterima dan didorong! Jika Anda memiliki saran, perbaikan, atau penambahan, silakan lakukan hal berikut:
1. Fork repository ini.
2. Buat branch baru (`git checkout -b feature-branch`).
3. Lakukan perubahan Anda.
4. Commit perubahan Anda (`git commit -m 'Tambah fitur tertentu'`).
5. Push ke branch (`git push origin feature-branch`).
6. Buka pull request.

Kontribusi Anda akan membantu membuat proyek ini lebih baik untuk semua orang.

## Lisensi
Proyek ini dilisensikan di bawah Lisensi MIT. Anda bebas menggunakan, memodifikasi, dan mendistribusikan perangkat lunak ini sesuai dengan ketentuan lisensi.

---

Dengan menyediakan proses otomatis yang terstreamlining untuk menyiapkan stack LAMP, skrip ini bertujuan untuk menghemat waktu Anda dan mengurangi kerumitan dalam mengkonfigurasi lingkungan server web. Apakah Anda sedang mengatur lingkungan pengembangan, server pengujian, atau server produksi, skrip ini siap membantu Anda.
```
