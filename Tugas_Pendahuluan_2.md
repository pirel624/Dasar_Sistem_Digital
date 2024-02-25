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
[A.B = B.A]
[A+B = B+A]

2. Kaidah Asosiatif
Kaidah ini menyatakan bahwa urutan dilakukannya operasi pada sederet operand tidaklah berpengaruh apabila seluruh operatornya sama.
Contoh:
[(A.B).C = A.(B.C)]
[(A+B)+C = A+(B+C)]

3. Kaidah Distributif
Kaidah ini menyatakan bahwa operasi dapat "disebar" ke beberapa term yang dipengaruhinya.
Contoh:
[A.(B+C) = (A.B)+(A.C)]
[A+(B.C) = (A+B).(A+C)]

4. Kaidah AND
Kaidah ini berlaku pada operasi AND
[A.0 = 0]
[A.1 = A]
[A.A = A]
[A.!A = 0]

5. Kaidah OR
Kaidah ini berlaku pada operasi OR
[A+0 = A]
[A+1 = 1]
[A+A = A]
[A+!A = 1]

6. Kaidah Invers
Kaidah ini menyatakan bahwa inversi ganda pada satu variabel menghasilkan nilai yang sama dengan variabel itu sendiri.
[!!A = A]



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
Jelaskan bagaimana cara melakukan konversi terhadap bilangan desimal menjadi bilangan biner dan sebaliknya!

Solusi:
Berikut ini adalah langkah yang harus dilakukan untuk merubah bilangan desimal ke bilangan biner:

1.  Bagi bilangan desimal awal dengan 2, catat nilai sisa dan hasilnya
2. Sekarang, bagi nilai hasil yang didapat pada langkah 1 dengan 2, dan lagi lagi catat hasil dan sisanya.
3. Ulangi langkah diatas hingga didapatkan hasil senilai 1
4. Sekarang, tulis nilai sisa dengan urutan terbalik (dari yang terakhir ke yang awal)

Least Significant Bit (LSB) ada pada penghujung sedangkan Most Significant Bit (MSB) ada pada awal.

![Decimal to Binary Conversion Methods - Examples & Explanation - Circuit  Globe](data:image/jpeg;base64,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)


