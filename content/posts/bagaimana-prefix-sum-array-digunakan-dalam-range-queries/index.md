---
title: "Bagaimana Prefix Sum Array Digunakan Dalam Range Queries?"
date: 2025-11-10
categories: 
  - "pemrograman"
tags: 
  - "pemrograman"
---

Pernahkah kamu merasa kesulitan mencari total penjualan produkmu dalam periode waktu tertentu? Atau mungkin menghitung jumlah pengunjung website dalam rentang tanggal tertentu? Jika iya, kamu tidak sendirian! Banyak dari kita bergelut dengan masalah serupa.

Kabar baiknya, ada solusi elegan dan efisien untuk masalah ini: **Prefix Sum Array**. Teknik ini, seringkali tersembunyi di balik layar, adalah pahlawan tanpa tanda jasa dalam dunia pemrograman.

Artikel ini akan membongkar rahasia **bagaimana Prefix Sum Array digunakan dalam Range Queries**. Kita akan menjelajahi konsepnya, memahami implementasinya, dan melihat contoh-contoh praktis yang akan membuatmu kagum. Siap untuk menyelam lebih dalam? Yuk, kita mulai!

## Apa Itu Prefix Sum Array?

Sederhananya, Prefix Sum Array adalah array baru yang menyimpan jumlah kumulatif elemen dari array asli. Setiap elemen di Prefix Sum Array menunjukkan jumlah semua elemen dari awal array asli hingga indeks tersebut.

Bingung? Mari kita lihat contoh. Anggap saja kita punya array: `[1, 2, 3, 4, 5]`.

Maka, Prefix Sum Array-nya akan menjadi: `[1, 3, 6, 10, 15]`.

Perhatikan:

- `PrefixSum[0] = Array[0] = 1`
- `PrefixSum[1] = Array[0] + Array[1] = 1 + 2 = 3`
- `PrefixSum[2] = Array[0] + Array[1] + Array[2] = 1 + 2 + 3 = 6`
- Dan seterusnya...

## Mengapa Prefix Sum Array Penting?

Prefix Sum Array menjadi sangat berguna ketika kita sering melakukan _range queries_. Range query adalah pertanyaan yang meminta kita menghitung jumlah elemen dalam rentang indeks tertentu dalam array.

Tanpa Prefix Sum Array, untuk setiap range query, kita harus menjumlahkan semua elemen dalam rentang tersebut. Ini bisa sangat lambat, terutama jika arraynya besar dan kita memiliki banyak query.

Dengan Prefix Sum Array, kita dapat menjawab range query hanya dalam waktu O(1) (konstan)! Ini jauh lebih cepat daripada O(n) (linear) yang dibutuhkan tanpa Prefix Sum Array.

## Bagaimana Prefix Sum Array Digunakan dalam Range Queries?

Inilah inti dari artikel ini: **bagaimana Prefix Sum Array digunakan dalam Range Queries**.

Misalkan kita ingin mencari jumlah elemen dari indeks `i` hingga indeks `j` (inklusif) dalam array asli. Dengan Prefix Sum Array, kita dapat menghitungnya dengan rumus sederhana:

`Sum(i, j) = PrefixSum[j] - PrefixSum[i-1]`

**Penting:** Perhatikan bahwa rumus ini hanya berlaku jika `i > 0`. Jika `i = 0`, maka `Sum(0, j) = PrefixSum[j]`.

**Contoh:**

Kembali ke array kita: `Array = [1, 2, 3, 4, 5]` dan `PrefixSum = [1, 3, 6, 10, 15]`.

Katakanlah kita ingin mencari jumlah elemen dari indeks 2 hingga 4 (yaitu, 3 + 4 + 5).

Menggunakan rumus di atas:

`Sum(2, 4) = PrefixSum[4] - PrefixSum[1] = 15 - 3 = 12`

Benar sekali! 3 + 4 + 5 = 12.

## Implementasi Prefix Sum Array dalam Kode

Mari kita lihat bagaimana cara mengimplementasikan Prefix Sum Array dalam beberapa bahasa pemrograman populer.

### Python

```python
def prefix_sum(arr):
  """Menghitung Prefix Sum Array dari array input."""
  n = len(arr)
  prefix_sum_arr = [0] * n
  prefix_sum_arr[0] = arr[0]
  for i in range(1, n):
    prefix_sum_arr[i] = prefix_sum_arr[i-1] + arr[i]
  return prefix_sum_arr

def range_sum(prefix_sum_arr, i, j):
  """Menghitung jumlah elemen dalam rentang i hingga j."""
  if i == 0:
    return prefix_sum_arr[j]
  else:
    return prefix_sum_arr[j] - prefix_sum_arr[i-1]

# Contoh penggunaan
arr = [1, 2, 3, 4, 5]
prefix_sum_arr = prefix_sum(arr)
print(f"Prefix Sum Array: prefix_sum_arr")

# Menghitung jumlah dari indeks 2 hingga 4
sum_2_4 = range_sum(prefix_sum_arr, 2, 4)
print(f"Jumlah dari indeks 2 hingga 4: sum_2_4")
```

### Java

