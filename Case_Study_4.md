# Case Study Modul 4
#### Muhammad Pirel Jenar Lubdhaka
#### 2306226681
#### Teknik Elektro 2023



X merupakan seorang mahasiswa Teknik Elektro yang sedang menempuh pembelajaran Dasar Sistem Digital. Suatu ketika Ia disuruh untuk membuat sebuah mesin besar, yang merupakan gabungan dari 4 mesin sekaligus (mesin A, B, C, D). Mesin tersebut bertujuan untuk menghasilkan dan membuat suatu barang. Suatu barang hanya dapat keluar dari mesin besar tersebut dengan kriteria sebagai berikut:

- Hanya mesin D sudah menyelesaikan tugasnya

- Hanya mesin C dan D sudah menyelesaikan tugasnya

- Mesin B dan C atau B dan D sudah menyelesaikan tugasnya

- Mesin B, C, dan D sudah menyelesaikan tugasnya

- Mesin A, B, dan C atau D sudah menyelesaikan tugasnya



## Permasalahan 1
Buatlah truth table dari soal cerita tersebut!

Solusi:



| A | B | C | D | O |
|---|---|---|---|---|
| 0 | 0 | 0 | 0 | 0 |
| 0 | 0 | 0 | 1 | 1 |
| 0 | 0 | 1 | 0 | 0 |
| 0 | 0 | 1 | 1 | 1 |
| 0 | 1 | 0 | 0 | 0 |
| 0 | 1 | 0 | 1 | 1 |
| 0 | 1 | 1 | 0 | 1 |
| 0 | 1 | 1 | 1 | 1 |
| 1 | 0 | 0 | 0 | 0 |
| 1 | 0 | 0 | 1 | 1 |
| 1 | 0 | 1 | 0 | 0 |
| 1 | 0 | 1 | 1 | 1 |
| 1 | 1 | 0 | 0 | 0 |
| 1 | 1 | 0 | 1 | 1 |
| 1 | 1 | 1 | 0 | 1 |
| 1 | 1 | 1 | 1 | 1 |



## Permasalahan 2
Carilah formula yang telah disederhanakan dari truth table yang telah dibuat!

Solusi:

Penyederhanaan akan dilakukan dengan menggunakan Kernaugh Map. Berikut adalah Kernaugh Map yang dibuat:


| ##### | CD    | 00    | 01    | 11    | 10    |
|-------|-------|-------|-------|-------|-------|
| AB    | ##### | ##### | ##### | ##### | ##### |
| 00    | ##### | 0     | 1     | 1     | 0     |
| 01    | ##### | 0     | 1     | 1     | 1     |
| 11    | ##### | 0     | 1     | 1     | 1     |
| 10    | ##### | 0     | 1     | 1     | 0     |

Berikut adalah kelompok-kelompok Implicant dari K-Map yang didapat:


| ##### | CD    | 00    | 01    | 11    | 10    |
|-------|-------|-------|-------|-------|-------|
| AB    | ##### | ##### | ##### | ##### | ##### |
| 00    | ##### | 0     | 1 @   | 1 @   | 0     |
| 01    | ##### | 0     | 1 @   | 1 @   | 1 %   |
| 11    | ##### | 0     | 1 @   | 1 @   | 1 %   |
| 10    | ##### | 0     | 1 @   | 1 @   | 0     |

Berikut adalah minterm-minterm yang didapatkan:

Kelompok @:

1. Variabel A mengalami perubahan nilai, abaikan
2. Variabel B mengalami perubahan nilai, abaikan
3. Variabel C mengalami perubahan nilai, abaikan
4. Variabel D memiliki nilai tetap, dengan nilai 1, D
5. Minterm yang didapatkan = D

Kelompok %:

1. Variabel A mengalami perubahan nilai, abaikan
2. Variabel B memiliki nilai tetap, dengan nilai 1, B
3. Variabel C memiliki nilai tetap, dengan nilai 1, C
4. Variabel D memiliki nilai tetap, dengan nilai 0, D'
5. Minterm yang didapatkan = BCD'

Ekspresi sederhana yang didapatkan adalah:

```
F = BCD' + D
```



