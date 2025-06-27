---
title: "Program C++: Membuat Persegi Panjang Bintang"
date: 2023-04-01
categories: 
  - "cpp"
---

Persegi panjang merupakan salah satu bentuk dasar dalam geometri yang sering digunakan dalam pemrograman.

Dalam artikel ini, kita akan membahas bagaimana cara membuat persegi panjang bintang menggunakan bahasa pemrograman C++.

Sebelum memulai, pastikan bahwa Anda sudah menginstal perangkat lunak atau IDE bahasa pemrograman C++ seperti Dev-C++ atau Code::Blocks.

Setelah itu, buatlah program baru dengan memilih File > New > Project pada menu utama. Pilih Console Application dan beri nama file program dengan "persegi\_panjang.cpp". Kemudian klik OK untuk membuat file baru.

**Langkah pertama** dalam membuat program ini adalah mendeklarasikan variabel untuk menyimpan nilai panjang dan lebar persegi panjang.

Variabel ini dapat dideklarasikan menggunakan tipe data integer.

**Berikut adalah contoh kode untuk mendeklarasikan variabel:**

```
int panjang, lebar;

```

Selanjutnya, kita dapat meminta pengguna untuk memasukkan nilai panjang dan lebar persegi panjang menggunakan fungsi cin.

Fungsi cin digunakan untuk membaca input dari pengguna dan menyimpannya ke dalam variabel yang sudah dideklarasikan sebelumnya.

**Berikut adalah contoh kode untuk meminta pengguna memasukkan nilai panjang dan lebar:**

```
cout << "Masukkan nilai panjang: ";
cin >> panjang;

cout << "Masukkan nilai lebar: ";
cin >> lebar;

```

Setelah nilai panjang dan lebar sudah dimasukkan oleh pengguna, maka kita dapat mulai membuat persegi panjang bintang menggunakan nested loop.

Nested loop adalah konsep di mana sebuah loop terletak di dalam loop lainnya. Hal ini berguna untuk mengulang kode secara berulang-ulang dengan berbagai kondisi yang berbeda.

Pada program ini, kita akan menggunakan dua buah nested loop, di mana loop pertama digunakan untuk mencetak baris dan loop kedua digunakan untuk mencetak bintang pada setiap baris.

**Baca Juga**: [Program C++: Membuat Persegi Bintang](https://ajiekusumadhany.com/program-cpp-membuat-persegi-bintang/)

**Berikut adalah contoh kode looping untuk membuat persegi panjang bintang:**

```
for (int i = 1; i <= panjang; i++) {
    for (int j = 1; j <= lebar; j++) {
        cout << "*";
    }
    cout << endl;
}

```

Pada kode di atas, **variabel i** digunakan untuk mengatur jumlah baris yang dicetak dan **variabel j** digunakan untuk mengatur jumlah bintang yang dicetak pada setiap baris.

Kita menggunakan **operator <=** untuk menentukan kondisi ulang loop, sehingga loop akan berjalan selama nilai i dan j masih kurang dari atau sama dengan nilai panjang dan lebar yang dimasukkan oleh pengguna.

Setelah kode tersebut dijalankan, maka hasilnya akan berupa persegi panjang bintang dengan panjang dan lebar yang sudah dimasukkan oleh pengguna.

## Kode C++ Membuat Persegi Panjang Bintang

Berikut adalah kode lengkap untuk program C++ membuat persegi panjang bintang:

```
#include <iostream>
using namespace std;

int main() {
    int panjang, lebar;

    cout << "Masukkan nilai panjang: ";
    cin >> panjang;

    cout << "Masukkan nilai lebar: ";
    cin >> lebar;

    for (int i = 1; i <= lebar; i++) 
    {
        for (int j = 1; j<= panjang; j++) 
        {
           cout << "*";
        }
           cout << endl;
    }
return 0;
}
```

Ada beberapa hal yang perlu diperhatikan saat membuat program persegi panjang bintang ini.

**Pertama**, pastikan bahwa variabel panjang dan lebar sudah dideklarasikan dengan benar dan mempunyai nilai yang valid.

**Kedua**, perhatikan penggunaan nested loop dengan benar dan gunakan operator <= untuk menentukan kondisi ulang loop.

**Ketiga**, jangan lupa untuk menggunakan cout dan endl untuk mencetak bintang pada setiap baris dan membuat baris baru setelah satu baris selesai dicetak.

Dalam mengembangkan kemampuan pemrograman, membuat program persegi panjang bintang ini hanya merupakan salah satu dari banyak hal yang bisa dipelajari.

Dalam pemrograman, terdapat banyak konsep dan teknologi yang harus dipelajari untuk menghasilkan program yang baik dan efektif.

Selain itu, program ini dapat dimodifikasi untuk mencetak berbagai bentuk lainnya seperti segitiga, trapesium, dan sebagainya.

Dengan menggunakan konsep nested loop, maka berbagai bentuk tersebut dapat dicetak dengan mudah dan efisien.

## Kesimpulan

Program C++ membuat persegi panjang bintang merupakan contoh sederhana dari pemrograman dengan menggunakan bahasa C++.

Meskipun sederhana, program ini dapat membantu dalam mempelajari konsep pemrograman dasar.

Oleh karena itu, bagi Anda yang ingin mempelajari pemrograman, program ini bisa menjadi langkah awal untuk memulai perjalanan belajar pemrograman.