```java
public class PrefixSum 

  public static int[] prefixSum(int[] arr) 
    int n = arr.length;
    int[] prefixSumArr = new int[n];
    prefixSumArr[0] = arr[0];
    for (int i = 1; i < n; i++) 
      prefixSumArr[i] = prefixSumArr[i-1] + arr[i];
    
    return prefixSumArr;
  

  public static int rangeSum(int[] prefixSumArr, int i, int j) 
    if (i == 0) 
      return prefixSumArr[j];
     else 
      return prefixSumArr[j] - prefixSumArr[i-1];
    
  

  public static void main(String[] args) 
    int[] arr = 1, 2, 3, 4, 5;
    int[] prefixSumArr = prefixSum(arr);
    System.out.println("Prefix Sum Array: " + java.util.Arrays.toString(prefixSumArr));

    // Menghitung jumlah dari indeks 2 hingga 4
    int sum_2_4 = rangeSum(prefixSumArr, 2, 4);
    System.out.println("Jumlah dari indeks 2 hingga 4: " + sum_2_4);
  
```

### C++

```c++
#include <iostream>
#include <vector>

using namespace std;

vector<int> prefixSum(vector<int> arr) 
  int n = arr.size();
  vector<int> prefixSumArr(n);
  prefixSumArr[0] = arr[0];
  for (int i = 1; i < n; i++) 
    prefixSumArr[i] = prefixSumArr[i-1] + arr[i];
  
  return prefixSumArr;

int rangeSum(vector<int> prefixSumArr, int i, int j) 
  if (i == 0) 
    return prefixSumArr[j];
   else 
    return prefixSumArr[j] - prefixSumArr[i-1];
  

int main() 
  vector<int> arr = 1, 2, 3, 4, 5;
  vector<int> prefixSumArr = prefixSum(arr);
  cout << "Prefix Sum Array: ";
  for (int x : prefixSumArr) 
    cout << x << " ";
  
  cout << endl;

  // Menghitung jumlah dari indeks 2 hingga 4
  int sum_2_4 = rangeSum(prefixSumArr, 2, 4);
  cout << "Jumlah dari indeks 2 hingga 4: " << sum_2_4 << endl;

  return 0;
```

Kode di atas menunjukkan implementasi dasar dari Prefix Sum Array dan cara menggunakannya untuk menghitung jumlah dalam rentang tertentu. Kamu dapat menyesuaikan kode ini sesuai dengan kebutuhan spesifik proyekmu.

## Contoh Kasus Penggunaan Prefix Sum Array

Prefix Sum Array memiliki banyak aplikasi praktis di berbagai bidang. Berikut beberapa contoh:

- **Analisis Data:** Menghitung total penjualan, pendapatan, atau metrik lainnya dalam rentang waktu tertentu.
- **Pemrosesan Gambar:** Menghitung jumlah piksel dalam area tertentu dari gambar.
- **Game Development:** Menghitung total damage yang diterima oleh karakter dalam rentang waktu tertentu.
- **Algoritma:** Digunakan sebagai building block dalam algoritma yang lebih kompleks, seperti Dynamic Programming.

## Optimasi dan Variasi

Meskipun Prefix Sum Array sangat efisien, ada beberapa cara untuk mengoptimalkannya atau menggunakan variasi yang berbeda tergantung pada kebutuhanmu:

- **Immutable Array:** Jika array asli tidak berubah, kita hanya perlu menghitung Prefix Sum Array sekali dan menggunakannya berulang kali.
- **2D Prefix Sum Array:** Untuk array dua dimensi (misalnya, matriks), kita dapat membuat 2D Prefix Sum Array untuk menghitung jumlah elemen dalam persegi panjang tertentu.
- **Binary Indexed Tree (Fenwick Tree):** Struktur data yang lebih canggih yang memungkinkan kita untuk melakukan update pada array asli dan menghitung range sum dengan efisien.

## Kesimpulan

Prefix Sum Array adalah teknik sederhana namun sangat ampuh yang dapat mempercepat proses perhitungan range queries secara signifikan. Dengan memahami konsepnya dan mengimplementasikannya dengan benar, kamu dapat meningkatkan efisiensi kode dan menyelesaikan masalah dengan lebih cepat.

Sekarang, giliranmu untuk mencoba dan bereksperimen dengan Prefix Sum Array. Cobalah menerapkannya dalam proyekmu sendiri dan lihat bagaimana ia dapat membantu memecahkan masalah yang kamu hadapi. Jangan ragu untuk berbagi pengalamanmu di bagian komentar!

## FAQ

**1\. Apa kompleksitas waktu untuk membuat Prefix Sum Array?**

Kompleksitas waktu untuk membuat Prefix Sum Array adalah O(n), di mana n adalah panjang array asli. Kita perlu melakukan iterasi sekali untuk menghitung jumlah kumulatif.

**2\. Apa kompleksitas waktu untuk menghitung range sum menggunakan Prefix Sum Array?**

Kompleksitas waktu untuk menghitung range sum menggunakan Prefix Sum Array adalah O(1). Kita hanya perlu melakukan dua operasi pengurangan.

**3\. Kapan saya harus menggunakan Prefix Sum Array?**

Kamu harus menggunakan Prefix Sum Array ketika kamu sering melakukan range queries pada array yang sama. Jika array asli sering berubah, mungkin ada struktur data lain yang lebih cocok, seperti Binary Indexed Tree.
