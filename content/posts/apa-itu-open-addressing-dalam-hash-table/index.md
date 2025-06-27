---
title: "Apa Itu Open Addressing Dalam Hash Table?"
date: 2025-07-01
categories: 
  - "pemrograman"
tags: 
  - "pemrograman"
---

Pernahkah kamu merasa frustrasi saat mencoba menyimpan data ke dalam struktur data, tapi ternyata slot yang kamu inginkan sudah penuh? Di dunia pemrograman, masalah ini sering terjadi, terutama saat menggunakan _hash table_. Nah, salah satu solusi cerdas untuk mengatasi bentrokan ini adalah dengan teknik yang disebut **open addressing**.

Artikel ini akan membongkar tuntas **apa itu open addressing dalam hash table**, bagaimana cara kerjanya, berbagai jenisnya, kelebihan dan kekurangannya, serta kapan sebaiknya kamu menggunakannya. Siap menyelam lebih dalam? Yuk, kita mulai!

## Memahami Dasar Hash Table

Sebelum kita membahas _open addressing_, mari kita segarkan ingatan tentang _hash table_. Secara sederhana, _hash table_ adalah struktur data yang menyimpan data dalam format _key-value pairs_.

- **Key:** Identifikasi unik untuk setiap data.
- **Value:** Data yang ingin disimpan.

Fungsi _hash_ digunakan untuk mengubah _key_ menjadi indeks dalam array, di mana _value_ akan disimpan. Masalahnya, terkadang dua _key_ yang berbeda bisa menghasilkan indeks yang sama, inilah yang disebut dengan _collision_ atau bentrokan.

## Apa Itu Open Addressing dalam Hash Table?

**Open addressing** adalah salah satu teknik untuk menangani _collision_ dalam _hash table_. Alih-alih menggunakan _linked list_ atau struktur data lain di setiap slot (seperti pada _separate chaining_), _open addressing_ mencari slot kosong lain dalam _hash table_ untuk menyimpan data yang bertabrakan.

Bayangkan sebuah parkiran. Jika tempat parkir yang kamu incar sudah terisi, kamu tidak membuat tempat parkir baru di atasnya, kan? Kamu akan mencari tempat parkir kosong di sekitar area tersebut. Nah, _open addressing_ bekerja dengan prinsip yang sama.

## Jenis-Jenis Open Addressing

Ada beberapa teknik _open addressing_ yang umum digunakan, masing-masing dengan cara yang berbeda dalam mencari slot kosong:

### Linear Probing

_Linear probing_ adalah teknik _open addressing_ yang paling sederhana. Jika terjadi _collision_, teknik ini akan mencari slot kosong berikutnya secara berurutan.

Misalnya, jika kita ingin menyimpan data pada indeks 5, tetapi indeks 5 sudah terisi, _linear probing_ akan mencoba indeks 6, lalu 7, 8, dan seterusnya, hingga menemukan slot kosong.

Kelebihan _linear probing_ adalah implementasinya yang mudah. Namun, ia rentan terhadap _clustering_, yaitu kecenderungan data untuk mengelompok di sekitar area tertentu dalam _hash table_. _Clustering_ dapat memperlambat proses pencarian dan penyisipan data.

### Quadratic Probing

_Quadratic probing_ mencoba mengatasi masalah _clustering_ pada _linear probing_ dengan menggunakan fungsi kuadratik untuk menentukan jarak antara slot yang diperiksa.

Alih-alih mencari slot berikutnya secara berurutan, _quadratic probing_ akan mencari slot dengan jarak 1, 4, 9, 16, dan seterusnya dari indeks awal.

Dengan menggunakan jarak yang lebih bervariasi, _quadratic probing_ dapat mengurangi _clustering_ dan meningkatkan kinerja. Namun, _quadratic probing_ juga memiliki kelemahan, yaitu tidak menjamin akan menemukan slot kosong jika _hash table_ hampir penuh.

### Double Hashing

_Double hashing_ adalah teknik _open addressing_ yang paling canggih. Teknik ini menggunakan dua fungsi _hash_ yang berbeda: satu untuk menentukan indeks awal dan satu lagi untuk menentukan jarak antara slot yang diperiksa.

