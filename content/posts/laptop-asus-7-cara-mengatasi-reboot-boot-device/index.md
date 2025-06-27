---
title: "Laptop Asus: 7+ Cara Mengatasi Reboot &amp; Boot Device"
date: 2025-08-11
categories: 
  - "laptop"
tags: 
  - "laptop"
---

**Laptop Asus: 7+ Cara Mengatasi Reboot & Boot Device**

Pernahkah Anda mengalami laptop Asus yang tiba-tiba reboot sendiri dan menampilkan pesan "Reboot and Select Proper Boot Device"? Bayangkan sedang mengerjakan tugas penting, tiba-tiba layar biru dan pesan error itu muncul. Frustrasi? Tentu saja! Masalah ini seringkali membuat panik, tapi jangan khawatir. Artikel ini akan memandu Anda melalui 7+ cara efektif mengatasi masalah "Reboot and Select Proper Boot Device" pada laptop Asus Anda, sehingga Anda bisa kembali bekerja atau bermain dengan tenang.

## Mengapa Laptop Asus Saya Menampilkan "Reboot and Select Proper Boot Device"?

Pesan error "Reboot and Select Proper Boot Device" mengindikasikan bahwa laptop Anda kesulitan menemukan sistem operasi (Windows) saat booting. Ada beberapa penyebab umumnya:

- **Kerusakan Hard Drive atau SSD:** Media penyimpanan yang rusak tidak dapat dibaca dengan benar.
- **Pengaturan BIOS yang Salah:** Urutan boot yang salah atau pengaturan BIOS yang tidak tepat.
- **File Sistem yang Rusak:** File sistem yang penting untuk booting mungkin korup.
- **Kabel Longgar:** Kabel SATA yang menghubungkan hard drive/SSD ke motherboard mungkin longgar.
- **Driver yang Bermasalah:** Driver yang usang atau tidak kompatibel dapat menyebabkan masalah booting.
- **Infeksi Virus:** Virus atau malware tertentu dapat merusak file sistem dan mengganggu proses booting.
- **Update Windows yang Gagal:** Proses update yang terganggu dapat menyebabkan kerusakan file sistem.

## 7+ Cara Mengatasi Laptop Reboot And Select Proper Boot Device Asus

Berikut adalah beberapa solusi yang bisa Anda coba untuk mengatasi masalah "Reboot and Select Proper Boot Device" pada laptop Asus Anda:

### 1\. Periksa Kabel dan Koneksi Fisik

Langkah pertama yang paling sederhana adalah memastikan semua kabel dan koneksi fisik terpasang dengan benar.

- **Buka casing laptop (jika memungkinkan dan Anda merasa nyaman).** Pastikan laptop dalam keadaan mati dan baterai dilepas.
- **Periksa kabel SATA yang menghubungkan hard drive/SSD ke motherboard.** Pastikan kabel terpasang dengan kuat di kedua ujungnya.
- **Jika Anda memiliki lebih dari satu hard drive/SSD, coba lepas salah satunya.** Kemudian, coba booting laptop hanya dengan satu drive.

### 2\. Ubah Urutan Boot di BIOS

BIOS (Basic Input/Output System) adalah program yang mengontrol proses booting laptop Anda. Anda perlu memastikan bahwa hard drive/SSD yang berisi sistem operasi Windows Anda adalah perangkat boot pertama.

- **Restart laptop Anda.**
- **Tekan tombol yang sesuai untuk masuk ke BIOS.** Tombol ini biasanya adalah Delete, F2, Esc, atau F12. Perhatikan pesan yang muncul saat laptop booting untuk mengetahui tombol yang tepat.
- **Cari opsi "Boot Order" atau "Boot Priority".** Lokasi opsi ini mungkin berbeda-beda tergantung pada merek dan model BIOS Anda.
- **Pastikan hard drive/SSD yang berisi sistem operasi Windows Anda berada di urutan pertama.** Gunakan tombol panah atau tombol +/- untuk mengubah urutan boot.
- **Simpan perubahan dan keluar dari BIOS.** Laptop Anda akan restart.

### 3\. Aktifkan atau Nonaktifkan UEFI/Legacy Boot

Mode boot UEFI (Unified Extensible Firmware Interface) adalah pengganti BIOS yang lebih modern. Terkadang, masalah "Reboot and Select Proper Boot Device" dapat diatasi dengan mengubah mode boot.

- **Masuk ke BIOS seperti yang dijelaskan di atas.**
- **Cari opsi "UEFI Boot" atau "Legacy Boot".**
- **Jika UEFI Boot aktif, coba nonaktifkan.** Jika Legacy Boot aktif, coba aktifkan.
- **Simpan perubahan dan keluar dari BIOS.**

### 4\. Perbaiki Master Boot Record (MBR) atau GUID Partition Table (GPT)

MBR dan GPT adalah struktur data yang menyimpan informasi tentang partisi hard drive. Jika MBR atau GPT rusak, laptop Anda mungkin tidak dapat menemukan sistem operasi.

- **Anda memerlukan media instalasi Windows (DVD atau USB) untuk melakukan perbaikan ini.** Jika Anda tidak memilikinya, Anda dapat membuatnya dengan menggunakan komputer lain.
    
