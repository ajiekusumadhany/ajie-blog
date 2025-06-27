---
title: "Apa Itu Fenwick Tree Dan Bagaimana Cara Menggunakannya?"
date: 2025-12-14
categories: 
  - "pemrograman"
tags: 
  - "pemrograman"
---

Pernahkah Anda merasa frustrasi saat harus menghitung jumlah elemen dalam rentang tertentu berulang kali? Atau mungkin Anda perlu memperbarui nilai elemen dalam array secara sering dan kemudian menghitung jumlahnya? Jika ya, mungkin Anda belum kenal dengan senjata rahasia para programmer: **Fenwick Tree**.

Artikel ini akan membahas tuntas **apa itu Fenwick Tree** dan bagaimana cara menggunakannya untuk menyelesaikan masalah-masalah tersebut secara efisien. Kita akan menyelami konsepnya, implementasinya, dan contoh penggunaannya. Siap untuk meningkatkan kemampuan pemrograman Anda? Mari kita mulai!

## Apa Itu Fenwick Tree?

Fenwick Tree, juga dikenal sebagai Binary Indexed Tree (BIT), adalah struktur data yang memungkinkan kita untuk melakukan dua operasi penting secara efisien:

- **Query:** Menghitung jumlah elemen dalam rentang tertentu (prefix sum).
- **Update:** Memperbarui nilai elemen dalam array.

Kelebihan Fenwick Tree adalah kompleksitas waktunya yang logaritmik (O(log n)) untuk kedua operasi tersebut, jauh lebih cepat dibandingkan dengan pendekatan naive yang membutuhkan O(n) untuk menghitung prefix sum.

## Mengapa Memilih Fenwick Tree?

Mungkin Anda bertanya, mengapa repot-repot mempelajari Fenwick Tree jika kita bisa menggunakan array biasa? Jawabannya terletak pada efisiensi. Bayangkan jika Anda memiliki array dengan jutaan elemen dan perlu melakukan ribuan operasi query dan update. Pendekatan naive akan sangat lambat. Fenwick Tree hadir sebagai solusi untuk mengatasi masalah ini.

Berikut adalah beberapa alasan mengapa Anda harus mempertimbangkan penggunaan Fenwick Tree:

- **Efisiensi:** Kompleksitas waktu logaritmik untuk query dan update.
- **Implementasi Relatif Sederhana:** Dibandingkan dengan struktur data lain seperti segment tree, implementasi Fenwick Tree relatif lebih sederhana.
- **Memori yang Efisien:** Fenwick Tree hanya membutuhkan ruang tambahan seukuran array input.

## Konsep Dasar Fenwick Tree

Fenwick Tree memanfaatkan representasi biner dari indeks untuk menyimpan informasi prefix sum secara efisien. Setiap node dalam Fenwick Tree bertanggung jawab untuk menyimpan jumlah elemen dalam rentang tertentu yang ditentukan oleh representasi biner dari indeksnya.

Untuk memahami konsep ini lebih baik, mari kita lihat contoh sederhana. Misalkan kita memiliki array `arr = [2, 1, 1, 3, 2, 3, 4, 5, 6, 7, 8, 9]`. Fenwick Tree yang sesuai akan menyimpan informasi prefix sum dalam struktur yang berbeda dari array asli.

### Representasi Biner dan LSB (Least Significant Bit)

Kunci untuk memahami Fenwick Tree adalah memahami bagaimana representasi biner dari indeks digunakan. Kita perlu mencari tahu LSB (Least Significant Bit) dari setiap indeks. LSB adalah bit paling kanan yang bernilai 1 dalam representasi biner sebuah angka.

Contoh:

- Indeks 6 (biner: 110): LSB adalah 2 (biner: 010)
- Indeks 12 (biner: 1100): LSB adalah 4 (biner: 0100)

Kita dapat menghitung LSB menggunakan operasi bitwise: `LSB = i & -i` (di mana `i` adalah indeks).

