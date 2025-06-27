---
title: "Apa Itu Interpolation Search Dan Bagaimana Dibandingkan Dengan Binary Search?"
date: 2025-08-18
categories: 
  - "pemrograman"
tags: 
  - "pemrograman"
---

Pernahkah kamu mencari buku di rak perpustakaan yang berantakan? Atau mungkin mencari kontak seseorang di daftar nama yang sangat panjang? Pasti frustrasi, kan? Nah, dalam dunia pemrograman, kita juga sering dihadapkan dengan masalah yang sama: mencari data dalam kumpulan data yang besar. Ada banyak cara untuk melakukan pencarian, dan salah satu metode yang menarik adalah **Interpolation Search**.

Artikel ini akan membahas **apa itu Interpolation Search** dan bagaimana ia dibandingkan dengan algoritma pencarian yang lebih umum, yaitu Binary Search. Kita akan menyelami cara kerjanya, kelebihan dan kekurangannya, serta kapan sebaiknya menggunakan Interpolation Search dibandingkan dengan Binary Search. Siap? Mari kita mulai!

## Apa Itu Interpolation Search?

Interpolation Search adalah algoritma pencarian untuk mencari posisi suatu nilai tertentu dalam array yang sudah diurutkan. Algoritma ini bekerja dengan cara menebak posisi nilai yang dicari berdasarkan nilai terendah dan tertinggi dalam array, serta nilai yang dicari itu sendiri. Idenya mirip dengan cara kita mencari kata dalam kamus: kita tidak mulai dari tengah (seperti Binary Search), tetapi memperkirakan posisinya berdasarkan huruf pertama kata tersebut.

Interpolation Search mengasumsikan bahwa data dalam array terdistribusi secara seragam. Artinya, nilai-nilai dalam array tersebar merata. Asumsi ini penting karena akurasi tebakan posisi sangat bergantung pada distribusi data.

## Bagaimana Cara Kerja Interpolation Search?

Interpolation Search bekerja dengan menggunakan rumus untuk memperkirakan posisi nilai yang dicari. Rumusnya adalah sebagai berikut:

```
pos = low + ((key - arr[low]) * (high - low)) / (arr[high] - arr[low])
```

Di mana:

- `pos` adalah perkiraan posisi nilai yang dicari (key).
- `low` adalah indeks batas bawah array.
- `high` adalah indeks batas atas array.
- `key` adalah nilai yang ingin dicari.
- `arr` adalah array yang diurutkan.

Setelah menghitung `pos`, algoritma memeriksa apakah `arr[pos]` sama dengan `key`. Jika sama, maka pencarian berhasil dan `pos` dikembalikan. Jika `arr[pos]` lebih kecil dari `key`, maka pencarian dilanjutkan di bagian kanan array (dari `pos + 1` hingga `high`). Jika `arr[pos]` lebih besar dari `key`, maka pencarian dilanjutkan di bagian kiri array (dari `low` hingga `pos - 1`). Proses ini diulang hingga nilai ditemukan atau batas pencarian menyempit dan nilai tidak ditemukan.

## Interpolation Search vs. Binary Search: Apa Bedanya?

Binary Search dan Interpolation Search sama-sama algoritma pencarian yang efisien untuk array yang sudah diurutkan. Namun, ada perbedaan mendasar dalam cara mereka bekerja:

- **Binary Search:** Selalu membagi array menjadi dua bagian yang sama besar dan membandingkan nilai yang dicari dengan elemen tengah.
- **Interpolation Search:** Menebak posisi nilai yang dicari berdasarkan distribusi data dalam array.

Perbedaan ini menghasilkan perbedaan dalam kinerja:

- **Kasus Terbaik:** Interpolation Search bisa lebih cepat daripada Binary Search jika data terdistribusi secara seragam dan nilai yang dicari berada di dekat posisi yang diperkirakan.
- **Kasus Terburuk:** Jika data tidak terdistribusi secara seragam (misalnya, banyak nilai yang berdekatan), Interpolation Search bisa menjadi sangat lambat, bahkan lebih lambat dari Binary Search.
- **Kompleksitas Waktu:**
    - Binary Search: O(log n) dalam semua kasus.
    - Interpolation Search: O(log log n) dalam kasus terbaik (data terdistribusi seragam), O(n) dalam kasus terburuk (data tidak terdistribusi seragam).

