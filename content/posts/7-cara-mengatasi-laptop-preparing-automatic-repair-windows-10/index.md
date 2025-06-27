---
title: "7+ Cara Mengatasi Laptop Preparing Automatic Repair Windows 10"
date: 2025-12-09
categories: 
  - "laptop"
tags: 
  - "laptop"
---

Pernahkah laptop kesayanganmu tiba-tiba terjebak di layar "Preparing Automatic Repair" tanpa ada ujungnya? Pasti bikin panik, kan? Rasanya kayak lagi nunggu antrian panjang di loket padahal lagi kebelet. Jangan khawatir, kamu nggak sendirian! Banyak pengguna Windows 10 mengalami masalah serupa. Kabar baiknya, ada beberapa cara jitu yang bisa kamu coba sendiri untuk mengatasi masalah ini. Artikel ini akan membongkar 7+ cara ampuh mengatasi laptop yang stuck di "Preparing Automatic Repair" Windows 10, lengkap dengan langkah-langkah yang mudah diikuti. Yuk, simak sampai habis!

## 7+ Cara Mengatasi Laptop Preparing Automatic Repair Windows 10

"Preparing Automatic Repair" seharusnya menjadi penyelamat saat Windows 10 mengalami masalah. Tapi ironisnya, justru seringkali malah menjadi masalah itu sendiri. Penyebabnya bisa beragam, mulai dari file sistem yang rusak, driver yang bermasalah, hingga masalah hardware. Sebelum panik dan bawa ke tukang servis, coba dulu langkah-langkah berikut ini:

### 1\. Tunggu dengan Sabar

Mungkin terdengar klise, tapi kadang "Preparing Automatic Repair" memang butuh waktu untuk menyelesaikan prosesnya. Terutama jika laptopmu sudah lama tidak dimatikan atau sedang menjalankan banyak aplikasi berat.

- **Tunggu minimal 1-2 jam.** Sambil menunggu, kamu bisa ngopi atau melakukan aktivitas lain yang nggak bikin stres.
- **Perhatikan indikator aktivitas hard drive.** Jika lampu indikator masih berkedip-kedip, berarti laptop masih bekerja.

Jika setelah menunggu lama dan tidak ada perubahan, lanjut ke langkah berikutnya.

### 2\. Hard Reset (Paksa Restart)

Cara ini bisa dibilang "obat kuat" untuk mengatasi masalah sementara. Hard reset akan mematikan paksa laptopmu dan memulainya kembali.

- **Tekan dan tahan tombol power selama 10-15 detik.** Laptop akan mati secara paksa.
- **Lepaskan tombol power dan tunggu beberapa detik.**
- **Tekan tombol power kembali untuk menyalakan laptop.**

Semoga saja dengan cara ini, laptopmu bisa booting dengan normal. Jika masih stuck di "Preparing Automatic Repair", jangan menyerah!

### 3\. Boot ke Safe Mode

Safe Mode adalah mode diagnostik yang menjalankan Windows dengan driver dan program minimal. Ini membantu mengidentifikasi apakah masalahnya disebabkan oleh software atau driver tertentu.

- **Restart laptopmu.**
- **Saat laptop mulai menyala, tekan terus-menerus tombol F8 atau Shift + F8.** (Tombol ini bisa berbeda tergantung merk laptopmu. Coba cari tahu tombol yang tepat untuk laptopmu.)
- **Pilih "Safe Mode" atau "Safe Mode with Networking" dari menu Advanced Boot Options.**

Jika laptop berhasil masuk ke Safe Mode, berarti masalahnya kemungkinan besar disebabkan oleh software atau driver.

### 4\. Jalankan System Restore

System Restore mengembalikan sistem Windows ke titik waktu sebelumnya saat laptop masih berfungsi dengan baik. Ini bisa menjadi solusi ampuh jika masalahnya disebabkan oleh perubahan software atau driver yang baru saja kamu instal.

- **Boot ke Safe Mode (lihat langkah sebelumnya).**
- **Ketik "System Restore" di kotak pencarian Windows.**
- **Pilih "Create a restore point".**
- **Ikuti instruksi di layar untuk memilih titik restore dan memulai proses System Restore.**

Pastikan kamu memilih titik restore yang dibuat sebelum masalah "Preparing Automatic Repair" muncul.

### 5\. Gunakan Command Prompt (CMD)

Command Prompt adalah alat baris perintah yang memungkinkan kamu menjalankan berbagai perintah untuk memperbaiki sistem Windows.

