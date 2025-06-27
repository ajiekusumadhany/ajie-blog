---
title: "Cara Mengatasi Error Xampp Mysql Shutdown Unexpectedly"
date: 2023-07-14
categories: 
  - "pemrograman"
---

Saat mengalami hal tersebut saya melakukan hal ini dan berhasil:

1. Ganti nama folder **mysql/data** menjadi **mysql/data\_old**
2. Buat folder salinan **mysql/backup** dan beri nama sebagai **mysql/data**
3. Salin semua folder database Anda dari **mysql/data\_old** ke **mysql/data** (kecuali folder mysql, performance\_schema, dan phpmyadmin)
4. Salin file **mysql/data\_old/ibdata1** ke folder **mysql/data**
5. Coba jalankan MySQL dari panel kontrol XAMPP

Dengan melakukan langkah-langkah diatas seharusnya error sudah bisa teratasi.

[![](images/Screenshot%20%2818%29.png)](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiER-XgNhvDfEXZnZTdFQUCAaZNroAkPyawSHb5YvZOceHkxloifTqE0gT9JHGmLBazgEgdr6BRh85BO9almbpDB95598uiYXGkAU1VKENKakT8hwMnqn0PB8meKEtkWea6Al1JAGQC2LkjHbkOL0y3J3iK257o_V25wUdSCbP8UyfYpscmCCLYXgF18QeI/s1600/Screenshot%20%2818%29.png)
