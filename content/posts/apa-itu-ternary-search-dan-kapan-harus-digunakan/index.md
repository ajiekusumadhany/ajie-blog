---
title: "Apa Itu Ternary Search Dan Kapan Harus Digunakan?"
date: 2025-07-03
categories: 
  - "pemrograman"
tags: 
  - "pemrograman"
---

Pernah nggak sih, kamu kebingungan mencari satu barang spesifik di antara tumpukan barang yang nggak karuan? Atau mungkin, kamu lagi nyari harga termurah buat tiket pesawat, tapi pilihannya bejibun banget? Nah, di dunia pemrograman, masalah pencarian kayak gini sering banget muncul. Tapi tenang, ada satu algoritma keren yang bisa jadi andalanmu: **Ternary Search**.

Artikel ini akan membongkar tuntas **apa itu Ternary Search dan kapan harus digunakan**. Kita akan kupas tuntas kelebihan, kekurangan, serta contoh penggunaannya biar kamu makin jago dalam memecahkan masalah pencarian. Yuk, simak!

## Apa Itu Ternary Search?

Ternary Search adalah algoritma pencarian yang digunakan untuk menemukan nilai maksimum atau minimum dari fungsi unimodal. Apa itu unimodal? Sederhananya, fungsi unimodal adalah fungsi yang awalnya naik (atau turun) hingga mencapai titik maksimum (atau minimum), lalu kemudian turun (atau naik) setelah titik tersebut.

Bayangkan kamu sedang mencari puncak gunung. Ternary Search akan membantumu menemukan puncak itu tanpa harus mendaki seluruh gunungnya. Caranya? Dengan membagi area pencarian menjadi tiga bagian dan membandingkan nilai di dua titik pemisah.

## Bagaimana Cara Kerja Ternary Search?

Proses Ternary Search cukup sederhana, tapi efektif:

1. **Mulai dengan interval pencarian.** Ini adalah rentang nilai tempat kita mencari nilai maksimum atau minimum.
2. **Bagi interval menjadi tiga bagian yang sama.** Kita mendapatkan dua titik tengah: `mid1` dan `mid2`.
3. **Evaluasi fungsi di `mid1` dan `mid2`.** Bandingkan nilai `f(mid1)` dan `f(mid2)`.
4. **Perbarui interval pencarian berdasarkan hasil perbandingan:**
    
    - Jika `f(mid1) < f(mid2)`, berarti nilai maksimum berada di sebelah kanan `mid1`. Kita perbarui interval menjadi `[mid1, kanan]`.
    - Jika `f(mid1) > f(mid2)`, berarti nilai maksimum berada di sebelah kiri `mid2`. Kita perbarui interval menjadi `[kiri, mid2]`.
    - Jika `f(mid1) == f(mid2)`, kita bisa mempersempit interval ke salah satu sisi, misalnya `[mid1, kanan]`.
5. **Ulangi langkah 2-4** sampai interval pencarian cukup kecil (misalnya, selisih antara `kiri` dan `kanan` kurang dari ambang batas tertentu).

## Kapan Harus Menggunakan Ternary Search?

Ternary Search sangat berguna dalam beberapa situasi tertentu:

- **Mencari nilai maksimum atau minimum fungsi unimodal:** Ini adalah penggunaan utamanya. Contohnya, mencari nilai maksimum dari fungsi kuadrat dalam rentang tertentu.
- **Optimasi parameter:** Dalam machine learning, kita sering mencari parameter optimal untuk suatu model. Jika fungsi loss (kerugian) bersifat unimodal terhadap parameter tersebut, Ternary Search bisa menjadi pilihan yang baik.
- **Pencarian dalam ruang kontinu:** Ternary Search bekerja dengan baik pada ruang pencarian yang kontinu, di mana nilai-nilai dapat berubah secara bertahap.

## Kelebihan dan Kekurangan Ternary Search

Seperti algoritma lainnya, Ternary Search punya kelebihan dan kekurangan yang perlu kamu pertimbangkan:

**Kelebihan:**

- **Efektif untuk fungsi unimodal:** Jika fungsi yang dicari memang unimodal, Ternary Search bisa menemukan nilai optimal dengan cepat.
- **Implementasi relatif sederhana:** Algoritmanya cukup mudah dipahami dan diimplementasikan.
- **Tidak memerlukan turunan:** Berbeda dengan metode optimasi lainnya, Ternary Search tidak memerlukan perhitungan turunan fungsi.

**Kekurangan:**

- **Hanya bekerja untuk fungsi unimodal:** Jika fungsi tidak unimodal, Ternary Search mungkin tidak menemukan nilai optimal yang sebenarnya.
- **Kurang efisien dibandingkan Binary Search pada array yang terurut:** Jika kamu hanya perlu mencari nilai dalam array yang sudah terurut, Binary Search biasanya lebih cepat.
- **Membutuhkan lebih banyak evaluasi fungsi:** Dibandingkan Binary Search, Ternary Search membutuhkan lebih banyak evaluasi fungsi dalam setiap iterasi.

## Contoh Penggunaan Ternary Search

Mari kita lihat beberapa contoh penggunaan Ternary Search dalam kode Python:

**Contoh 1: Mencari maksimum fungsi kuadrat**

