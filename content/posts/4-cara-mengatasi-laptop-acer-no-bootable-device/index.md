---
title: "4+ Cara Mengatasi Laptop Acer No Bootable Device"
date: 2025-08-06
categories: 
  - "laptop"
tags: 
  - "cara"
  - "laptop"
  - "mengatasi"
---

Pernahkah kamu panik saat menyalakan laptop Acer kesayangan, tapi yang muncul malah tulisan "No Bootable Device"? Rasanya seperti mimpi buruk, ya? Padahal, kerjaan numpuk, deadline sudah di depan mata, dan semua data penting ada di dalam laptop itu. Jangan langsung panik! Masalah ini lebih umum dari yang kamu kira, dan seringkali bisa diatasi sendiri di rumah tanpa perlu langsung lari ke tukang servis.

Artikel ini akan membantumu memahami apa itu "No Bootable Device", kenapa masalah ini bisa terjadi pada laptop Acer-mu, dan yang terpenting, memberikanmu 4+ cara ampuh untuk mengatasinya. Jadi, siapkan kopi, tarik kursi, dan mari kita bedah masalah ini satu per satu. Kita akan mengembalikan laptop Acer-mu ke kondisi prima secepat mungkin!

## Apa Itu "No Bootable Device" dan Kenapa Muncul?

Secara sederhana, "No Bootable Device" berarti laptopmu tidak bisa menemukan sistem operasi (seperti Windows) untuk dijalankan. Laptop membutuhkan "bootable device" (biasanya hard drive atau SSD) yang berisi file sistem operasi agar bisa berfungsi.

Nah, kenapa pesan kesalahan ini bisa muncul? Ada beberapa kemungkinan penyebabnya:

- **Kerusakan Hard Drive/SSD:** Ini adalah penyebab paling serius. Jika hard drive atau SSD-mu rusak secara fisik, laptop tidak akan bisa mengaksesnya.
- **BIOS Tidak Mendeteksi Hard Drive/SSD:** Kadang, BIOS (Basic Input/Output System) laptopmu tidak bisa mendeteksi keberadaan hard drive atau SSD.
- **Boot Order yang Salah:** BIOS memiliki urutan perangkat yang dicari saat booting. Jika hard drive/SSD-mu tidak berada di urutan pertama, laptop akan gagal menemukan sistem operasi.
- **File Sistem Operasi Rusak:** File-file penting yang dibutuhkan untuk menjalankan Windows bisa rusak karena berbagai alasan, seperti virus, kesalahan saat update, atau mati listrik tiba-tiba.
- **Kabel Longgar atau Terputus:** Kabel yang menghubungkan hard drive/SSD ke motherboard bisa longgar atau bahkan terputus.
- **Masalah pada Driver:** Driver yang tidak kompatibel atau rusak juga bisa menyebabkan masalah boot.

## 4+ Cara Mengatasi Laptop Acer No Bootable Device

Setelah memahami penyebabnya, sekarang saatnya kita membahas cara mengatasinya. Ikuti langkah-langkah berikut secara berurutan, dan semoga salah satu cara ini berhasil menyelamatkan laptop Acer-mu!

### 1\. Cek dan Pastikan Hard Drive/SSD Terdeteksi di BIOS

Langkah pertama yang penting adalah memastikan bahwa BIOS laptopmu mendeteksi hard drive atau SSD. Caranya:

1. **Matikan laptop Acer-mu sepenuhnya.**
2. **Nyalakan laptop, lalu segera tekan tombol BIOS.** Tombol ini bervariasi tergantung model laptop Acer-mu. Biasanya, tombol yang digunakan adalah **F2, Delete, Esc, atau F12.** Coba tekan beberapa kali sampai masuk ke menu BIOS. Jika tidak yakin, coba cari di internet dengan kata kunci "tombol BIOS laptop Acer \[model laptopmu\]".
3. **Di menu BIOS, cari bagian yang menunjukkan daftar perangkat penyimpanan.** Biasanya, bagian ini bernama "Boot", "Storage", atau "Information".
4. **Periksa apakah hard drive atau SSD-mu terdaftar di sana.** Jika tidak ada, kemungkinan ada masalah dengan koneksi fisik atau kerusakan pada hard drive/SSD.

