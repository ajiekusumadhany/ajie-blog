---
title: "3+ Cara Mengatasi Wifi Tidak Tersambung Di Laptop"
date: 2025-11-16
categories: 
  - "laptop"
tags: 
  - "cara"
  - "laptop"
  - "mengatasi"
---

Pernah nggak sih lagi asyik-asyiknya kerja atau nonton film di laptop, eh tiba-tiba WiFi-nya ngadat? Pasti bikin kesel banget, kan? Udah coba restart router, tapi tetep aja WiFi tidak tersambung di laptop. Jangan panik dulu! Masalah ini sering banget terjadi dan biasanya ada solusi yang gampang.

Di artikel ini, kita bakal bahas lebih dari 3 cara mengatasi WiFi tidak tersambung di laptop. Mulai dari yang paling sederhana sampai yang agak teknis, semuanya dikupas tuntas biar kamu bisa langsung praktik dan internetan lagi dengan lancar. Yuk, simak!

## 3+ Cara Mengatasi Wifi Tidak Tersambung Di Laptop

WiFi yang nggak mau nyambung di laptop itu bisa disebabkan banyak hal. Mulai dari masalah driver, pengaturan jaringan, sampai masalah hardware. Tenang, kita coba urutkan solusinya dari yang paling mudah dulu, ya.

### 1\. Cek Koneksi Fisik dan Pengaturan Dasar

Kadang, masalahnya sepele banget dan kita nggak sadar. Sebelum masuk ke hal yang lebih teknis, pastikan dulu hal-hal berikut:

- **Pastikan WiFi di Laptop Aktif:** Cek ikon WiFi di pojok kanan bawah layar. Pastikan ikon tersebut aktif (biasanya berwarna biru atau putih). Kalau mati, klik ikonnya untuk mengaktifkan WiFi.
- **Mode Pesawat (Airplane Mode):** Kadang, tanpa sengaja kita mengaktifkan mode pesawat. Mode ini mematikan semua koneksi nirkabel, termasuk WiFi. Pastikan mode pesawat dalam keadaan mati.
- **Router dan Modem:** Coba restart router dan modem kamu. Cabut kabel power, tunggu sekitar 30 detik, lalu colokkan kembali. Tunggu sampai router dan modem menyala sempurna. Ini seringkali jadi solusi paling ampuh.
- **Kabel:** Periksa semua kabel yang terhubung ke router dan modem. Pastikan semua kabel terpasang dengan benar dan tidak ada yang longgar.
- **WiFi yang Benar:** Pastikan kamu memilih jaringan WiFi yang benar. Periksa nama WiFi (SSID) dan masukkan password yang sesuai. Salah ketik password bisa jadi penyebab utama WiFi tidak tersambung di laptop.

### 2\. Troubleshoot Jaringan Windows

Windows punya fitur troubleshooting yang lumayan ampuh buat mendeteksi dan memperbaiki masalah jaringan. Cara menggunakannya:

- **Buka Troubleshooter:** Klik kanan ikon WiFi di pojok kanan bawah layar, lalu pilih "Troubleshoot problems" atau "Perbaiki masalah".
- **Ikuti Instruksi:** Windows akan otomatis mendeteksi masalah dan memberikan solusi. Ikuti saja instruksi yang muncul di layar. Biasanya, troubleshooter bisa memperbaiki masalah koneksi yang umum.

### 3\. Update atau Reset Driver WiFi

Driver WiFi yang sudah usang atau rusak bisa jadi penyebab WiFi tidak tersambung di laptop. Coba lakukan update atau reset driver WiFi:

- **Buka Device Manager:** Ketik "Device Manager" di kolom pencarian Windows, lalu buka aplikasinya.
- **Cari Network Adapters:** Cari dan perluas kategori "Network adapters".
- **Update Driver:** Klik kanan pada adapter WiFi kamu (biasanya ada kata "Wireless" atau "WiFi" di namanya), lalu pilih "Update driver". Pilih "Search automatically for drivers" agar Windows mencari driver terbaru secara otomatis.
- **Uninstall dan Reinstall Driver:** Jika update driver tidak berhasil, coba uninstall driver. Klik kanan pada adapter WiFi, pilih "Uninstall device", lalu centang "Delete the driver software for this device" jika ada. Setelah itu, restart laptop kamu. Windows akan otomatis menginstall driver WiFi saat laptop menyala kembali.
- **Download Driver dari Website Produsen:** Jika cara di atas masih belum berhasil, coba download driver WiFi terbaru dari website produsen laptop kamu. Biasanya, mereka menyediakan driver yang paling kompatibel dengan hardware laptop kamu.

### 4\. Reset Pengaturan Jaringan

Pengaturan jaringan yang salah konfigurasi juga bisa menyebabkan masalah koneksi WiFi. Coba reset pengaturan jaringan ke default:

- **Buka Command Prompt (Admin):** Ketik "cmd" di kolom pencarian Windows, klik kanan pada "Command Prompt", lalu pilih "Run as administrator".
- **Ketik Perintah:** Ketik perintah berikut satu per satu, lalu tekan Enter setelah setiap perintah:
    - `netsh winsock reset`
    - `netsh int ip reset`
    - `ipconfig /release`
    - `ipconfig /renew`
    - `ipconfig /flushdns`
- **Restart Laptop:** Setelah semua perintah selesai dijalankan, restart laptop kamu.

### 5\. Periksa Pengaturan IP Address

Kadang, laptop kamu tidak mendapatkan IP address yang benar dari router, sehingga WiFi tidak tersambung di laptop. Coba atur IP address secara manual atau otomatis:

- **Buka Network Connections:** Ketik "Network Connections" di kolom pencarian Windows, lalu buka aplikasinya.
- **Pilih Adapter WiFi:** Klik kanan pada adapter WiFi kamu, lalu pilih "Properties".
- **Pilih Internet Protocol Version 4 (TCP/IPv4):** Cari dan pilih "Internet Protocol Version 4 (TCP/IPv4)", lalu klik "Properties".
- **Otomatis (DHCP):** Pilih "Obtain an IP address automatically" dan "Obtain DNS server address automatically". Ini akan membuat laptop kamu mendapatkan IP address dan DNS server secara otomatis dari router.
- **Manual:** Jika cara otomatis tidak berhasil, kamu bisa mencoba mengatur IP address secara manual. Tanyakan IP address, subnet mask, default gateway, dan DNS server ke penyedia layanan internet (ISP) kamu atau lihat di pengaturan router. Masukkan informasi tersebut ke kolom yang sesuai.

### 6\. Periksa Firewall dan Antivirus

Firewall atau antivirus yang terlalu ketat bisa memblokir koneksi WiFi. Coba nonaktifkan sementara firewall dan antivirus kamu, lalu coba sambungkan ke WiFi lagi. Jika berhasil, berarti firewall atau antivirus kamu yang bermasalah.

- **Nonaktifkan Firewall:** Buka "Windows Defender Firewall" di Control Panel, lalu pilih "Turn Windows Defender Firewall on or off". Pilih "Turn off Windows Defender Firewall (not recommended)" untuk domain network, private network, dan public network.
- **Nonaktifkan Antivirus:** Cari ikon antivirus kamu di system tray (pojok kanan bawah layar), klik kanan, lalu pilih opsi untuk menonaktifkan sementara (biasanya ada pilihan "Disable" atau "Turn off").

**Perhatian:** Jangan lupa aktifkan kembali firewall dan antivirus kamu setelah selesai mencoba, ya. Ini penting untuk keamanan laptop kamu.

### 7\. Periksa Hardware WiFi

Jika semua cara di atas sudah dicoba dan WiFi tidak tersambung di laptop, kemungkinan ada masalah dengan hardware WiFi laptop kamu.

- **Periksa Kartu WiFi:** Jika laptop kamu menggunakan kartu WiFi internal, coba periksa apakah kartu tersebut terpasang dengan benar. Buka casing laptop (hati-hati, ya, atau minta bantuan teknisi) dan pastikan kartu WiFi terpasang dengan baik di slotnya.
- **Coba USB WiFi Adapter:** Sebagai alternatif, kamu bisa mencoba menggunakan USB WiFi adapter. Adapter ini bisa jadi solusi sementara jika kartu WiFi internal kamu bermasalah.

### 8\. Update BIOS

Meskipun jarang terjadi, BIOS yang sudah usang juga bisa menyebabkan masalah kompatibilitas dengan hardware WiFi. Coba update BIOS laptop kamu ke versi terbaru.

**Perhatian:** Update BIOS adalah proses yang berisiko. Pastikan kamu mengikuti instruksi dengan benar dan memiliki backup data sebelum melakukan update BIOS. Jika ragu, sebaiknya minta bantuan teknisi.

## Kesimpulan

WiFi tidak tersambung di laptop memang menjengkelkan, tapi dengan mencoba langkah-langkah di atas, kamu seharusnya bisa menemukan solusinya. Mulai dari memeriksa hal-hal dasar seperti memastikan WiFi aktif, sampai mencoba solusi yang lebih teknis seperti update driver atau reset pengaturan jaringan.

Punya pengalaman lain dalam mengatasi masalah WiFi di laptop? Share di kolom komentar, yuk! Siapa tahu bisa membantu teman-teman lain yang sedang mengalami masalah serupa.

## FAQ (Frequently Asked Questions)

**1\. Kenapa WiFi di laptop saya tiba-tiba tidak terdeteksi?**

Ada beberapa kemungkinan penyebabnya:

- **Driver WiFi bermasalah:** Coba update atau reinstall driver WiFi kamu.
- **Mode pesawat aktif:** Pastikan mode pesawat dalam keadaan mati.
- **Hardware WiFi bermasalah:** Coba periksa kartu WiFi internal atau gunakan USB WiFi adapter.
- **Router bermasalah:** Coba restart router kamu.

**2\. Bagaimana cara mengetahui password WiFi yang sudah tersimpan di laptop?**

- **Buka Network and Sharing Center:** Ketik "Network and Sharing Center" di kolom pencarian Windows, lalu buka aplikasinya.
- **Pilih WiFi:** Klik nama WiFi kamu.
- **Wireless Properties:** Klik "Wireless Properties".
- **Security Tab:** Buka tab "Security", lalu centang "Show characters" untuk melihat password WiFi.

**3\. Apakah mengganti router bisa menyelesaikan masalah WiFi yang sering putus-putus di laptop?**

Tergantung. Jika masalahnya memang ada pada router yang sudah usang atau tidak mendukung standar WiFi terbaru, mengganti router bisa jadi solusi. Tapi, pastikan dulu kamu sudah mencoba solusi lain seperti update firmware router, mengubah channel WiFi, atau memposisikan router di tempat yang strategis.

**4\. Kenapa setelah update Windows, WiFi saya jadi tidak bisa connect?**

Kemungkinan ada masalah kompatibilitas antara driver WiFi yang lama dengan versi Windows yang baru. Coba update driver WiFi kamu ke versi terbaru yang kompatibel dengan Windows versi kamu. Kamu bisa download driver terbaru dari website produsen laptop kamu.