```python
def f(x):
  return -x**2 + 4*x + 5

def ternary_search(l, r, error):
  while r - l > error:
    m1 = l + (r - l) / 3
    m2 = r - (r - l) / 3
    if f(m1) < f(m2):
      l = m1
    else:
      r = m2
  return (l + r) / 2

l = 0
r = 4
error = 0.00001
max_x = ternary_search(l, r, error)
print("Nilai x untuk maksimum:", max_x)
print("Nilai maksimum:", f(max_x))
```

Dalam contoh ini, kita mencari nilai x yang memaksimalkan fungsi kuadrat `f(x) = -x^2 + 4x + 5` dalam interval \[0, 4\].

**Contoh 2: Optimasi parameter dalam Machine Learning (simulasi)**

```python
import random

def loss_function(parameter):
  # Simulasi fungsi loss yang unimodal
  return (parameter - 2)**2 + random.uniform(-0.1, 0.1)

def ternary_search_ml(l, r, error):
  while r - l > error:
    m1 = l + (r - l) / 3
    m2 = r - (r - l) / 3
    if loss_function(m1) < loss_function(m2):
      r = m2
    else:
      l = m1
  return (l + r) / 2

l = 0
r = 4
error = 0.001
optimal_parameter = ternary_search_ml(l, r, error)
print("Parameter optimal:", optimal_parameter)
print("Loss minimal:", loss_function(optimal_parameter))
```

Contoh ini mensimulasikan pencarian parameter optimal untuk suatu model machine learning. Perhatikan bahwa fungsi `loss_function` dibuat unimodal (dengan sedikit noise).

## Perbandingan Ternary Search dengan Binary Search

Meskipun keduanya adalah algoritma pencarian, Ternary Search dan Binary Search memiliki perbedaan mendasar:

| Fitur | Ternary Search | Binary Search |
| --- | --- | --- |
| Jenis Data | Fungsi unimodal | Array yang terurut |
| Tujuan | Mencari nilai maksimum atau minimum | Mencari nilai tertentu |
| Cara Kerja | Membagi interval menjadi tiga bagian | Membagi interval menjadi dua bagian |
| Kompleksitas Waktu | O(log₃ n) | O(log₂ n) |
| Kondisi | Fungsi harus unimodal | Array harus terurut |

Secara umum, Binary Search lebih efisien daripada Ternary Search jika data sudah terurut dan tujuan pencarian adalah mencari nilai tertentu. Namun, jika kamu berurusan dengan fungsi unimodal, Ternary Search adalah pilihan yang lebih tepat.

## Tips dan Trik Penggunaan Ternary Search

- **Pastikan fungsi unimodal:** Sebelum menggunakan Ternary Search, pastikan bahwa fungsi yang ingin kamu optimalkan benar-benar unimodal. Jika tidak, hasilnya bisa jadi tidak akurat.
- **Pilih interval yang tepat:** Interval pencarian awal harus mencakup nilai optimal yang ingin kamu temukan.
- **Tentukan ambang batas yang sesuai:** Ambang batas untuk menghentikan iterasi (misalnya, `error` dalam contoh kode) harus dipilih dengan hati-hati. Terlalu kecil, iterasi akan memakan waktu lama. Terlalu besar, hasilnya mungkin kurang akurat.
- **Pertimbangkan penggunaan metode optimasi lain:** Jika fungsi tidak unimodal atau kamu memerlukan akurasi yang sangat tinggi, pertimbangkan untuk menggunakan metode optimasi yang lebih canggih, seperti Gradient Descent atau algoritma genetika.

## Kesimpulan

**Ternary Search** adalah alat yang ampuh untuk mencari nilai maksimum atau minimum dari fungsi unimodal. Meskipun memiliki keterbatasan, algoritma ini bisa sangat berguna dalam berbagai aplikasi, mulai dari optimasi parameter hingga pencarian dalam ruang kontinu. Dengan memahami cara kerja, kelebihan, dan kekurangan Ternary Search, kamu bisa memanfaatkannya secara efektif untuk memecahkan masalah pencarian yang kompleks.

Gimana? Sudah lebih paham kan tentang Ternary Search? Jangan ragu untuk mencoba mengimplementasikannya sendiri dan berbagi pengalamanmu di kolom komentar!

## FAQ (Frequently Asked Questions)

**1\. Apa yang terjadi jika fungsi tidak unimodal saat menggunakan Ternary Search?**

Jika fungsi tidak unimodal, Ternary Search mungkin akan terjebak dalam lokal optimum dan tidak menemukan nilai optimal yang sebenarnya. Dalam kasus seperti ini, sebaiknya gunakan metode optimasi yang lebih canggih yang dapat menangani fungsi non-unimodal.

**2\. Apakah Ternary Search bisa digunakan untuk mencari nilai minimum juga?**

Tentu saja! Ternary Search dapat digunakan untuk mencari nilai minimum dengan sedikit modifikasi. Alih-alih mencari nilai yang lebih besar di `mid1` dan `mid2`, kita mencari nilai yang lebih kecil.

**3\. Bagaimana cara menentukan ambang batas yang tepat untuk menghentikan iterasi?**

Ambang batas yang tepat tergantung pada tingkat akurasi yang kamu butuhkan dan karakteristik fungsi yang kamu optimalkan. Cobalah beberapa nilai yang berbeda dan lihat bagaimana hasilnya. Semakin kecil ambang batas, semakin akurat hasilnya, tetapi semakin lama waktu komputasinya.
