# Tugas Pendahuluan Modul 2
#### Muhammad Pirel Jenar Lubdhaka
#### 2306226681
#### Teknik Elektro 2023

## Permasalahan 1
Jelaskan apa yang dimaksud dengan aljabar boolean, serta berikan contoh penerapannya!

Solusi:

Aljabar boolean adalah sistem aljabar yang mana operator dan logika mendasarnya adalah operator boolean sementara operand dasarnya adalah nilai biner/boolean. Sistem ini digunakan untuk memetakan dan memanipulasi sistem gerbang logika, juga untuk mengecek kebenaran pernyataan logika.

Contoh dari penerapan aljabar boolean adalah pada pembuatan desain gerbang logika berdasarkan pada suatu tabel kebenaran. Awalnya, dari tabel kebeneraan akan didapatkan sejumlah term yang menyatakan output dari gerbang logika, berdasarkan inputnya, sejumlah term ini dinamakan bentuk kanonik. Dari bentuk kanonik ini, akan diterapkan aljabar boolean dan identitas identitasnya sehingga didapatkan persamaan boolean yang lebih sederhana. Kemudian, apabila persamaan boolean ini sudah paling sederhana, desain gerbang logika akan dibuat berdasarkannya dengan bantuan Kernaugh Map untuk mendapatkan hasil yang paling optimal.



## Permasalahan 2
Sebutkan dan jelaskan minimal lima kaidah aljabar boolean!

Solusi:

1. Kaidah Komutatif
Kaidah ini menyatakan bahwa untuk seluruh operasi biner, letak dari operand dapat dibolak balik. Dalam kata lain, selama kedua operand masih dioperasikan oleh satu operator yang sama, maka letaknya didalam persamaan aljabar linear tidak berpengaruh kepada hasilnya.
Contoh:
A.B = B.A
A+B = B+A

2. Kaidah Asosiatif
Kaidah ini menyatakan bahwa urutan dilakukannya operasi pada sederet operand tidaklah berpengaruh apabila seluruh operatornya sama.
Contoh:
(A.B).C = A.(B.C)
(A+B)+C = A+(B+C)

3. Kaidah Distributif
Kaidah ini menyatakan bahwa operasi dapat "disebar" ke beberapa term yang dipengaruhinya.
Contoh:
A.(B+C) = (A.B)+(A.C)
A+(B.C) = (A+B).(A+C)

4. Kaidah AND
Kaidah ini berlaku pada operasi AND
A.0 = 0
A.1 = A
A.A = A
A.!A = 0

5. Kaidah OR
Kaidah ini berlaku pada operasi OR
A+0 = A
A+1 = 1
A+A = A
A+!A = 1

6. Kaidah Invers
Kaidah ini menyatakan bahwa inversi ganda pada satu variabel menghasilkan nilai yang sama dengan variabel itu sendiri.
!!A = A



## Permasalahan 3
Apa yang dimaksud dengan gerbang logika? Sebutkan contoh gerbang logika dasar beserta tabel kebenarannya (truth table) dan berikan contoh IC dari gerbang logika tersebut!

Solusi:
Gerbang logika adalah implementasi fisik dari operator yang didefinisikan pada aljabar boolean. Terdapat banyak gerbang logika, tetapi yang mendasari seluruh gerbang logika adalah 3 gerbang logika berikut:

Gerbang AND
Gerbang ini memiliki 2 input atau lebih. Gerbang ini akan mengeluarkan nilai HIGH apabila seluruh inputnya bernilai HIGH. Berikut adalah tabel kebenarannya:


| Input 1 | Input 2 | Output |
|---------|---------|--------|
| 1       | 1       | 1      |
| 1       | 0       | 0      |
| 0       | 1       | 0      |
| 0       | 0       | 0      |

Berikut adalah contoh ICnya:
74x08
74x11
74x21

Gerbang OR
Gerbang ini memiliki 2 input atau lebih. Gerbang ini mengeluarkan nilai HIGH apabila salah satu dari inputnya memiliki nilai HIGH. Berikut adalah tabel kebenarannya:


| Input 1 | Input 2 | Output |
|---------|---------|--------|
| 1       | 1       | 1      |
| 1       | 0       | 1      |
| 0       | 1       | 1      |
| 0       | 0       | 0      |

Berikut adalah contoh ICnya:
74x32
74x4075
74x4072
74x4078

Gerbang NOT
Gerbang ini memiliki 1 atau lebih input dan output. Gerbang ini akan mengeluarkan nilai kebalikan dari inputnya. Berikut adalah tabel kebenarannya:


| Input | Output |
|-------|--------|
| 1     | 0      |
| 0     | 1      |

Berikut adalah contoh ICnya:
74x04



## Permasalahan 4

