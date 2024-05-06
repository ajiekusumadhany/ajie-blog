---
title: 'Program C++: Membuat Segitiga Bintang'
date: Sun, 02 Apr 2023 06:21:02 +0000
draft: false
tags: ['C++', 'Pemrograman']
---

Pemrograman C++ merupakan salah satu jenis pemrograman yang paling sering digunakan dalam membuat program komputer. Pada artikel kali ini, kita akan membahas bagaimana cara membuat program C++ untuk membuat segitiga bintang. Segitiga bintang merupakan salah satu bentuk bangun datar yang paling sederhana dan sering digunakan dalam pemrograman. Dalam membuat program C++ untuk membuat segitiga bintang, kita dapat menggunakan perulangan dan logika sederhana untuk menghasilkan pola yang diinginkan.

Langkah Membuat Segitiga Bintang
--------------------------------

Berikut adalah langkah-langkah untuk membuat segitiga bintang dengan bahasa c++:

### 1\. Tentukan jumlah baris dan kolom

Dalam membuat segitiga bintang, kita perlu menentukan jumlah baris dan kolom yang akan digunakan. Jumlah baris menentukan tinggi dari segitiga, sedangkan jumlah kolom menentukan lebar dari segitiga.

### 2\. Gunakan perulangan untuk menghasilkan pola bintang

Setelah menentukan jumlah baris dan kolom, kita dapat menggunakan perulangan untuk menghasilkan pola bintang yang diinginkan. Ada beberapa jenis perulangan yang dapat digunakan, seperti for loop, while loop, dan do-while loop. Pada contoh program ini, kita akan menggunakan for loop.

### 2\. Gunakan logika sederhana untuk menghasilkan pola bintang

Selain menggunakan perulangan, kita juga perlu menggunakan logika sederhana untuk menghasilkan pola bintang yang diinginkan. Pada contoh program ini, kita akan menggunakan logika sederhana yang memanfaatkan hubungan antara baris dan kolom dalam segitiga. Berikut adalah contoh **program C++ untuk membuat segitiga bintang** dengan 5 baris:```
#include <iostream>
using namespace std;

int main() {
   int n = 5; // jumlah baris

   for(int i = 1; i <= n; i++) { // perulangan untuk baris
      for(int j = 1; j <= n-i; j++) { // perulangan untuk spasi
         cout << " ";
      }
      for(int k = 1; k <= 2\*i-1; k++) { // perulangan untuk bintang
         cout << "\*";
      }
      cout << endl; // baris baru
   }

   return 0;
}

```**Lihat**: [Hasil Program](https://onlinegdb.com/JuASkhsA7) Pada program di atas, kita menggunakan tiga perulangan for loop untuk menghasilkan pola segitiga bintang dengan 5 baris. **Pertama**, kita menggunakan perulangan pertama untuk mengatur jumlah baris yang akan dibuat. **Kemudian**, kita menggunakan perulangan kedua untuk menentukan jumlah spasi yang akan ditampilkan di setiap baris. **Setelah itu**, kita menggunakan perulangan ketiga untuk menampilkan jumlah bintang yang sesuai dengan pola segitiga bintang. Pada program di atas, kita menggunakan operator "<<" untuk menampilkan output di layar. Operator ini digunakan untuk menampilkan nilai yang disimpan dalam variabel, seperti string atau angka. Kita juga menggunakan fungsi endl untuk membuat baris baru setelah menampilkan setiap baris. Hasil dari program di atas adalah segitiga bintang dengan 5 baris:```
    \*
   \*\*\*
  \*\*\*\*\*
 \*\*\*\*\*\*\*
\*\*\*\*\*\*\*\*\*

```Pada contoh program di atas, kita menggunakan jumlah baris yang telah ditentukan Namun, jika kita ingin membuat segitiga bintang dengan jumlah baris yang berbeda, kita dapat dengan mudah mengubah nilai variabel n sesuai dengan keinginan kita. Selain itu, kita juga dapat membuat variasi pola segitiga bintang dengan menggunakan logika sederhana yang berbeda. Sebagai contoh, kita dapat membuat pola segitiga bintang yang memiliki bintang di bagian kiri atau kanan segitiga dengan mengubah logika perulangan pada program di atas. Berikut adalah contoh program C++ untuk membuat segitiga bintang dengan 6 baris dan bintang di bagian kiri segitiga:```
#include <iostream>
using namespace std;

int main() {
   int n = 6; // jumlah baris

   for(int i = 1; i <= n; i++) { // perulangan untuk baris
      for(int j = 1; j <= i; j++) { // perulangan untuk bintang
         cout << "\*";
      }
      cout << endl; // baris baru
   }

   return 0;
}

```**Lihat**: [Hasil Program](https://www.onlinegdb.com/wM7NqaBEc) Pada program di atas, kita menggunakan perulangan for loop untuk menampilkan bintang pada setiap baris. Kita menggunakan variabel i sebagai penghitung baris dan variabel j sebagai penghitung bintang pada setiap baris. Hasil dari program di atas adalah segitiga bintang dengan 6 baris dan bintang di bagian kiri segitiga:```
\*
\*\*
\*\*\*
\*\*\*\*
\*\*\*\*\*
\*\*\*\*\*\*
```Dengan menggunakan logika dan perulangan yang berbeda, kita dapat membuat berbagai variasi pola segitiga bintang yang menarik dan kreatif.

**Baca Juga**: [Program C++: Membuat Segitiga Bintang Terbalik](https://blog.ajiekusumadhany.com/cpp-membuat-segitiga-bintang-terbalik/)

Kesimpulan
----------

Dalam membuat program C++ untuk membuat segitiga bintang, ada beberapa hal yang perlu diperhatikan. **Pertama**, pastikan kita memahami konsep perulangan dan logika sederhana yang digunakan dalam pembuatan pola segitiga bintang. **Kedua**, pastikan kita menggunakan sintaks dan struktur kode yang benar dalam membuat program C++. **Ketiga**, pastikan kita menguji program yang telah dibuat untuk memastikan program berjalan dengan baik dan menghasilkan output yang diinginkan. Dalam mengembangkan kemampuan pemrograman, membuat program C++ untuk membuat segitiga bintang dapat menjadi latihan yang bermanfaat. Selain melatih kemampuan memahami konsep dasar pemrograman, membuat program ini juga dapat membantu kita mengembangkan kemampuan kreativitas dalam menciptakan pola segitiga bintang yang menarik dan berbeda.