- **Boot ke Safe Mode with Command Prompt.**
- **Ketik perintah berikut satu per satu, lalu tekan Enter setelah setiap perintah:**
    
    - `chkdsk /r c:` (Perintah ini akan memeriksa dan memperbaiki kesalahan pada hard drive C:)
    - `sfc /scannow` (Perintah ini akan memindai dan memperbaiki file sistem Windows yang rusak)
    - `bootrec /fixmbr` (Perintah ini akan memperbaiki Master Boot Record)
    - `bootrec /fixboot` (Perintah ini akan memperbaiki Boot Sector)
    - `bootrec /rebuildbcd` (Perintah ini akan membangun ulang Boot Configuration Data)
- **Restart laptopmu setelah semua perintah selesai dijalankan.**

Perintah-perintah ini cukup powerful dan bisa membantu mengatasi berbagai masalah booting.

### 6\. Nonaktifkan Automatic Repair

Mungkin terdengar aneh, tapi menonaktifkan Automatic Repair justru bisa menjadi solusi. Terkadang, fitur ini justru menjadi penyebab masalah "Preparing Automatic Repair".

- **Boot ke Safe Mode with Command Prompt.**
- **Ketik perintah berikut, lalu tekan Enter:**
    
    - `bcdedit /set default recoveryenabled no`
- **Restart laptopmu.**

Dengan menonaktifkan Automatic Repair, laptopmu akan mencoba booting langsung ke Windows tanpa melalui proses perbaikan otomatis.

### 7\. Reset Windows 10

Jika semua cara di atas gagal, opsi terakhir adalah mereset Windows 10. Ini akan mengembalikan laptopmu ke pengaturan pabrik.

- **Boot ke Windows Recovery Environment (WinRE).** Caranya bisa berbeda tergantung merk laptopmu, tapi biasanya dengan menekan tombol F11 atau tombol recovery lainnya saat laptop mulai menyala.
- **Pilih "Troubleshoot" > "Reset this PC".**
- **Pilih opsi "Keep my files" (jika kamu ingin menyimpan data pribadi) atau "Remove everything" (jika kamu ingin menghapus semua data).**
- **Ikuti instruksi di layar untuk menyelesaikan proses reset.**

**Peringatan:** Mereset Windows 10 akan menghapus semua program dan pengaturan yang kamu instal. Pastikan kamu sudah membackup data penting sebelum melakukan reset.

### 8\. Periksa Hardware

Jika semua cara software sudah dicoba dan masih gagal, kemungkinan masalahnya ada pada hardware.

- **Periksa RAM (Random Access Memory).** Lepaskan modul RAM dan bersihkan pinnya dengan penghapus pensil. Pasang kembali dan coba booting.
- **Periksa Hard Drive atau SSD.** Pastikan kabel terpasang dengan benar. Jika memungkinkan, coba ganti kabel SATA atau coba hard drive/SSD di laptop lain untuk memastikan kondisinya.

Jika kamu tidak yakin cara melakukan perbaikan hardware, sebaiknya bawa laptopmu ke teknisi profesional.

## Kesimpulan

Mengatasi laptop yang stuck di "Preparing Automatic Repair" Windows 10 memang membutuhkan kesabaran dan ketelitian. Tapi dengan mengikuti langkah-langkah di atas, kamu punya peluang besar untuk memperbaikinya sendiri. Ingat, selalu backup data pentingmu sebelum melakukan perubahan sistem yang signifikan.

Punya pengalaman lain dalam mengatasi masalah "Preparing Automatic Repair"? Jangan ragu untuk berbagi di kolom komentar! Mari saling membantu!

## FAQ (Frequently Asked Questions)

**1\. Kenapa laptop saya sering stuck di "Preparing Automatic Repair"?**

Penyebabnya bisa beragam, mulai dari file sistem yang rusak, driver yang bermasalah, masalah hardware, hingga infeksi malware.

**2\. Apakah mereset Windows 10 akan menghapus semua data saya?**

Tergantung opsi yang kamu pilih. Jika kamu memilih "Keep my files", data pribadi kamu akan tetap tersimpan. Tapi jika kamu memilih "Remove everything", semua data akan dihapus.

**3\. Berapa lama proses "Preparing Automatic Repair" seharusnya berlangsung?**

Idealnya, proses ini hanya membutuhkan beberapa menit. Jika sudah berlangsung lebih dari 1-2 jam tanpa ada perubahan, kemungkinan ada masalah yang lebih serius.