## Kapan Menggunakan Interpolation Search?

Interpolation Search cocok digunakan ketika:

- Array sudah diurutkan.
- Data dalam array terdistribusi secara seragam atau mendekati seragam.
- Ukuran array cukup besar.

Interpolation Search kurang cocok digunakan ketika:

- Data dalam array tidak terdistribusi secara seragam.
- Ukuran array kecil.

## Contoh Kode Interpolation Search (Python)

Berikut adalah contoh implementasi Interpolation Search dalam bahasa Python:

```python
def interpolation_search(arr, low, high, key):
  """Mencari key dalam array arr menggunakan Interpolation Search."""

  while low <= high and key >= arr[low] and key <= arr[high]:
    # Perkirakan posisi
    pos = low + ((key - arr[low]) * (high - low)) // (arr[high] - arr[low])

    # Jika ditemukan
    if arr[pos] == key:
      return pos

    # Jika key lebih besar, cari di bagian kanan
    if arr[pos] < key:
      low = pos + 1

    # Jika key lebih kecil, cari di bagian kiri
    else:
      high = pos - 1

  return -1  # Tidak ditemukan

# Contoh penggunaan
arr = [10, 12, 13, 16, 18, 19, 20, 21, 22, 23, 24, 33, 35, 42, 47]
key = 22
index = interpolation_search(arr, 0, len(arr) - 1, key)

if index != -1:
  print("Elemen ditemukan pada index", index)
else:
  print("Elemen tidak ditemukan")
```

## Kelebihan dan Kekurangan Interpolation Search

**Kelebihan:**

- Potensi lebih cepat daripada Binary Search dalam kasus terbaik (data terdistribusi seragam).
- Lebih intuitif daripada Binary Search karena meniru cara manusia mencari informasi.

**Kekurangan:**

- Kinerja sangat buruk jika data tidak terdistribusi seragam.
- Lebih kompleks untuk diimplementasikan daripada Binary Search.
- Membutuhkan lebih banyak memori karena perlu menghitung perkiraan posisi.

## Kesimpulan

Interpolation Search adalah algoritma pencarian yang menarik dan berpotensi lebih cepat daripada Binary Search dalam kondisi tertentu. Namun, penting untuk memahami asumsi dan keterbatasannya sebelum menggunakannya. Jika data terdistribusi secara seragam, Interpolation Search bisa menjadi pilihan yang baik. Namun, jika tidak, Binary Search mungkin menjadi pilihan yang lebih aman dan stabil. Coba eksperimen dengan berbagai dataset untuk melihat mana yang bekerja lebih baik untuk kasus penggunaanmu. Apakah kamu punya pengalaman menggunakan Interpolation Search? Bagikan pengalamanmu di kolom komentar!

## FAQ

**1\. Kapan sebaiknya menggunakan Interpolation Search daripada Binary Search?**

Gunakan Interpolation Search ketika array sudah diurutkan dan data terdistribusi secara seragam. Jika data tidak terdistribusi seragam, Binary Search lebih disarankan.

**2\. Apakah Interpolation Search selalu lebih cepat daripada Binary Search?**

Tidak. Interpolation Search hanya lebih cepat dalam kasus terbaik, yaitu ketika data terdistribusi seragam. Dalam kasus terburuk, Interpolation Search bisa jauh lebih lambat.

**3\. Bagaimana cara mengatasi masalah distribusi data yang tidak seragam pada Interpolation Search?**

Salah satu cara adalah dengan menggunakan teknik pre-processing untuk mengubah distribusi data menjadi lebih seragam. Namun, ini bisa menambah kompleksitas dan overhead pada algoritma. Pilihan lainnya adalah tetap menggunakan Binary Search yang lebih stabil.