### Bagaimana Fenwick Tree Menyimpan Informasi?

Setiap node `FenwickTree[i]` menyimpan jumlah elemen dari `arr[i - LSB(i) + 1]` hingga `arr[i]`.

Contoh:

- `FenwickTree[6]` menyimpan jumlah `arr[5] + arr[6]` (karena LSB(6) = 2, maka rentangnya adalah dari 6-2+1 = 5 hingga 6)
- `FenwickTree[8]` menyimpan jumlah `arr[1] + arr[2] + arr[3] + arr[4] + arr[5] + arr[6] + arr[7] + arr[8]` (karena LSB(8) = 8, maka rentangnya adalah dari 8-8+1 = 1 hingga 8)

## Implementasi Fenwick Tree

Sekarang, mari kita lihat bagaimana cara mengimplementasikan Fenwick Tree. Kita akan menggunakan Python sebagai contoh.

### Inisialisasi Fenwick Tree

```python
def build_fenwick_tree(arr):
  """
  Membangun Fenwick Tree dari array input.

  Args:
    arr: Array input.

  Returns:
    Fenwick Tree yang dibangun dari array input.
  """
  n = len(arr)
  fenwick_tree = [0] * (n + 1)  # Index 0 tidak digunakan
  for i in range(1, n + 1):
    fenwick_tree[i] = arr[i - 1]
    j = i + (i & -i)
    if j <= n:
      fenwick_tree[j] += fenwick_tree[i]
  return fenwick_tree
```

### Query (Menghitung Prefix Sum)

```python
def query(fenwick_tree, i):
  """
  Menghitung jumlah elemen dari arr[0] hingga arr[i-1].

  Args:
    fenwick_tree: Fenwick Tree.
    i: Indeks hingga mana jumlah elemen akan dihitung.

  Returns:
    Jumlah elemen dari arr[0] hingga arr[i-1].
  """
  sum = 0
  while i > 0:
    sum += fenwick_tree[i]
    i -= (i & -i)
  return sum
```

### Update (Memperbarui Nilai Elemen)

```python
def update(fenwick_tree, i, delta):
  """
  Memperbarui nilai elemen pada indeks i dengan delta.

  Args:
    fenwick_tree: Fenwick Tree.
    i: Indeks elemen yang akan diperbarui.
    delta: Nilai yang akan ditambahkan ke elemen.
  """
  n = len(fenwick_tree) - 1
  while i <= n:
    fenwick_tree[i] += delta
    i += (i & -i)
```

### Contoh Penggunaan

```python
arr = [2, 1, 1, 3, 2, 3, 4, 5, 6, 7, 8, 9]
fenwick_tree = build_fenwick_tree(arr)

# Menghitung jumlah elemen dari arr[0] hingga arr[5]
print(f"Jumlah elemen dari arr[0] hingga arr[5]: query(fenwick_tree, 6)")

# Memperbarui nilai arr[3] dengan menambahkan 5
update(fenwick_tree, 4, 5) # Indeks di Fenwick Tree dimulai dari 1

# Menghitung jumlah elemen dari arr[0] hingga arr[5] setelah update
print(f"Jumlah elemen dari arr[0] hingga arr[5] setelah update: query(fenwick_tree, 6)")
```

## Contoh Soal dan Solusi

Mari kita lihat contoh soal yang bisa diselesaikan dengan Fenwick Tree.

**Soal:**

Diberikan sebuah array `arr` dan serangkaian query. Setiap query adalah salah satu dari dua jenis:

1. `Query(l, r)`: Hitung jumlah elemen dari `arr[l]` hingga `arr[r]`.
2. `Update(i, val)`: Perbarui nilai `arr[i]` menjadi `val`.

**Solusi:**

Kita dapat menggunakan Fenwick Tree untuk menyelesaikan soal ini secara efisien.