**Jika Hard Drive/SSD Terdeteksi:** Lanjutkan ke langkah berikutnya.

**Jika Hard Drive/SSD Tidak Terdeteksi:**

- **Matikan laptop dan buka casingnya (jika kamu merasa nyaman melakukannya).** Pastikan kamu sudah mencabut semua kabel dan baterai sebelum membuka casing.
- **Periksa kabel SATA (untuk hard drive) atau konektor (untuk SSD) yang menghubungkan perangkat penyimpanan ke motherboard.** Pastikan kabel terpasang dengan benar dan tidak longgar.
- **Jika memungkinkan, coba ganti kabel SATA dengan yang baru.**
- **Jika masih tidak terdeteksi, kemungkinan besar hard drive atau SSD-mu rusak.** Kamu perlu menggantinya dengan yang baru.

### 2\. Atur Ulang Boot Order di BIOS

Jika hard drive/SSD terdeteksi di BIOS, langkah selanjutnya adalah memastikan bahwa perangkat tersebut berada di urutan pertama dalam boot order.

1. **Masuk kembali ke menu BIOS seperti pada langkah sebelumnya.**
2. **Cari bagian "Boot Order" atau "Boot Priority".**
3. **Pastikan hard drive atau SSD yang berisi sistem operasi Windows berada di urutan pertama.** Kamu bisa mengubah urutan ini menggunakan tombol panah atau tombol +/-.
4. **Simpan perubahan dan keluar dari BIOS.** Biasanya, ada opsi "Save & Exit" atau "Exit Saving Changes". Laptop akan restart secara otomatis.

**Penting:** Pastikan kamu memilih hard drive/SSD yang benar. Jika kamu memiliki beberapa perangkat penyimpanan, perhatikan nama dan modelnya.

### 3\. Jalankan Startup Repair Melalui Advanced Options

Jika masalah masih berlanjut, kamu bisa mencoba menjalankan Startup Repair melalui Advanced Options. Ini adalah fitur bawaan Windows yang bisa memperbaiki masalah boot secara otomatis.

1. **Siapkan media instalasi Windows (DVD atau USB).** Jika kamu tidak punya, kamu bisa membuatnya menggunakan laptop lain. Download file ISO Windows dari situs resmi Microsoft dan gunakan tool seperti Rufus untuk membuat bootable USB.
2. **Boot laptop Acer-mu dari media instalasi Windows.** Pastikan BIOS sudah diatur untuk boot dari DVD/USB.
3. **Setelah masuk ke menu instalasi Windows, jangan langsung menginstal.** Pilih opsi "Repair your computer" atau "Troubleshoot".
4. **Pilih "Advanced options".**
5. **Pilih "Startup Repair".** Windows akan mencoba mendiagnosis dan memperbaiki masalah boot secara otomatis.

Proses ini mungkin memakan waktu beberapa menit. Setelah selesai, restart laptopmu dan lihat apakah masalah sudah teratasi.

### 4\. Gunakan Command Prompt untuk Memperbaiki Boot Record

Jika Startup Repair tidak berhasil, kamu bisa mencoba memperbaiki boot record secara manual menggunakan Command Prompt. Cara ini lebih teknis, tapi seringkali efektif.

1. **Ikuti langkah 1-4 pada bagian Startup Repair di atas untuk masuk ke "Advanced options".**
    
2. **Pilih "Command Prompt".**
    
3. **Ketik perintah berikut satu per satu, lalu tekan Enter setelah setiap perintah:**
    
    - `bootrec /fixmbr`
    - `bootrec /fixboot`
    - `bootrec /scanos`
    - `bootrec /rebuildbcd`
4. **Setelah semua perintah selesai dijalankan, ketik `exit` dan tekan Enter untuk keluar dari Command Prompt.**
    
5. **Restart laptopmu.**
    

**Penjelasan Perintah:**

- `bootrec /fixmbr`: Memperbaiki Master Boot Record (MBR), bagian penting dari hard drive yang digunakan untuk memulai sistem operasi.
- `bootrec /fixboot`: Menulis boot sector baru ke partisi sistem.
- `bootrec /scanos`: Memindai semua sistem operasi yang terinstal di hard drive.
- `bootrec /rebuildbcd`: Membangun ulang Boot Configuration Data (BCD), database yang berisi informasi tentang bagaimana Windows harus di-boot.