## Permasalahan 3
Buatlah rangkaian tersebut pada Proteus!

Solusi:

Berikut adalah skema rangkaian yang dibuat telah dibuat pada proteus:

![Proteus_1](https://github.com/pirel624/Dasar_Sistem_Digital/blob/cf2130bd64ae931bcd34f7a549ab07aa9007391e/Case%20Study%204_Elementary%20Digital%20System.BMP)



## Permasalahan 4
Suatu ketika IC yang ingin kalian gunakan habis, dan kalian hanya memiliki IC NAND, NOR, XOR, dan XNOR. Bagaimana cara kalian menyelesaikan masalah tersebut? Buatlah rangkaian menggunakan IC tersebut pada Proteus! **TIDAK DIPERKENANKAN MENGGUNAKAN IC NOT!**

Solusi:

Berikut adalah rangkaian substitusi, hanya dengan menggunakan IC NAND:

![Proteus_NAND](https://github.com/pirel624/Dasar_Sistem_Digital/blob/d68bbae354045a54de2d2e3a999f551b0f313841/Case%20Study%204_Elementary%20Digital%20System%202.bmp)



## Permasalahan 5
Berikan analisis dari rangkaian yang telah kalian buat!

Solusi:

Pertama, mari kita lihat bentuk dari ekspresi aljabar boolean yang mewakili logika dari rangkaian tersebut:

```
F = BCD' + D
```

Ekspresi tersebut ada dalam bentuk Sums of Products. Dalam bentuk ini, kita dapat secara sistematis melakukan operasi dengan tahap: inversi (NOT), irisan (AND), dan gabungan (OR).

Pada rangkaian yang saya buat, komponen yang paling kiri merupakan kolom hex inverter 7404. Bagian ini berfungsi untuk mendapatkan nilai komplement dari setiap input A, B, C, dan D.

Berikutnya, pada bagian tengah, terdapat gerbang AND 7408. Bagian ini berfungsi untuk mengolah output dari bagian kiri menjadi output-output sesuai dengan minterm yang ada (dalam kasus ini, BCD' dan D). Untuk kemudahan, saya harusnya menggunakan satu gerbang AND dengan tiga input untuk mengakomodasi sinyal B, C, dan D'. Tetapi sayangnya saya tak dapat menemukan gerbang tersebut. Oleh karena itu saya substitusi dengan 2 gerbang AND input ganda, dengan output gerbang pertama dihubungkan dengan salah satu input gerbang kedua.

Bagian terakhir, yang paling kanan, terdapat satu gerbang OR. Gerbang ini berguna untuk menSUMkan produk produk yang dihasilkan oleh gerbang-gerbang AND yang ada di bagian tengah rangkaian. Dalam kasus ini, input satu dari gerbang OR adalah BCD' dan input duanya adalah D.

Output dari gerbang OR adalah output dari keseluruhan sistem logika yang diminta. Untuk mengindikasikan nilainya, output ini dihubungkan dengan LED dan resistor 1000 Ohms. Resistor berguna untuk memecah tegangan sehingga LED tidak terbakar.



## Permasalahan 6
Berikan analisis dari rangkaian yang menggunakan **gerbang kombinasional & universal** yang telah kalian buat!

Solusi:

Analisis yang dapat diambil dari rangkaian yang ini hanyalah bahwa setiap gerbang dari rangkaian awal telah disubstitusi dengan ekuivalen versi NANDnya.



## Permasalaahan 7
Berikan kesimpulan dari praktikum hari ini!

Solusi:

1. Dalam keadaan dimana tidak terdapat suatu gerbang logika, maka dapat disubstitusikan dengan gerbang universal atau gerbang kombinasi.
2. Gerbang universal dapat digunakan secara total untuk mengstreamline proses desain dan produksi.
3. Truth Table penting untuk didapatkan dengan benar dan akurat nilainya. Rancangan dapat melenceng dari keinginan apabila Truth Table memiliki kesalahan.
4. Alat alat simulasi dan diagnostik seperti Proteus memiliki peran besar dalam memudahakan proses desain dan debugging rancangan. Ada baiknya alat alat ini dikuasai.


