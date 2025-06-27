---
title: "Variabel pada JavaScript: Pengertian, dan Penggunaannya"
date: 2023-03-24
categories: 
  - "javascript"
---

JavaScript adalah bahasa pemrograman yang sangat populer di kalangan pengembang web. Salah satu fitur paling penting dari JavaScript adalah kemampuannya menggunakan variabel untuk menyimpan nilai dan data.

Variabel pada JavaScript dapat digunakan untuk mempermudah pemrograman, memanipulasi data, dan membuat program lebih fleksibel.

Artikel ini akan menjelaskan apa itu variabel pada JavaScript dan bagaimana cara menggunakannya.

## Pengertian Variable pada JavaScript

Variabel pada JavaScript adalah suatu nama yang digunakan untuk menyimpan nilai atau data. Variabel dapat diberikan nilai berupa angka, string, boolean, atau nilai lainnya.

Setelah variabel diberi nilai, nilai tersebut dapat digunakan di dalam program untuk melakukan operasi matematika, memanipulasi string, atau mengambil keputusan berdasarkan nilai boolean.

## Cara Mendeklarasikan Variable pada JavaScript

Untuk mendeklarasikan variabel pada JavaScript, kita dapat menggunakan var, let, atau const. Ketiganya memiliki perbedaan dalam cara mereka mengelola variabel.

### 1\. var

Var digunakan untuk mendeklarasikan variabel yang dapat diubah nilainya. Variabel yang dideklarasikan dengan var dapat diakses di seluruh program.

Contoh penggunaannya adalah sebagai berikut:

```
var angka = 10;
var nama = "John";
```

### 2\. let

let digunakan untuk mendeklarasikan variabel yang nilainya dapat diubah. Variabel yang dideklarasikan dengan let hanya dapat diakses di dalam blok kode tempat variabel tersebut dideklarasikan.

Contoh penggunaannya adalah sebagai berikut:

```
let angka = 10;
let nama = "John";

```

### 3\. const

const digunakan untuk mendeklarasikan variabel yang nilainya tetap atau tidak dapat diubah. Variabel yang dideklarasikan dengan const hanya dapat diakses di dalam blok kode tempat variabel tersebut dideklarasikan.

Contoh penggunaannya adalah sebagai berikut:

```
const angka = 10;
const nama = "John";

```

## Cara Menggunakan Variable pada JavaScript

Setelah variabel dideklarasikan, kita dapat menggunakannya dalam program. Berikut adalah beberapa cara untuk menggunakan variabel pada JavaScript:

### 1\. Menampilkan nilai variabel

Untuk menampilkan nilai variabel, kita dapat menggunakan fungsi console.log(). Fungsi ini akan menampilkan nilai variabel pada konsol web browser.

```
var angka = 10;
console.log(angka); // Output: 10

```

### 2\. Menggunakan variabel dalam operasi matematika

Variabel dapat digunakan dalam operasi matematika. Contohnya:

```
var angka1 = 10;
var angka2 = 5;
var hasil = angka1 + angka2;
console.log(hasil); // Output: 15

```

### 3\. Menggunakan variabel dalam manipulasi string

Variabel juga dapat digunakan untuk memanipulasi string. Contohnya:

```
var namaDepan = "John";
var namaBelakang = "Doe";
var namaLengkap = namaDepan + " " + namaBelakang;
console.log(namaLengkap); // Output: John Doe

```

## Kesimpulan

Variabel pada JavaScript adalah nama yang digunakan untuk menyimpan nilai atau data. Variabel pada JavaScript dapat dideklarasikan dengan kata kunci var, let, atau const, tergantung pada jenis variabel yang ingin dibuat.

Variabel yang dideklarasikan dengan var dapat diubah nilainya dan dapat diakses di seluruh program,

sedangkan variabel yang dideklarasikan dengan let atau const nilainya dapat diubah atau tidak tergantung pada kata kunci yang digunakan dan hanya dapat diakses di dalam blok kode tempat variabel tersebut dideklarasikan.

Variabel pada JavaScript dapat digunakan dalam berbagai operasi, seperti operasi matematika, manipulasi string, atau pengambilan keputusan berdasarkan nilai boolean.

Untuk menampilkan nilai variabel pada konsol web browser, kita dapat menggunakan fungsi console.log().

Dengan pemahaman yang baik tentang variabel pada JavaScript, Anda dapat membuat program yang lebih fleksibel dan mudah untuk dipelajari.

Oleh karena itu, jangan ragu untuk mempelajari variabel pada JavaScript dan menggunakannya dalam pengembangan web Anda.

**Baca Juga**: [Mengenal Tipe Data JavaScript dan Penggunaannya](https://ajiekusumadhany.com/tipe-data-javascript-dan-penggunaannya/)