- **Boot laptop Anda dari media instalasi Windows.**
    
- **Pilih bahasa dan keyboard Anda.**
    
- **Klik "Repair your computer" atau "Troubleshoot".**
    
- **Pilih "Command Prompt".**
    
- **Ketik perintah berikut dan tekan Enter setelah setiap perintah:**
    
    - `bootrec /fixmbr`
    - `bootrec /fixboot`
    - `bootrec /scanos`
    - `bootrec /rebuildbcd`
- **Restart laptop Anda.**
    

**Catatan:** Perintah di atas berfungsi untuk sistem yang menggunakan MBR. Jika sistem Anda menggunakan GPT, perintahnya sedikit berbeda. Anda perlu mencari panduan spesifik untuk memperbaiki GPT menggunakan Command Prompt.

### 5\. Jalankan Startup Repair

Startup Repair adalah alat bawaan Windows yang dapat memperbaiki masalah booting umum.

- **Boot laptop Anda dari media instalasi Windows seperti yang dijelaskan di atas.**
- **Pilih bahasa dan keyboard Anda.**
- **Klik "Repair your computer" atau "Troubleshoot".**
- **Pilih "Startup Repair".**
- **Ikuti petunjuk di layar.**

### 6\. Periksa Kesehatan Hard Drive/SSD

Hard drive atau SSD yang rusak dapat menyebabkan masalah booting. Anda dapat menggunakan alat diagnostik untuk memeriksa kesehatan drive Anda.

- **Anda dapat menggunakan alat diagnostik bawaan Windows (CHKDSK) atau alat pihak ketiga seperti CrystalDiskInfo.**
    
- **Untuk menggunakan CHKDSK, buka Command Prompt (seperti yang dijelaskan di atas) dan ketik perintah berikut:**
    
    - `chkdsk /f /r C:` (Ganti C: dengan huruf drive sistem Anda).
- **Restart laptop Anda.**
    

**Catatan:** CHKDSK dapat memakan waktu lama untuk dijalankan, tergantung pada ukuran dan kondisi hard drive/SSD Anda.

### 7\. Reset BIOS ke Pengaturan Default

Jika Anda telah mengubah pengaturan BIOS dan tidak yakin pengaturan mana yang menyebabkan masalah, Anda dapat mencoba mereset BIOS ke pengaturan default.

- **Masuk ke BIOS seperti yang dijelaskan di atas.**
- **Cari opsi "Load Defaults" atau "Reset to Default".**
- **Pilih opsi tersebut dan ikuti petunjuk di layar.**
- **Simpan perubahan dan keluar dari BIOS.**

### 8\. Instal Ulang Windows (Opsi Terakhir)

Jika semua solusi di atas tidak berhasil, kemungkinan besar ada masalah serius dengan sistem operasi Anda dan Anda perlu menginstal ulang Windows.

- **Pastikan Anda memiliki backup data penting Anda sebelum menginstal ulang Windows.** Proses instalasi ulang akan menghapus semua data di hard drive Anda.
- **Boot laptop Anda dari media instalasi Windows.**
- **Ikuti petunjuk di layar untuk menginstal ulang Windows.**

## Kesimpulan

Masalah "Reboot and Select Proper Boot Device" pada laptop Asus memang menjengkelkan, tapi seringkali dapat diatasi dengan langkah-langkah yang tepat. Mulailah dengan memeriksa koneksi fisik dan urutan boot di BIOS. Jika masalah berlanjut, coba perbaiki MBR/GPT, jalankan Startup Repair, atau periksa kesehatan hard drive/SSD Anda. Jika semua gagal, instal ulang Windows adalah opsi terakhir. Semoga artikel ini membantu Anda mengatasi masalah ini dan membuat laptop Asus Anda kembali berfungsi normal! Apakah Anda memiliki pengalaman lain dalam mengatasi masalah ini? Bagikan di komentar di bawah!

## FAQ (Frequently Asked Questions)

**1\. Mengapa laptop saya terus menerus reboot dan menampilkan pesan "Reboot and Select Proper Boot Device"?**

```
*   Laptop Anda mungkin mengalami masalah ini karena hard drive/SSD yang rusak, pengaturan BIOS yang salah, file sistem yang rusak, kabel yang longgar, driver yang bermasalah, infeksi virus, atau update Windows yang gagal.
```

**2\. Bagaimana cara mengetahui apakah hard drive/SSD saya rusak?**

```
*   Anda dapat menggunakan alat diagnostik seperti CHKDSK (bawaan Windows) atau CrystalDiskInfo (pihak ketiga) untuk memeriksa kesehatan hard drive/SSD Anda.  Jika alat diagnostik menemukan error, kemungkinan besar hard drive/SSD Anda rusak dan perlu diganti.
```

**3\. Apakah menginstal ulang Windows akan menghapus semua data saya?**

```
*   Ya, proses instalasi ulang Windows akan menghapus semua data di hard drive Anda.  Oleh karena itu, sangat penting untuk membackup data penting Anda sebelum menginstal ulang Windows.
```
