---
title: "Apa Itu Disjoint Set Union Dan Bagaimana Meningkatkan Algoritma?"
date: 2025-11-12
categories: 
  - "pemrograman"
tags: 
  - "pemrograman"
---

Pernah nggak sih, lagi asik main game puzzle, terus kepikiran: "Gimana ya caranya komputer bisa tahu kalau dua bagian ini sebenarnya nyambung?" Nah, di dunia pemrograman, ada satu struktur data keren yang jago banget buat masalah kayak gini: **Disjoint Set Union**!

Bingung? Tenang aja! Artikel ini bakal ngebahas tuntas **apa itu Disjoint Set Union** (DSU), kenapa dia penting, dan yang paling seru, gimana caranya ningkatin algoritma DSU biar makin ngebut. Jadi, siap buat jadi master DSU? Yuk, mulai!

## Apa Itu Disjoint Set Union (DSU)?

Sederhananya, Disjoint Set Union (DSU), atau kadang disebut Union-Find, adalah struktur data yang digunakan untuk melacak sekumpulan elemen yang terbagi menjadi beberapa himpunan yang saling lepas (disjoint). Setiap himpunan memiliki perwakilan (representative) yang unik.

DSU punya dua operasi utama:

- **Find(x):** Mencari tahu himpunan mana yang dimiliki elemen `x`. Operasi ini mengembalikan perwakilan dari himpunan tersebut.
- **Union(x, y):** Menggabungkan himpunan yang berisi elemen `x` dan himpunan yang berisi elemen `y` menjadi satu himpunan.

Bayangin aja kayak gini: kita punya beberapa pulau yang terisolasi. Operasi `Find` itu kayak nyari tahu pulau mana yang lagi kita injak. Operasi `Union` itu kayak membangun jembatan yang menghubungkan dua pulau.

### Kenapa Disjoint Set Union Penting?

DSU itu penting karena dia bisa menyelesaikan banyak masalah dengan efisien. Beberapa contohnya:

- **Mencari komponen terhubung dalam graf:** DSU bisa digunakan untuk mencari tahu berapa banyak komponen terhubung (kelompok node yang saling terhubung) dalam sebuah graf.
- **Mendeteksi siklus dalam graf:** DSU bisa mendeteksi apakah sebuah graf memiliki siklus (lingkaran).
- **Clustering:** DSU bisa digunakan untuk mengelompokkan data berdasarkan kemiripan.
- **Kruskal's Algorithm (Minimum Spanning Tree):** Algoritma Kruskal, yang digunakan untuk mencari minimum spanning tree (pohon rentang minimum) dalam sebuah graf, sangat bergantung pada DSU.

Intinya, DSU itu alat yang ampuh buat masalah-masalah yang melibatkan pengelompokan dan konektivitas.

## Implementasi Dasar Disjoint Set Union

Implementasi dasar DSU biasanya menggunakan array `parent` untuk menyimpan informasi tentang "orang tua" dari setiap elemen. Awalnya, setiap elemen adalah "orang tua" dari dirinya sendiri, yang berarti setiap elemen membentuk himpunannya sendiri.

Berikut contoh implementasi sederhana dalam pseudocode:

```
function Initialize(n):
  for i = 1 to n:
    parent[i] = i

function Find(x):
  if parent[x] == x:
    return x
  return Find(parent[x])

function Union(x, y):
  xRoot = Find(x)
  yRoot = Find(y)
  if xRoot != yRoot:
    parent[xRoot] = yRoot
```

Penjelasan:

- `Initialize(n)`: Inisialisasi array `parent` dengan ukuran `n`. Setiap elemen `i` awalnya menjadi "orang tua" dari dirinya sendiri.
- `Find(x)`: Secara rekursif mencari "orang tua" dari `x` sampai menemukan elemen yang merupakan "orang tua" dari dirinya sendiri (root). Inilah perwakilan dari himpunan yang berisi `x`.
- `Union(x, y)`: Mencari perwakilan dari himpunan yang berisi `x` dan `y`. Jika perwakilan mereka berbeda, berarti mereka berada di himpunan yang berbeda. Kita kemudian menggabungkan kedua himpunan tersebut dengan menjadikan perwakilan salah satu himpunan sebagai "orang tua" dari perwakilan himpunan lainnya.

### Masalah dengan Implementasi Dasar

Implementasi dasar ini cukup sederhana, tapi punya satu masalah besar: kinerjanya bisa buruk dalam beberapa kasus. Bayangin kalau kita melakukan serangkaian operasi `Union` yang selalu menggabungkan himpunan ke satu arah. Ini bisa menghasilkan "pohon" yang sangat tinggi, sehingga operasi `Find` membutuhkan waktu O(n) dalam kasus terburuk, di mana `n` adalah jumlah elemen.

## Meningkatkan Algoritma Disjoint Set Union

Untungnya, ada dua teknik yang bisa kita gunakan untuk meningkatkan kinerja DSU secara signifikan:

1. **Path Compression:**
2. **Union by Rank:**

### Path Compression

Path compression adalah teknik untuk "meratakan" pohon DSU selama operasi `Find`. Saat kita mencari perwakilan dari sebuah elemen `x`, kita langsung menghubungkan `x` ke root yang ditemukan. Ini secara efektif memperpendek jalur ke root untuk semua elemen di sepanjang jalur pencarian.

Implementasi Path Compression (pseudocode):

```
function Find(x):
  if parent[x] == x:
    return x
  parent[x] = Find(parent[x])  // Path Compression
  return parent[x]
```

