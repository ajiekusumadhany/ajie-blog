---
title: "Program C++: Membuat Persegi Bintang"
date: 2023-04-01
categories: 
  - "cpp"
---

Persegi bintang adalah bentuk dasar dalam dunia pemrograman, karena dapat menjadi fondasi dari bentuk-bentuk geometris yang lebih kompleks.

Dalam artikel ini, kita akan membahas bagaimana cara membuat persegi bintang menggunakan bahasa pemrograman C++.

Program ini akan memungkinkan pengguna untuk memasukkan jumlah baris dan kolom dari persegi yang ingin dicetak, dan kemudian mencetak persegi bintang sesuai dengan jumlah baris dan kolom yang dimasukkan.

## Cara Membuat Persegi Bintang

Mari kita mulai dengan membuat program C++ yang sederhana untuk mencetak persegi bintang dengan jumlah baris dan kolom yang telah ditentukan:

```
#include <iostream>
using namespace std;

int main()
{
    int baris, kolom;
    cout << "Masukkan jumlah baris: ";
    cin >> baris;

    cout << "Masukkan jumlah kolom: ";
    cin >> kolom;

    for(int i = 0; i < baris; i++)
    {
        for(int j = 0; j < kolom; j++)
        {
            cout << "* ";
        }
        cout << endl;
    }

    return 0;
}

```

## Penjelasan

Pertama, program akan meminta pengguna untuk memasukkan jumlah baris dan kolom yang diinginkan menggunakan fungsi cin dari C++.

Kemudian, program akan menggunakan loop for untuk mencetak baris dan kolom persegi bintang sesuai dengan jumlah yang dimasukkan.

Loop for pertama akan mencetak jumlah baris yang dimasukkan oleh pengguna, sedangkan loop for kedua akan mencetak jumlah kolom yang dimasukkan.

Dalam loop for kedua, penggunaan cout << "\* "; akan mencetak bintang di setiap kolom dan cout << endl; akan mencetak baris baru setelah loop for kedua selesai dieksekusi.

Mari kita lihat bagaimana program ini bekerja dengan menguji dengan input 3 baris dan 4 kolom:

```
Masukkan jumlah baris: 3
Masukkan jumlah kolom: 4
* * * *
* * * *
* * * *

```

Program berhasil mencetak persegi bintang dengan 3 baris dan 4 kolom seperti yang diminta pengguna.

Namun, program ini memiliki kelemahan yaitu jika pengguna memasukkan angka negatif atau nol untuk jumlah baris atau kolom, maka program akan tetap mencetak persegi bintang tanpa adanya baris atau kolom.

Untuk mengatasi masalah ini, kita perlu menambahkan kode untuk memeriksa apakah jumlah baris atau kolom yang dimasukkan adalah bilangan positif.

Jika jumlah baris atau kolom kurang dari atau sama dengan 0, program akan meminta pengguna untuk memasukkan jumlah yang valid.

**Baca Juga**: [Program C++: Membuat Persegi Panjang Bintang](https://ajiekusumadhany.com/cpp-membuat-persegi-panjang-bintang/)

**Berikut adalah kode program C++ yang telah diperbarui:**

```
#include <iostream>
using namespace std;

int main()
{
    int baris, kolom;

    do {
        cout << "Masukkan jumlah baris: ";
        cin >> baris;

        if(baris <= 0) {
            cout << "Jumlah baris harus positif.\n";
        }
    } while(baris <= 0);

    do {
        cout << "Masukkan jumlah kolom: ";
        cin >> kolom;

        if(kolom <= 0) {
            cout << "Jumlah kolom harus positif.\n";
        }
    } while(kolom <= 0);

    for(int i = 0; i < kolom; i++)
    {
    for(int j = 0; j < kolom; j++)
    {
        cout << "* ";
    }
        cout << endl;
    }
return 0;
}
```

Dalam program yang diperbarui ini, kami menggunakan loop do-while untuk memastikan bahwa jumlah baris dan kolom yang dimasukkan selalu positif.

Jika pengguna memasukkan angka negatif atau nol, program akan mencetak pesan kesalahan dan meminta pengguna untuk memasukkan jumlah yang valid.

Kami juga menggunakan endl untuk mencetak baris baru setelah setiap baris persegi bintang selesai dicetak. Ini memberikan tampilan persegi bintang yang lebih mudah dibaca.

Program ini sangat sederhana dan mudah dimengerti, bahkan oleh mereka yang baru memulai dengan bahasa pemrograman C++.

Namun, ini hanya merupakan contoh dasar dari bagaimana membuat program persegi bintang menggunakan bahasa pemrograman C++.

Ada banyak cara untuk memperluas program ini dan mencetak persegi bintang dengan pola yang lebih kompleks atau bahkan memperluas ke bentuk geometris lainnya.

## Kesimpulan

Jadi, itulah cara membuat program C++ sederhana untuk mencetak persegi bintang. Ada banyak variasi dan cara yang berbeda untuk mencetak pola persegi bintang, dan semuanya tergantung pada kebutuhan dan preferensi Anda.
