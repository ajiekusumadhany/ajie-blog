---
title: "Apa Itu Mark-and-Sweep Algorithm Dalam Garbage Collection?"
date: 2025-09-10
categories: 
  - "pemrograman"
tags: 
  - "pemrograman"
---

Pernahkah Anda bertanya-tanya ke mana perginya memori yang tidak lagi digunakan oleh program Anda? Bayangkan tumpukan sampah yang terus menggunung, lama kelamaan membuat segalanya jadi lambat dan berantakan. Nah, di dunia pemrograman, inilah yang disebut dengan "memory leak". Untungnya, ada pahlawan tanpa tanda jasa yang siap membersihkan kekacauan ini: **Mark-and-Sweep Algorithm** dalam _garbage collection_.

Artikel ini akan mengupas tuntas **apa itu Mark-and-Sweep Algorithm** dan bagaimana ia bekerja secara ajaib untuk membebaskan memori yang tak terpakai. Bersiaplah untuk menyelami dunia _garbage collection_ yang seru dan penting!

## Apa Itu Garbage Collection?

Sebelum membahas lebih dalam tentang **Mark-and-Sweep Algorithm**, mari kita pahami dulu apa itu _garbage collection_. Secara sederhana, _garbage collection_ adalah proses otomatis yang membebaskan memori yang tidak lagi digunakan oleh program.

Bayangkan Anda sedang bermain dengan balok susun. Setelah selesai, Anda tidak mungkin membiarkan balok-balok itu berserakan di mana-mana, kan? Anda akan membereskannya dan menyimpannya kembali ke dalam kotak. Begitu pula dengan _garbage collection_, ia membereskan memori yang tidak terpakai dan mengembalikannya agar bisa digunakan oleh program lain.

## Mengapa Garbage Collection Penting?

_Garbage collection_ sangat penting karena beberapa alasan:

- **Mencegah Memory Leak:** Tanpa _garbage collection_, program bisa kehabisan memori karena terus menerus membuat objek baru tanpa membebaskan yang lama. Ini bisa menyebabkan program menjadi lambat, bahkan crash.
- **Menyederhanakan Pengembangan:** _Garbage collection_ membebaskan programmer dari tugas manual mengelola memori. Mereka bisa fokus pada logika program tanpa perlu khawatir tentang alokasi dan dealokasi memori.
- **Meningkatkan Stabilitas:** Dengan mencegah _memory leak_, _garbage collection_ membantu meningkatkan stabilitas dan keandalan program.

## Apa Itu Mark-and-Sweep Algorithm dalam Garbage Collection?

**Mark-and-Sweep Algorithm** adalah salah satu algoritma _garbage collection_ yang paling umum dan mendasar. Algoritma ini bekerja dalam dua fase utama:

1. **Mark Phase (Fase Penandaan):** Pada fase ini, _garbage collector_ (pengumpul sampah) menelusuri semua objek yang dapat dijangkau (reachable) dari _root set_. _Root set_ adalah sekumpulan objek yang dijamin hidup, seperti variabel global dan objek yang sedang digunakan oleh stack. Setiap objek yang dapat dijangkau ditandai sebagai "hidup".
2. **Sweep Phase (Fase Penyapuan):** Pada fase ini, _garbage collector_ menyapu seluruh memori _heap_. Objek yang tidak ditandai sebagai "hidup" dianggap sebagai "sampah" dan memorinya dibebaskan.

Sederhananya, algoritma ini mencari semua barang yang masih dipakai, lalu membuang sisanya.

## Bagaimana Mark-and-Sweep Algorithm Bekerja?

Mari kita telaah lebih dalam bagaimana **Mark-and-Sweep Algorithm** bekerja:

### 1\. Fase Penandaan (Mark Phase)

- **Mulai dari Root Set:** _Garbage collector_ mulai dari _root set_ dan menelusuri semua objek yang direferensikan oleh objek-objek tersebut.
- **Penandaan Objek:** Setiap objek yang dikunjungi ditandai sebagai "hidup". Penandaan ini biasanya dilakukan dengan mengubah satu bit di header objek.
- **Rekursi:** Proses penelusuran dan penandaan berlanjut secara rekursif sampai semua objek yang dapat dijangkau telah ditandai.

### 2\. Fase Penyapuan (Sweep Phase)

- **Iterasi Melalui Heap:** _Garbage collector_ mengiterasi melalui seluruh memori _heap_.
- **Pemeriksaan Tanda:** Untuk setiap objek, _garbage collector_ memeriksa apakah objek tersebut ditandai sebagai "hidup".
- **Pembersihan Sampah:** Jika objek tidak ditandai, maka objek tersebut dianggap sebagai sampah dan memorinya dibebaskan. Memori yang dibebaskan ini kemudian dapat digunakan untuk mengalokasikan objek baru.

