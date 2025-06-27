---
title: "Program C++ Untuk Menentukan Bilangan Ganjil Kelipatan 7"
date: 2023-03-27
categories: 
  - "cpp"
---

Bilangan ganjil kelipatan 7 adalah bilangan bulat positif yang tidak habis dibagi oleh 2 dan merupakan kelipatan dari 7. Contohnya adalah 7, 21, 35, 49, dan seterusnya.

Dalam artikel ini, kita akan membuat program C++ untuk menentukan apakah sebuah bilangan bulat positif merupakan bilangan ganjil kelipatan 7 atau tidak.

## Membuat Program C++ Menentukan Bilangan Ganjil Kelipatan 7

Berikut adalah langkah-langkah untuk membuat program C++ menentukan apakah suatu bilangan termasuk bilangan ganjil kelipatan 7 atau bukan.

### Langkah 1: Menentukan Bilangan Ganjil

Pertama-tama, kita perlu menentukan apakah bilangan yang diinputkan adalah bilangan ganjil atau bukan. Untuk menentukan hal tersebut, kita bisa menggunakan operator modulus (%).

Operator modulus akan menghasilkan sisa pembagian dari dua bilangan. Jika sisa pembagian antara bilangan dengan 2 sama dengan 1, maka bilangan tersebut adalah bilangan ganjil.

Jika sisa pembagian sama dengan 0, maka bilangan tersebut adalah bilangan genap.

Berikut adalah contoh kode C++ untuk menentukan apakah sebuah bilangan adalah bilangan ganjil atau tidak:

```
#include <iostream>
using namespace std;

int main() {
    int bilangan;
    cout << "Masukkan sebuah bilangan: ";
    cin >> bilangan;

if (bilangan % 2 == 1) {
    cout << "Bilangan tersebut adalah bilangan ganjil." << endl;
} else {
    cout << "Bilangan tersebut adalah bilangan genap." << endl;
}
    return 0;
}
```

### Langkah 2: Menentukan Bilangan Kelipatan 7

Setelah menentukan apakah bilangan tersebut ganjil atau genap, kita perlu menentukan apakah bilangan tersebut merupakan kelipatan dari 7 atau tidak.

Untuk menentukan hal tersebut, kita bisa menggunakan operator modulus lagi. Kali ini, kita akan membandingkan sisa pembagian bilangan dengan 7.

Jika sisa pembagian sama dengan 0, maka bilangan tersebut merupakan kelipatan dari 7.

Jika sisa pembagian tidak sama dengan 0, maka bilangan tersebut bukan merupakan kelipatan dari 7.

Berikut adalah contoh kode C++ untuk menentukan apakah sebuah bilangan adalah kelipatan 7 atau tidak:

```
#include <iostream>
using namespace std;

int main() {
    int bilangan;
    cout << "Masukkan sebuah bilangan: ";
    cin >> bilangan;

if (bilangan % 7 == 0) {
    cout << "Bilangan tersebut adalah kelipatan 7." << endl;
} else {
    cout << "Bilangan tersebut bukan kelipatan 7." << endl;
}

    return 0;
}

```

 

### Langkah 3: Menggabungkan Kedua Fungsi

Sekarang, kita telah berhasil menentukan apakah bilangan tersebut ganjil atau genap dan kelipatan 7 atau tidak.  Kita perlu menggabungkan kedua fungsi tersebut menjadi satu program C++.

Berikut adalah contoh kode C++ lengkap untuk menentukan apakah sebuah bilangan adalah bilangan ganjil kelipatan 7 atau tidak:

```
#include <iostream>
using namespace std;

int main() {
    int bilangan;
    cout << "Masukkan sebuah bilangan: ";
    cin >> bilangan;

    if (bilangan % 2 == 1 && bilangan % 7 == 0) {
        cout << "Bilangan tersebut adalah bilangan ganjil kelipatan 7." << endl;
    } else {
        cout << "Bilangan tersebut bukan bilangan ganjil kelipatan 7." << endl;
    }
    
    return 0;
}

```

Kode di atas akan meminta pengguna untuk memasukkan sebuah bilangan bulat. Kemudian, program akan menentukan apakah bilangan tersebut ganjil atau genap dan kelipatan 7 atau tidak.

Jika bilangan tersebut ganjil dan kelipatan 7, maka program akan mencetak "Bilangan tersebut adalah bilangan ganjil kelipatan 7".

Jika tidak, maka program akan mencetak "Bilangan tersebut bukan bilangan ganjil kelipatan 7".

**Baca Juga**: [Program C++: Membuat Segitiga Bintang](https://ajiekusumadhany.com/program-cpp-membuat-segitiga-bintang/)

## Kesimpulan

Dalam artikel ini, kita telah membuat program C++ untuk menentukan apakah sebuah bilangan bulat positif merupakan bilangan ganjil kelipatan 7 atau tidak.

Kita menggunakan operator modulus untuk menentukan apakah bilangan tersebut ganjil atau genap, dan untuk menentukan apakah bilangan tersebut merupakan kelipatan dari 7 atau tidak.

Dengan program ini, kita dapat mengetahui dengan cepat apakah sebuah bilangan merupakan bilangan ganjil kelipatan 7 atau tidak.
