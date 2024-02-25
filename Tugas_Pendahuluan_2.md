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
Contoh:\
[A.B = B.A]\
[A+B = B+A]

2. Kaidah Asosiatif
Kaidah ini menyatakan bahwa urutan dilakukannya operasi pada sederet operand tidaklah berpengaruh apabila seluruh operatornya sama.
Contoh:\
[(A.B).C = A.(B.C)]\
[(A+B)+C = A+(B+C)]

3. Kaidah Distributif
Kaidah ini menyatakan bahwa operasi dapat "disebar" ke beberapa term yang dipengaruhinya.
Contoh:\
[A.(B+C) = (A.B)+(A.C)]\
[A+(B.C) = (A+B).(A+C)]

4. Kaidah AND
Kaidah ini berlaku pada operasi AND\
[A.0 = 0]\
[A.1 = A]\
[A.A = A]\
[A.!A = 0]

5. Kaidah OR
Kaidah ini berlaku pada operasi OR\
[A+0 = A]\
[A+1 = 1]\
[A+A = A]\
[A+!A = 1]

6. Kaidah Invers
Kaidah ini menyatakan bahwa inversi ganda pada satu variabel menghasilkan nilai yang sama dengan variabel itu sendiri.\
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

![Decimal to Binary (Definition, Conversion, Table and Examples)](data:image/png;base64,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)

Berikut ini adalah langkah yang harus dilakukan untuk mengkonversi bilangan biner ke bilangan desimal:

1. Tulis bilangan binernya dan catat pangkatnya dari kanan ke kiri (mulai dari 0)
2. Tulis setiap digit bilangan dari nomor 1 disertai dengan perkalian dengan 2 pangkatnya dari kanan ke kiri, sehingga digit pertama akan dikalikan dengan 2 pangkat terbesar
3. Jumlahkan seluruh produk dari tahap 2
4. Hasilnya adalah bilangan desimal yang diinginkan.



## Permasalahan 5
Ubahlah bilangan desimal di bawah ini menjadi bilangan biner, sertakan langkah-langkahnya! \
a. 15\
b. 27

Solusi:
a. \
15 / 2 = 7 || 15 % 2 = 1\
7 / 2 = 3 || 7 % 2 = 1\
3 / 2 = 1	|| 3 % 2 = 1\
Hasil => 1111

b.\
27 / 2 = 13 || 27 % 2 = 1\
13 / 2 = 6 || 13 % 2 = 1\
6 / 2 = 3 || 6 % 2 = 0\
3 / 2 = 1 || 3 % 2 = 1\
Hasil=> 11011