### 5\. Lakukan Reset atau Instal Ulang Windows (Opsi Terakhir)

Jika semua cara di atas tidak berhasil, opsi terakhir adalah melakukan reset atau instal ulang Windows. **Perlu diingat, cara ini akan menghapus semua data di partisi sistem (biasanya drive C:). Jadi, pastikan kamu sudah membackup data pentingmu sebelum melakukan reset atau instal ulang.**

**Reset Windows:**

1. **Ikuti langkah 1-4 pada bagian Startup Repair di atas untuk masuk ke "Advanced options".**
2. **Pilih "Reset this PC".**
3. **Pilih opsi yang kamu inginkan.** Kamu bisa memilih untuk menghapus semua data atau hanya menghapus aplikasi dan pengaturan, tetapi menyimpan file pribadi.
4. **Ikuti petunjuk di layar untuk menyelesaikan proses reset.**

**Instal Ulang Windows:**

1. **Boot laptop Acer-mu dari media instalasi Windows (DVD atau USB).**
2. **Ikuti petunjuk di layar untuk menginstal Windows.**
3. **Pastikan kamu memilih opsi "Custom: Install Windows only (advanced)" dan menghapus semua partisi yang ada di hard drive sebelum menginstal Windows.** Ini akan memastikan instalasi yang bersih dan bebas dari masalah.

## Kesimpulan

Menemukan pesan "No Bootable Device" di laptop Acer memang bikin frustrasi. Tapi, dengan mengikuti langkah-langkah di atas, kamu punya peluang besar untuk mengatasinya sendiri. Mulai dari pengecekan sederhana di BIOS hingga perbaikan boot record menggunakan Command Prompt, setiap langkah membawa harapan untuk menghidupkan kembali laptopmu. Jika semua usaha sudah dilakukan dan masalah tetap ada, mungkin sudah saatnya mempertimbangkan untuk membawa laptop ke teknisi profesional.

Punya pengalaman serupa dengan "No Bootable Device"? Atau punya tips lain yang ingin dibagikan? Jangan ragu untuk tulis di kolom komentar! Sharing is caring, dan pengalamanmu mungkin bisa membantu orang lain yang sedang mengalami masalah yang sama.

## FAQ (Frequently Asked Questions)

Berikut beberapa pertanyaan umum seputar masalah "No Bootable Device" pada laptop Acer:

**1\. Apakah semua cara di atas bisa dilakukan sendiri tanpa keahlian khusus?**

Sebagian besar cara di atas relatif mudah diikuti. Namun, membuka casing laptop dan memeriksa koneksi fisik memerlukan kehati-hatian. Jika kamu tidak yakin, sebaiknya minta bantuan teman yang berpengalaman atau bawa ke teknisi.

**2\. Berapa lama waktu yang dibutuhkan untuk mengatasi masalah "No Bootable Device"?**

Waktu yang dibutuhkan bervariasi tergantung penyebab masalah dan kecepatan internetmu (jika perlu mendownload file ISO Windows). Pengecekan BIOS mungkin hanya butuh beberapa menit, sedangkan instal ulang Windows bisa memakan waktu beberapa jam.

**3\. Apakah masalah "No Bootable Device" bisa dicegah?**

Tentu saja! Beberapa tips untuk mencegah masalah ini:

- **Backup data secara rutin:** Ini sangat penting untuk menghindari kehilangan data jika terjadi masalah.
- **Jaga laptop dari benturan dan kerusakan fisik:** Hard drive/SSD rentan terhadap kerusakan fisik.
- **Hindari mematikan laptop secara paksa:** Matikan laptop melalui menu Windows.
- **Gunakan software antivirus yang terpercaya:** Virus bisa merusak file sistem operasi.
- **Pastikan driver selalu up-to-date:** Driver yang tidak kompatibel bisa menyebabkan masalah boot.

Semoga artikel ini bermanfaat! Selamat mencoba dan semoga laptop Acer-mu segera kembali normal!