1. Bangun Fenwick Tree dari array input.
2. Untuk setiap query `Query(l, r)`, hitung `query(fenwick_tree, r+1) - query(fenwick_tree, l)`.
3. Untuk setiap query `Update(i, val)`, hitung `delta = val - arr[i]`. Kemudian, perbarui Fenwick Tree dengan `update(fenwick_tree, i+1, delta)`. Terakhir, perbarui nilai `arr[i]` dengan `val`.

## Kapan Sebaiknya Menggunakan Fenwick Tree?

Fenwick Tree sangat berguna dalam situasi di mana Anda perlu melakukan operasi query dan update pada array secara berulang. Beberapa contoh kasus penggunaan meliputi:

- **Menghitung jumlah elemen dalam rentang tertentu secara dinamis:** Misalnya, menghitung jumlah penjualan produk dalam periode waktu tertentu dan memperbarui data penjualan secara real-time.
- **Menghitung inversi dalam array:** Inversi adalah pasangan elemen dalam array di mana elemen yang lebih kecil muncul setelah elemen yang lebih besar.
- **Kompresi data:** Fenwick Tree dapat digunakan untuk mengimplementasikan algoritma kompresi data tertentu.

## Kelebihan dan Kekurangan Fenwick Tree

**Kelebihan:**

- Implementasi relatif sederhana.
- Membutuhkan ruang memori yang efisien.
- Kompleksitas waktu logaritmik untuk query dan update.

**Kekurangan:**

- Hanya dapat digunakan untuk operasi yang bersifat asosiatif dan komutatif (seperti penjumlahan).
- Kurang fleksibel dibandingkan dengan struktur data lain seperti segment tree.

## Kesimpulan

**Apa itu Fenwick Tree?** Fenwick Tree adalah struktur data yang efisien untuk menghitung prefix sum dan melakukan update pada array. Dengan kompleksitas waktu logaritmik, Fenwick Tree adalah pilihan yang tepat untuk menyelesaikan masalah yang melibatkan operasi query dan update secara berulang.

Semoga artikel ini memberikan pemahaman yang jelas tentang Fenwick Tree dan bagaimana cara menggunakannya. Jangan ragu untuk bereksperimen dengan kode dan mencoba menyelesaikan soal-soal latihan untuk memperdalam pemahaman Anda. Selamat mencoba dan semoga sukses!

## FAQ

**1\. Apa perbedaan antara Fenwick Tree dan Segment Tree?**

Fenwick Tree dan Segment Tree adalah struktur data yang serupa yang digunakan untuk menyelesaikan masalah yang melibatkan query dan update pada array. Perbedaan utama adalah:

- **Implementasi:** Implementasi Fenwick Tree relatif lebih sederhana daripada Segment Tree.
- **Fleksibilitas:** Segment Tree lebih fleksibel dan dapat digunakan untuk berbagai jenis operasi, sementara Fenwick Tree terbatas pada operasi yang bersifat asosiatif dan komutatif.
- **Kompleksitas Waktu:** Dalam banyak kasus, kompleksitas waktu untuk query dan update pada Fenwick Tree dan Segment Tree adalah sama (O(log n)).

**2\. Kapan sebaiknya saya menggunakan Fenwick Tree daripada Segment Tree?**

Anda sebaiknya menggunakan Fenwick Tree jika:

- Anda membutuhkan implementasi yang sederhana dan cepat.
- Anda hanya perlu melakukan operasi yang bersifat asosiatif dan komutatif (seperti penjumlahan).
- Anda memiliki keterbatasan memori.

**3\. Apakah Fenwick Tree hanya bisa digunakan untuk penjumlahan?**

Tidak sepenuhnya. Fenwick Tree paling umum digunakan untuk penjumlahan karena operasi penjumlahan bersifat asosiatif dan komutatif. Namun, Fenwick Tree juga bisa digunakan untuk operasi lain yang memenuhi syarat tersebut, seperti perkalian (dengan modulo) atau operasi XOR. Kuncinya adalah memastikan bahwa operasi tersebut memenuhi sifat asosiatif dan komutatif agar Fenwick Tree dapat berfungsi dengan benar.
