---
title: "Mudah! Cara Pasang Twrp Xiaomi"
date: 2023-11-02
categories: 
  - "smartphone"
tags: 
  - "xiaomi"
---

Jika Anda pengguna smartphone [Xiaomi](https://ajiekusumadhany.com/gadget/smartphone/xiaomi/), tidak lengkap rasanya jika belum memasang TWRP. TWRP (Team Win Recovery Project) adalah custom recovery yang memungkinkan Anda untuk menginstal ROM kustom, melakukan backup data, menghapus bloatware, dan masih banyak lagi. Namun, bagi sebagian orang, proses instalasi TWRP bisa terasa sulit dan membingungkan. Nah, dalam artikel ini, kami akan memberikan langkah-langkah mudah untuk memasang TWRP di smartphone Xiaomi Anda dalam bentuk listicle. Yuk, simak!

 

## Langkah 1: Unlock Bootloader

 

Sebelum memasang TWRP, Anda perlu melakukan unlock bootloader terlebih dahulu. Caranya:

 

1\. Aktifkan Opsi Pengembang dengan cara masuk ke Pengaturan, pilih Tentang Ponsel, lalu ketuk beberapa kali pada Nomor Build hingga muncul notifikasi bahwa Opsi Pengembang telah diaktifkan.

 

2\. Masuk ke Opsi Pengembang dan aktifkan OEM Unlocking dan USB Debugging.

 

3\. Hubungkan smartphone Xiaomi Anda ke komputer melalui kabel USB.

 

4\. Buka Command Prompt di komputer dan ketik perintah `adb devices` untuk memastikan smartphone sudah terdeteksi.

 

5\. Kemudian, ketik perintah `adb reboot bootloader` untuk masuk ke mode bootloader.

 

6\. Setelah masuk ke mode bootloader, ketik perintah `fastboot devices` untuk memastikan smartphone sudah terhubung ke komputer melalui mode fastboot.

 

7\. Untuk melakukan unlock bootloader, ketik perintah `fastboot oem unlock`. Smartphone Anda akan restart dan bootloader akan ter-unlock.

 

## Langkah 2: Unduh dan Pasang ADB dan Fastboot

 

Untuk memasang TWRP, Anda perlu mengunduh dan memasang ADB dan Fastboot di komputer Anda. Caranya:

 

1\. Kunjungi situs resmi Android SDK Platform Tools (https://developer.android.com/studio/releases/platform-tools) dan unduh versi terbaru sesuai dengan sistem operasi Anda.

 

2\. Ekstrak file yang telah Anda unduh.

 

3\. Buka folder hasil ekstraksi, klik kanan di dalam folder tersebut, lalu pilih "Open PowerShell window here" atau "Open Command Prompt here".

 

4\. Ketik perintah `adb devices` untuk memastikan bila ADB sudah terpasang dengan baik dan smartphone sudah terdeteksi.

 

## Langkah 3: Unduh TWRP

 

Langkah selanjutnya adalah mengunduh file TWRP sesuai dengan tipe smartphone Xiaomi Anda. Caranya:

 

1\. Buka situs resmi TWRP (https://twrp.me/Devices/Xiaomi/) dan cari model smartphone Xiaomi Anda.

 

2\. Klik link unduh yang tersedia di sebelah kanan model smartphone Anda.

 

3\. File TWRP akan diunduh dalam format .img.

 

## Langkah 4: Pasang TWRP

 

Setelah file TWRP berhasil diunduh, saatnya memasangnya di smartphone Xiaomi Anda. Caranya:

 

1\. Salin file TWRP yang diunduh ke dalam folder ADB yang telah Anda ekstrak sebelumnya.

 

2\. Buka Command Prompt atau PowerShell seperti pada langkah sebelumnya.

 

3\. Ketik perintah `adb reboot bootloader` untuk masuk ke mode bootloader.

 

4\. Setelah masuk ke mode bootloader, ketik perintah `fastboot boot namafile.img` (ganti "namafile" dengan nama file TWRP yang Anda unduh).

 

5\. TWRP akan terpasang sementara dan smartphone akan mem-boot ke recovery mode.

 

6\. Pada TWRP, ketuk opsi "Install" dan cari file TWRP yang ada di dalam smartphone.

 

7\. Setelah file TWRP ditemukan, geser untuk mengkonfirmasi proses instalasi.

 

8\. Tunggu hingga proses instalasi selesai.

 

9\. Setelah proses instalasi selesai, ketuk opsi "Reboot System" untuk me-restart smartphone.

 

## Kesimpulan

 

Itulah langkah-langkah mudah untuk memasang TWRP di smartphone Xiaomi Anda. Dengan memasang TWRP, Anda dapat menikmati berbagai fitur dan kemudahan yang tidak tersedia di recovery bawaan Xiaomi. Namun, perlu diingat bahwa memasang TWRP akan membatalkan garansi resmi smartphone Anda dan bisa berpotensi menyebabkan kerusakan jika tidak dilakukan dengan benar. Oleh karena itu, pastikan Anda mengikuti langkah-langkah dengan teliti dan bertanggung jawab atas risiko yang mungkin terjadi.

 

## FAQ (Pertanyaan Sering Diajukan)

 

**1\. Apakah memasang TWRP bisa membatalkan garansi resmi smartphone?**

 

Ya, memasang TWRP biasanya akan membatalkan garansi resmi smartphone. Namun, ada beberapa produsen smartphone yang memperbolehkan pengguna untuk memasang TWRP tanpa membatalkan garansi, seperti OnePlus.

 

**2\. Apakah TWRP hanya tersedia untuk smartphone Xiaomi?**

 

Tidak, TWRP tersedia untuk berbagai merek smartphone lainnya juga. Namun, setiap merek dan model smartphone memiliki versi TWRP yang berbeda, jadi pastikan Anda mengunduh file TWRP yang tepat untuk smartphone Anda.

 

**3\. Apakah memasang TWRP bisa menghapus semua data di smartphone?**

 

Tidak, memasang TWRP tidak akan menghapus data di smartphone Anda. Namun, saat melakukan flash ROM kustom atau factory reset melalui TWRP, maka semua data di smartphone akan terhapus.

 

**4\. Bagaimana cara mengakses TWRP setelah terpasang?**

 

Untuk mengakses TWRP setelah terpasang, matikan smartphone Anda, lalu tekan kombinasi tombol power dan volume up secara bersamaan hingga masuk ke menu TWRP.

 

**5\. Bisakah TWRP digunakan untuk menginstal ROM kustom?**

 

Ya, TWRP dapat digunakan untuk menginstal ROM kustom. Anda dapat mengunduh file ROM kustom yang diinginkan dan menginstalnya melalui opsi "Install" di TWRP.
