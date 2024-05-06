---
title: 'Pengertian, Jenis, dan Contoh Soal Finite State Automata'
date: Mon, 13 Mar 2023 22:07:30 +0000
draft: false
tags: ['Pendidikan']
---

Apa itu Finite State Automata?
------------------------------

Finite state automata (FSA), atau dalam bahasa Indonesia disebut juga mesin automata berhingga, adalah model matematis yang digunakan untuk merepresentasikan sebuah sistem yang memiliki keterbatasan input yang dapat diterima. Finite state automata (FSA) dibagi menjadi 2 macam yaitu:

1.  Deterministic Finite Automata (DFA) : Mesin automata yang sudah teratur
2.  Non Deterministic Finite Automata (NDFA) : Mesin automata yang belum teratur

Untuk merancang sebuah mesin automata terdiri dari 5 komponen:

M = (Q , Σ , δ , S , F )

*   Q = himpunan state
*   Σ = himpunan simbol input
*   δ = fungsi transisi δ : Q × Σ
*   S = state awal / initial state , S ∈ Q
*   F = state akhir, F ⊆ Q

Perbedaan DFA dan NDFA
----------------------

Berikut adalah perbedaan antara Deterministic Finite Automata (DFA) dengan Non Deterministic Finite Automata (NDFA).

### Deterministic Finite Automata (DFA)

*   Sudah teratur
*   Jika diberikan inputan hanya mempunyai satu keputusan yaitu: diterima atau ditolak
    *   Diterima: jika berhenti pada state terakhir
    *   Ditolak: jika berhenti tidak pada state terakhir
*   Laku dijual di pasar

### Non Deterministic Finite Automata (NDFA)

*   Belum teratur
*   Jika diberi inputan mempunyai beberapa kemungkinan, yaitu:
    *   Diterima: jika berhenti di state akhir
    *   Ditolak: jika berhenti bukan di state akhir
    *   Macet: jika inputan belum habis tapi jalur sudah tidak ada
*   Belum laku / tidak laku dijual

**Baca juga**: [Definisi Otomata dan Teori Bahasa](https://blog.ajiekusumadhany.com/definisi-otomata-dan-teori-bahasa/)

Contoh Soal
-----------

**A**. Gambarkan FSA jika diketahui Fungsi Transisi Berikut:

δ

0

1

Q0

Q1

Q3

Q1

Q2

Q0

Q2

Q3

Q2

Q3

Q2

Q1

Jawab:

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEil-ekR_K7-kQCmcrEHkHWmhu5N-_HDuH3x-81Nx_sicNH4qdhLyC7xY_z3JWKdSGdjO4nxYhvFPhHNSY5p273HekFT-_BE-vCn8LCfUCzo6MyjOwFODSlP4IyNi5tG634oQ42fsGz_EJca1fWtpid0FDRri5o7C2bmQKcQE6t2tp8QNVq95ghmXbR6/w320-h255/IMG_20230308_193715.JPG)

Misal diberi inputan 1100101 maka: q0-q3-q1-q2-q3-q1-q2-q2 -(Ditolak) Misal diberi inputan 1010111 maka: q0-q3-q2-q2-q3-q1-q0-q3 -(Diterima) **B**. Gambarkan FSA jika diketahui Fungsi Transisi Berikut:

δ

0

1

Q0

Q1

Q2

Q1

\-

Q1,Q3

Q2

Q3

Q2

Q3

Q1

Q0

Jawab:

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEil0I7ZOHGJbFYYBs9NxKiAoKBBttiePDl0jDL5MFl2LsDFdHxBH5dyg4V8FDPYtf81nTScRFp7DKSAfLWtdd368NeX9K0_bsdvimhXgdkrV8_IGZw_Al2Rj8SvPI2OYj7cwRe315VPFs-eL9hVI7ud-ELaHPXQIe-F-AGduTMT_272KLUANa0qlDRV/w320-h245/IMG_20230308_193748.JPG)

Misal diberi inputan 1100011 maka: q0-q2-q2-q2-q3-q1-q1 -(Ditolak) q0-q3-q2-q2-q3-q1-q0-q3 -(Diterima)

Latihan Soal
------------

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEijGcKYbFyrWi6oWG_Z-xfm_viKQb7tLRRCHfzZr_Tft7Qhws1aAmJYhoRkkqDRzc3yXq0YH8cJcK8tZ2__aM4-yaemVuyKnQyKNs4Ae23_Q64x1dg9ZxNYl0TnDlCup6KTOJzSARKG9Sd-mkvqg9PvYZmF_ZdyV3IYOlxSyJhst1pGOirfljiLNyXb/s1600/IMG_20230308_194733.jpg) ![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjQSkO3BXWq9Xeo2JwgBO71NM7TXaF8jfyyydZU3BLeawE_Kzt8VgRinZYiKyHfpq5i0s9lqrIBdapwYWj6cE6nFMGzQwMyyW_fJTWVqm48N3jqRKDu1wzI3LvUjPk7rGyXyjRATCAH8LLSwR8jwfzJ7f35IjQQRxbiyB7Ag4zUd1AyKxexaQIPhUK9/s1600/IMG_20230308_194805.jpg)