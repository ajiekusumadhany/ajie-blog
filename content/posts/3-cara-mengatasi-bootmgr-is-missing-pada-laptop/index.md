---
title: "3+ Cara Mengatasi Bootmgr Is Missing Pada Laptop"
date: 2025-08-02
categories: 
  - "laptop"
tags: 
  - "cara"
  - "laptop"
  - "mengatasi"
---

Lagi asyik-asyiknya ngerjain tugas atau nonton film, tiba-tiba laptop kamu mati mendadak? Pas dinyalain lagi, eh malah muncul tulisan "BOOTMGR is missing"? Panik, kan? Jangan khawatir, kamu nggak sendirian kok. Masalah ini sering banget dialami pengguna laptop Windows.

BOOTMGR (Windows Boot Manager) itu ibaratnya kondektur yang mengarahkan sistem operasi untuk berjalan. Kalau dia hilang atau rusak, ya jelas laptop jadi bingung dan nggak bisa booting. Tapi tenang, nggak perlu langsung bawa ke tukang servis. Ada beberapa cara sederhana yang bisa kamu coba sendiri untuk mengatasi "BOOTMGR is missing" pada laptop.

Di artikel ini, kita bakal kupas tuntas 3+ cara ampuh mengatasi masalah ini. Mulai dari yang paling sederhana, sampai yang sedikit lebih teknis. Dijamin, setelah baca artikel ini, kamu bisa nyalain laptop kesayanganmu lagi tanpa ribet! Yuk, simak selengkapnya!

## 3+ Cara Mengatasi Bootmgr Is Missing Pada Laptop

Berikut adalah beberapa cara yang bisa kamu coba untuk mengatasi masalah "BOOTMGR is missing" pada laptop Windows kamu:

### 1\. Restart Laptop

Percaya atau tidak, cara paling sederhana ini seringkali jadi solusi mujarab. Kadang, masalah "BOOTMGR is missing" muncul karena kesalahan sementara pada sistem.

- **Caranya:** Matikan paksa laptop kamu dengan menekan tombol power agak lama (sekitar 5-10 detik). Tunggu beberapa saat, lalu nyalakan kembali.

Siapa tahu, dengan restart sederhana ini, laptop kamu bisa kembali normal. Kalau masih belum berhasil, lanjut ke cara berikutnya.

### 2\. Periksa Urutan Boot di BIOS

BIOS (Basic Input/Output System) adalah sistem dasar yang pertama kali dijalankan saat laptop dinyalakan. Di BIOS, kamu bisa mengatur urutan booting, yaitu dari mana laptop akan mencoba membaca sistem operasi. Kalau urutan booting salah, misalnya laptop mencoba booting dari USB yang kosong, ya pasti muncul masalah.

- **Caranya:**
    1. Restart laptop kamu.
    2. Saat logo pabrikan muncul (misalnya logo ASUS, Lenovo, atau Acer), segera tekan tombol BIOS. Tombol ini berbeda-beda tergantung merek laptop. Biasanya tombol yang digunakan adalah `Del`, `F2`, `F12`, `Esc`, atau `F10`. Coba cari informasi tombol BIOS untuk merek laptop kamu di internet.
    3. Setelah masuk ke BIOS, cari menu "Boot", "Boot Order", atau yang sejenisnya.
    4. Pastikan hard drive atau SSD (tempat sistem operasi Windows kamu terinstall) berada di urutan pertama.
    5. Simpan perubahan dan keluar dari BIOS. Biasanya ada pilihan "Save & Exit" atau tekan tombol `F10`.

Setelah kamu mengatur urutan booting dengan benar, coba restart laptop kamu. Semoga kali ini berhasil!

### 3\. Gunakan Startup Repair dengan Media Instalasi Windows

Jika kedua cara di atas belum membuahkan hasil, saatnya menggunakan jurus yang lebih ampuh, yaitu Startup Repair. Tapi, untuk melakukan ini, kamu membutuhkan media instalasi Windows, bisa berupa DVD atau USB bootable.

- **Persiapan:**
    - Siapkan DVD atau USB bootable Windows yang sesuai dengan versi Windows yang terinstall di laptop kamu. Jika belum punya, kamu bisa membuatnya dengan bantuan laptop lain.
- **Caranya:**
    1. Masukkan DVD atau tancapkan USB bootable ke laptop kamu.
    2. Restart laptop kamu.
    3. Pastikan laptop booting dari DVD atau USB. Jika tidak otomatis, kamu mungkin perlu masuk ke BIOS lagi dan mengubah urutan booting seperti pada cara sebelumnya.
    4. Setelah booting dari media instalasi, pilih bahasa dan keyboard yang sesuai.
    5. Pada layar "Install Windows", jangan klik "Install now". Pilih "Repair your computer" di bagian bawah.
    6. Pilih "Troubleshoot" > "Advanced options" > "Startup Repair".
    7. Windows akan mencoba memperbaiki masalah booting secara otomatis. Proses ini mungkin memakan waktu beberapa menit.

Setelah proses Startup Repair selesai, restart laptop kamu. Semoga "BOOTMGR is missing" sudah hilang dan laptop kamu bisa booting dengan normal.

### 4\. Perbaiki MBR (Master Boot Record) dan Boot Sector