Perhatikan baris `parent[x] = Find(parent[x])`. Setelah kita menemukan root dari `x`, kita langsung mengupdate `parent[x]` untuk menunjuk langsung ke root. Ini membuat operasi `Find` berikutnya untuk `x` (dan semua elemen di sepanjang jalur pencarian) menjadi jauh lebih cepat.

### Union by Rank

Union by Rank adalah teknik untuk memilih "orang tua" yang lebih baik saat melakukan operasi `Union`. Ide dasarnya adalah melacak "rank" dari setiap himpunan. Rank ini kira-kira mewakili kedalaman pohon yang mewakili himpunan tersebut. Saat kita menggabungkan dua himpunan, kita selalu menjadikan himpunan dengan rank yang lebih kecil sebagai "anak" dari himpunan dengan rank yang lebih besar. Jika rank kedua himpunan sama, kita bisa menjadikan salah satu sebagai "orang tua" dan meningkatkan rank himpunan "orang tua" tersebut.

Implementasi Union by Rank (pseudocode):

```
function Initialize(n):
  for i = 1 to n:
    parent[i] = i
    rank[i] = 0  // Inisialisasi rank menjadi 0

function Union(x, y):
  xRoot = Find(x)
  yRoot = Find(y)
  if xRoot != yRoot:
    if rank[xRoot] < rank[yRoot]:
      parent[xRoot] = yRoot
    else if rank[xRoot] > rank[yRoot]:
      parent[yRoot] = xRoot
    else:
      parent[yRoot] = xRoot
      rank[xRoot] = rank[xRoot] + 1
```

Penjelasan:

- `Initialize(n)`: Kita menambahkan array `rank` untuk melacak rank dari setiap himpunan. Awalnya, semua rank diinisialisasi menjadi 0.
- `Union(x, y)`: Kita membandingkan rank dari himpunan yang berisi `x` dan `y`. Jika rank mereka berbeda, kita menjadikan himpunan dengan rank yang lebih kecil sebagai "anak" dari himpunan dengan rank yang lebih besar. Jika rank mereka sama, kita menjadikan salah satu sebagai "orang tua" dan meningkatkan rank himpunan "orang tua" tersebut.

### Kombinasi Path Compression dan Union by Rank

Kombinasi Path Compression dan Union by Rank memberikan peningkatan kinerja yang luar biasa untuk DSU. Dengan kedua teknik ini, kompleksitas waktu amortisasi untuk operasi `Find` dan `Union` mendekati O(α(n)), di mana α(n) adalah inverse Ackermann function. Inverse Ackermann function tumbuh sangat lambat, sehingga dalam praktiknya, kompleksitas waktu ini bisa dianggap konstan (O(1)).

## Contoh Penggunaan Disjoint Set Union

Mari kita lihat contoh penggunaan DSU untuk mencari komponen terhubung dalam graf. Misalkan kita punya graf dengan 5 node (1 sampai 5) dan beberapa edge:

- (1, 2)
- (2, 3)
- (4, 5)

Kita bisa menggunakan DSU untuk mencari tahu berapa banyak komponen terhubung yang ada dalam graf ini.

1. **Inisialisasi DSU:** Kita inisialisasi DSU dengan 5 elemen, masing-masing mewakili sebuah node.
2. **Proses Edge:** Untuk setiap edge (u, v), kita panggil `Union(u, v)`. Ini menggabungkan himpunan yang berisi node `u` dan `v`.
3. **Cari Jumlah Komponen:** Setelah memproses semua edge, kita bisa mencari jumlah komponen terhubung dengan menghitung berapa banyak node yang merupakan "orang tua" dari dirinya sendiri (root).

Setelah menjalankan algoritma DSU dengan edge yang diberikan, kita akan mendapatkan dua komponen terhubung: 1, 2, 3 dan 4, 5.

## Kesimpulan

Disjoint Set Union adalah struktur data yang powerful dan efisien untuk menyelesaikan masalah yang melibatkan pengelompokan dan konektivitas. Dengan teknik Path Compression dan Union by Rank, kita bisa meningkatkan kinerja DSU secara signifikan. Sekarang, giliran kamu buat eksplorasi lebih lanjut dan coba terapkan DSU di berbagai masalah! Punya pengalaman menarik dengan DSU? Share di kolom komentar, yuk!

## FAQ

**1\. Apa bedanya Disjoint Set Union dengan struktur data lain seperti Linked List?**

Linked List bisa digunakan untuk menyimpan sekumpulan elemen, tapi DSU lebih fokus pada pengelompokan elemen ke dalam himpunan yang saling lepas dan mencari tahu himpunan mana yang dimiliki sebuah elemen dengan cepat. DSU dengan Path Compression dan Union by Rank jauh lebih efisien untuk operasi `Find` dan `Union` dibandingkan dengan Linked List.

**2\. Kapan sebaiknya menggunakan Disjoint Set Union?**

DSU cocok digunakan ketika kita perlu melacak sekumpulan elemen yang terbagi menjadi beberapa himpunan yang saling lepas dan kita perlu melakukan operasi `Find` dan `Union` secara efisien. Contohnya, dalam masalah mencari komponen terhubung dalam graf atau mendeteksi siklus.

**3\. Apakah ada batasan dalam penggunaan Disjoint Set Union?**

DSU biasanya digunakan untuk masalah yang melibatkan himpunan yang statis. Artinya, elemen tidak ditambahkan atau dihapus dari himpunan setelah inisialisasi. Jika kita perlu melakukan operasi penambahan atau penghapusan elemen, struktur data lain mungkin lebih cocok.