## Contoh Sederhana Mark-and-Sweep Algorithm

Bayangkan sebuah jaringan pertemanan di media sosial. _Root set_ adalah akun Anda. Fase penandaan akan menelusuri semua teman Anda, teman dari teman Anda, dan seterusnya, menandai mereka sebagai "hidup". Fase penyapuan kemudian akan menghapus akun-akun yang tidak terhubung dengan Anda sama sekali (tidak ditandai).

## Kelebihan dan Kekurangan Mark-and-Sweep Algorithm

Seperti algoritma lainnya, **Mark-and-Sweep Algorithm** memiliki kelebihan dan kekurangan:

### Kelebihan:

- **Sederhana dan Mudah Diimplementasikan:** Algoritma ini relatif mudah dipahami dan diimplementasikan.
- **Tidak Memerlukan Ruang Tambahan yang Signifikan:** Algoritma ini hanya memerlukan sedikit ruang tambahan untuk penandaan objek.
- **Dapat Menangani Circular References:** Algoritma ini dapat menangani _circular references_ (objek yang saling mereferensikan satu sama lain), yang merupakan masalah bagi beberapa algoritma _garbage collection_ lainnya.

### Kekurangan:

- **Pause Times:** Proses _garbage collection_ dapat menyebabkan jeda (pause) dalam eksekusi program, terutama pada sistem dengan memori besar.
- **Fragmentasi Memori:** Algoritma ini dapat menyebabkan fragmentasi memori, di mana memori terbagi menjadi blok-blok kecil yang tidak berdekatan, sehingga sulit untuk mengalokasikan objek yang besar.
- **Membutuhkan Waktu yang Cukup Lama:** Fase penandaan dan penyapuan dapat memakan waktu yang cukup lama, terutama pada sistem dengan banyak objek.

## Optimasi Mark-and-Sweep Algorithm

Beberapa teknik optimasi dapat digunakan untuk meningkatkan kinerja **Mark-and-Sweep Algorithm**, seperti:

- **Incremental Garbage Collection:** Melakukan _garbage collection_ secara bertahap, sehingga mengurangi _pause times_.
- **Generational Garbage Collection:** Membagi memori menjadi beberapa generasi, di mana objek yang lebih baru lebih sering dikumpulkan sampahnya daripada objek yang lebih lama.
- **Compaction:** Memindahkan objek-objek yang hidup ke satu area memori, sehingga mengurangi fragmentasi.

## Alternatif Mark-and-Sweep Algorithm

Selain **Mark-and-Sweep Algorithm**, ada beberapa algoritma _garbage collection_ lain yang umum digunakan, seperti:

- **Reference Counting:** Menghitung jumlah referensi ke setiap objek. Jika jumlah referensi menjadi nol, maka objek tersebut dianggap sebagai sampah.
- **Copying Garbage Collection:** Membagi memori menjadi dua area. Objek yang hidup disalin dari satu area ke area lain, dan area yang lama dibebaskan.

## Kesimpulan

**Mark-and-Sweep Algorithm** adalah fondasi penting dalam dunia _garbage collection_. Memahami cara kerjanya membantu kita mengapresiasi bagaimana program kita dapat berjalan dengan efisien dan stabil. Meskipun memiliki beberapa kekurangan, algoritma ini tetap menjadi pilihan populer dan terus dikembangkan untuk mengatasi tantangan pengelolaan memori modern.

Apakah Anda pernah mengalami masalah _memory leak_ dalam proyek Anda? Bagikan pengalaman Anda di kolom komentar!

## FAQ (Frequently Asked Questions)

**1\. Apa itu Root Set dalam Mark-and-Sweep Algorithm?**

_Root set_ adalah sekumpulan objek yang dijamin hidup dan menjadi titik awal penelusuran dalam fase penandaan. Contoh _root set_ adalah variabel global, objek yang sedang digunakan oleh stack, dan objek yang direferensikan oleh _garbage collector_ itu sendiri.

**2\. Mengapa Mark-and-Sweep Algorithm dapat menyebabkan Pause Times?**

Fase penandaan dan penyapuan dalam **Mark-and-Sweep Algorithm** membutuhkan waktu untuk menelusuri dan memproses seluruh memori _heap_. Selama proses ini, program mungkin perlu dihentikan sementara (pause) untuk menghindari konflik dengan _garbage collector_.

**3\. Bagaimana cara mengurangi Fragmentasi Memori yang disebabkan oleh Mark-and-Sweep Algorithm?**

Salah satu cara untuk mengurangi fragmentasi memori adalah dengan menggunakan teknik _compaction_. _Compaction_ memindahkan objek-objek yang hidup ke satu area memori, sehingga membebaskan blok-blok memori yang lebih besar dan berdekatan.