Jika Startup Repair masih belum berhasil, kemungkinan masalahnya lebih dalam, yaitu pada MBR (Master Boot Record) atau Boot Sector. MBR adalah bagian penting dari hard drive yang berisi informasi tentang partisi dan sistem operasi yang terinstall. Boot Sector adalah bagian dari partisi yang berisi kode untuk memulai proses booting. Jika keduanya rusak, ya jelas laptop nggak bisa booting.

Untuk memperbaiki MBR dan Boot Sector, kamu perlu menggunakan Command Prompt dari media instalasi Windows.

- **Caranya:**
    1. Booting dari media instalasi Windows seperti pada cara sebelumnya.
    2. Pilih bahasa dan keyboard yang sesuai.
    3. Pada layar "Install Windows", pilih "Repair your computer" di bagian bawah.
    4. Pilih "Troubleshoot" > "Advanced options" > "Command Prompt".
    5. Di Command Prompt, ketik perintah berikut satu per satu, lalu tekan Enter setelah setiap perintah:
        - `bootrec /fixmbr`
        - `bootrec /fixboot`
        - `bootrec /scanos`
        - `bootrec /rebuildbcd`
    6. Setelah semua perintah selesai dijalankan, ketik `exit` lalu tekan Enter untuk keluar dari Command Prompt.
    7. Restart laptop kamu.

Perintah-perintah di atas berfungsi untuk:

- `/fixmbr`: Memperbaiki MBR yang rusak.
- `/fixboot`: Memperbaiki Boot Sector yang rusak.
- `/scanos`: Memindai semua sistem operasi yang terinstall di hard drive.
- `/rebuildbcd`: Membangun ulang Boot Configuration Data (BCD), yaitu database yang berisi informasi tentang sistem operasi yang bisa di-boot.

Cara ini biasanya ampuh untuk mengatasi masalah "BOOTMGR is missing" yang disebabkan oleh kerusakan MBR atau Boot Sector.

### 5\. Cek Kondisi Hard Drive

Meskipun jarang terjadi, masalah "BOOTMGR is missing" juga bisa disebabkan oleh kerusakan fisik pada hard drive. Jika hard drive sudah mulai rusak, kemungkinan besar akan muncul bad sector atau masalah lainnya yang bisa mengganggu proses booting.

Untuk mengecek kondisi hard drive, kamu bisa menggunakan tools diagnostik yang disediakan oleh pabrikan hard drive atau menggunakan tools pihak ketiga seperti CrystalDiskInfo.

- **Caranya:**
    1. Unduh dan install CrystalDiskInfo di laptop lain yang berfungsi.
    2. Lepaskan hard drive dari laptop yang bermasalah dan hubungkan ke laptop yang berfungsi (bisa menggunakan adapter SATA to USB).
    3. Jalankan CrystalDiskInfo.
    4. Perhatikan status hard drive. Jika statusnya "Caution" atau "Bad", berarti hard drive kamu sudah bermasalah dan sebaiknya segera diganti.

Jika hard drive kamu memang rusak, satu-satunya solusi adalah menggantinya dengan hard drive baru.

## Kesimpulan

Masalah "BOOTMGR is missing" pada laptop memang bikin panik, tapi jangan buru-buru nyerah. Dengan beberapa cara sederhana yang sudah kita bahas di atas, kamu bisa mencoba memperbaikinya sendiri. Mulai dari restart laptop, periksa urutan booting di BIOS, gunakan Startup Repair, perbaiki MBR dan Boot Sector, sampai cek kondisi hard drive.

Semoga salah satu cara di atas berhasil mengatasi masalah kamu. Kalau masih belum berhasil juga, mungkin memang saatnya meminta bantuan teknisi profesional. Tapi, setidaknya kamu sudah mencoba yang terbaik!

Punya pengalaman lain dalam mengatasi "BOOTMGR is missing"? Jangan ragu untuk berbagi di kolom komentar!

## FAQ (Frequently Asked Questions)

Berikut adalah beberapa pertanyaan yang sering diajukan terkait masalah "BOOTMGR is missing":

**1\. Apa itu BOOTMGR?**

BOOTMGR adalah singkatan dari Windows Boot Manager. Ini adalah program kecil yang dijalankan saat laptop pertama kali dinyalakan. Tugasnya adalah mencari dan memulai sistem operasi Windows. Jika BOOTMGR hilang atau rusak, laptop tidak akan bisa booting.

**2\. Apa penyebab munculnya pesan "BOOTMGR is missing"?**

Ada beberapa penyebab umum munculnya pesan "BOOTMGR is missing", antara lain:

- File BOOTMGR rusak atau terhapus.
- Urutan booting di BIOS salah.
- MBR (Master Boot Record) atau Boot Sector rusak.
- Hard drive rusak.
- Kabel SATA longgar.

**3\. Apakah semua cara di atas aman untuk data saya?**

Sebagian besar cara di atas aman untuk data kamu. Namun, ada beberapa hal yang perlu diperhatikan:

- Saat memperbaiki MBR dan Boot Sector, pastikan kamu mengetik perintah dengan benar. Salah ketik bisa menyebabkan masalah yang lebih serius.
- Jika hard drive kamu sudah rusak, sebaiknya segera backup data kamu sebelum melakukan perbaikan apapun.

**4\. Apakah saya harus menginstall ulang Windows jika semua cara di atas gagal?**

Menginstall ulang Windows adalah opsi terakhir jika semua cara di atas gagal. Namun, sebelum melakukan itu, pastikan kamu sudah membackup semua data penting kamu. Proses install ulang Windows akan menghapus semua data di hard drive.