Jika terjadi _collision_, _double hashing_ akan menggunakan fungsi _hash_ kedua untuk menghitung jarak antara slot yang diperiksa. Dengan menggunakan dua fungsi _hash_ yang independen, _double hashing_ dapat mengurangi _clustering_ secara signifikan dan memberikan kinerja yang lebih baik daripada _linear probing_ dan _quadratic probing_.

Namun, _double hashing_ juga lebih kompleks untuk diimplementasikan. Penting untuk memilih dua fungsi _hash_ yang baik untuk menghindari _clustering_ dan memastikan kinerja yang optimal.

## Kelebihan dan Kekurangan Open Addressing

Seperti teknik lainnya, _open addressing_ memiliki kelebihan dan kekurangan:

**Kelebihan:**

- **Memori Efisien:** Tidak memerlukan memori tambahan untuk menyimpan _pointer_ (seperti pada _separate chaining_). Semua data disimpan langsung di dalam _hash table_.
- **Implementasi Relatif Sederhana:** Terutama _linear probing_.
- **Cache Friendly:** Data disimpan secara berdekatan dalam memori, yang dapat meningkatkan kinerja karena _cache_ lebih efektif.

**Kekurangan:**

- **Rentan terhadap Clustering:** Terutama _linear probing_.
- **Kinerja Menurun saat Hash Table Hampir Penuh:** Pencarian slot kosong bisa menjadi sangat lambat.
- **Penghapusan Data Lebih Kompleks:** Menghapus data bisa meninggalkan "lubang" yang perlu ditangani dengan hati-hati agar tidak mengganggu pencarian data selanjutnya.

## Kapan Sebaiknya Menggunakan Open Addressing?

_Open addressing_ cocok digunakan dalam situasi berikut:

- **Memori Terbatas:** Ketika penggunaan memori harus dioptimalkan.
- **Data Cenderung Statis:** Ketika data jarang ditambahkan atau dihapus.
- **Kinerja Cache Penting:** Ketika kinerja _cache_ menjadi prioritas.

Namun, jika data sering ditambahkan atau dihapus, atau jika _hash table_ sering kali hampir penuh, _separate chaining_ mungkin menjadi pilihan yang lebih baik.

## Kesimpulan

**Open addressing** adalah teknik yang efektif untuk menangani _collision_ dalam _hash table_, terutama ketika memori terbatas dan kinerja _cache_ penting. Memahami berbagai jenis _open addressing_ (linear probing, quadratic probing, dan double hashing) serta kelebihan dan kekurangannya akan membantu kamu memilih teknik yang paling sesuai dengan kebutuhan aplikasi kamu.

Teknik mana yang paling kamu sukai? Atau apakah kamu memiliki pengalaman menarik dengan _open addressing_ yang ingin kamu bagikan? Mari kita diskusikan di kolom komentar!

## FAQ

**1\. Apa perbedaan utama antara open addressing dan separate chaining?**

Perbedaan utama terletak pada cara penanganan _collision_. _Open addressing_ mencari slot kosong lain di dalam _hash table_, sedangkan _separate chaining_ menggunakan _linked list_ (atau struktur data lain) di setiap slot untuk menyimpan data yang bertabrakan.

**2\. Bagaimana cara menghapus data dalam hash table yang menggunakan open addressing?**

Menghapus data dalam _open addressing_ lebih kompleks karena meninggalkan "lubang". Salah satu cara adalah dengan menandai slot yang dihapus sebagai "dihapus" (misalnya, dengan menggunakan nilai khusus). Saat mencari data, kita harus melewati slot yang ditandai sebagai "dihapus". Namun, saat menyisipkan data baru, kita dapat menggunakan slot yang ditandai sebagai "dihapus".

**3\. Apa yang terjadi jika hash table sudah penuh saat menggunakan open addressing?**

Jika _hash table_ sudah penuh, penyisipan data baru akan gagal. Penting untuk memastikan bahwa _hash table_ memiliki ukuran yang cukup besar untuk menampung data yang diharapkan. Atau, kamu bisa menggunakan teknik _rehashing_ untuk membuat _hash table_ yang lebih besar dan memindahkan semua data ke _hash table_ yang baru.
