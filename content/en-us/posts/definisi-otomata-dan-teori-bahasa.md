---
title: 'Definisi Otomata dan Teori Bahasa'
date: Mon, 13 Mar 2023 16:12:32 +0000
draft: false
tags: ['Pendidikan']
---

Definisi Otomata
----------------

Jenis mesin sederhana yang dapat menerima inputan, dapat melakukan pemyimpanan sementara, serta dapat mengambil keputusan atau kesimpulan dari input yang diberikan.

Simbol State
------------

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiHIpP0Lr-I500II9fgWvCT_JU5JPJjpzJlyjdFpfXsOiG98xjJEtSMCfZan8MRvRsf0SVxO24MHLw9-jv70LfvSLUkU9CLVxqgUdV0lAL1JyghC3aCjq6-6fNh-sOXr5a__Y9Buq72Fj7UCwMIV4DPZG6rGCo4k0rYPBJtGcVL6oCDL-482DKe85bt/s1600/otomata.png "simbol state")

Table
-----

0

1

q1

q2

q3

q2

q1

q1

q3

q3

q2

Cara Baca Table
---------------

*   q1 diberi inputan 0 menuju ke q2
*   q1 diberi inputan 1 menuju ke q3
*   q2 diberi inputan 0 menuju ke q1
*   q2 diberi inputan 1 menuju ke q1
*   q3 diberi inputan 0 menuju ke q3
*   q3 diberi inputan 1 menuju ke q2

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhkSSkBUF9IX-yOcEZgABFGOFxud-GIuUeyShvg5BluddOVxBk6qG9PIzY0vADQ88cMZfRJrOlZJ6BzkW-BJcCSqwp68H-yco6nmai0BzQLOuhwvXx-QoGXZ6ZhOdIQSbxDN48lhIF3VvISAxFYZbMj8ZtLGdqLXBi24rSRH12HK9vgsA4M2PYjrpzl/s1600/state.png "simbol state")

**Baca juga**: [Pengertian, Jenis, dan Contoh Soal Finite State Automata](https://blog.ajiekusumadhany.com/pengertian-jenis-finite-state-automata/)

Contoh
------

**1.Misal diberi input 11001** maka: q1->q3->q2->q1->q2->q1 Hasilnya: inputan 11001 -> tidak diterima (ditolak) karena berhenti tidak di state terakhir. **2.Misal diberi input 110001** maka: q1->q3->q2->q1->q2->q1->q3 Hasilnya: inputan 110001 -> diterima karena berhenti di state terakhir.