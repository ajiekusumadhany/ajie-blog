---
title: "Program C++: Membuat Piramida Bintang"
date: 2023-04-04
categories: 
  - "cpp"
---

Piramida bintang adalah salah satu pola umum yang sering digunakan dalam pemrograman, termasuk dalam pemrograman C++.

Pola ini terdiri dari barisan bintang yang membentuk piramida segitiga terbalik. Piramida bintang dapat dibuat dengan menggunakan konsep loop atau perulangan dalam C++.

Dalam artikel ini, kita akan membahas bagaimana membuat program C++ untuk membuat piramida bintang.

## Membuat Piramida Bintang dengan C++

**Langkah pertama** dalam membuat program piramida bintang adalah dengan menentukan tinggi atau ukuran piramida yang akan dibuat.

Misalnya, jika kita ingin membuat piramida dengan tinggi 5, maka kita akan menggunakan variabel tinggi=5 dalam program.

Berikut ini adalah contoh program sederhana untuk membuat piramida bintang dengan menggunakan loop for:

```
#include <iostream>
using namespace std;

int main() {
    int tinggi = 5;
    for(int i=1; i<=tinggi; i++) {
        // Membuat spasi di setiap baris
        for(int j=1; j<=tinggi-i; j++) {
            cout << " ";
        }

        // Membuat bintang di setiap baris
        for(int k=1; k<=(2*i-1); k++) {
            cout << "*";
        }

        // Pindah ke baris baru setiap selesai membuat baris bintang
        cout << endl;
    }

    return 0;
}

```

## Penjelasan Program

Mari kita bahas bagaimana program ini bekerja. Pertama, kita menentukan tinggi piramida dengan menggunakan variabel tinggi=5.

Kemudian, kita menggunakan loop for untuk membuat setiap baris dari piramida. Loop pertama untuk variabel i, dimulai dari 1 hingga mencapai tinggi piramida. Ini digunakan untuk menghitung berapa banyak baris yang akan dibuat.

Selanjutnya, kita menggunakan loop kedua untuk variabel j, dimulai dari 1 hingga mencapai tinggi-i. Loop ini digunakan untuk membuat spasi di setiap baris sebelum membuat bintang. Jumlah spasi yang dibuat akan berkurang seiring dengan naiknya baris pada piramida.

Loop ketiga digunakan untuk variabel k, dimulai dari 1 hingga mencapai (2\*i-1). Loop ini digunakan untuk membuat bintang di setiap baris. Jumlah bintang yang dibuat akan bertambah seiring dengan naiknya baris pada piramida.

Setelah membuat baris bintang dan spasi, kita menggunakan cout << endl; untuk pindah ke baris baru dan memulai pembuatan baris baru pada piramida.

**Baca Juga**: [Program C++: Membuat Segitiga Bintang Terbalik](https://ajiekusumadhany.com/cpp-membuat-segitiga-bintang-terbalik/)

## Kesimpulan

Membuat piramida bintang adalah salah satu latihan umum dalam pemrograman. Dalam artikel ini, kita telah membahas bagaimana membuat program C++ untuk membuat piramida bintang dengan menggunakan konsep loop atau perulangan.

Program ini dapat dengan mudah dimodifikasi untuk membuat piramida bintang dengan tinggi yang berbeda.
