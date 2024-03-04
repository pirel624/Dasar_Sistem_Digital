# Case Study Modul 3
#### Muhammad Pirel Jenar Lubdhaka
#### 2306226681
#### Teknik Elektro 2023



## Truth Table:



| A 2 | A 1 | A 0 | 0 |
|-----|-----|-----|---|
| 0   | 0   | 0   | 1 |
| 0   | 0   | 1   | 0 |
| 0   | 1   | 0   | 1 |
| 0   | 1   | 1   | 0 |
| 1   | 0   | 0   | 1 |
| 1   | 0   | 1   | 1 |
| 1   | 1   | 0   | 0 |
| 1   | 1   | 1   | 1 |



## Permasalahan 1
Apakah persamaan tersebut di dalam bentuk SOM atau POM? Apa yang membedakan keduanya dan bagaimana cara mengkonversi dari 1 bentuk ke bentuk lainnya?

Solusi:

Persamaan tersebut ada dalam bentuk Sum of Minterm. Yang membedakan keduanya adalah bahwa pada SOM setiap suku menyatakan salah satu kondisi dimana outputnya akan bernilai HIGH, sementara pada POM setiap suku menyatakan salah satu syarat agar outputnya bernilai HIGH.

Salah satu cara untuk mengonversi bentuk POS ke SOM dan sebaliknya adalah dengan memanfaatkan prinsip _De Morgan_.

```
F  = xy' + yz'
F' = (xy' + yz')'
   = (xy')'(yz')'
   = (x'+y)(y'+z)
   = x'y' + x'z + yy' + yz
   = x'y' + x'z + yz
F  = F''
   = (x'y'+x'z+yz)'
   = (x'y')'(x'z)'(yz)'
   = (x+y)(x+z')(y'+z')
   = (x+y)(y'+z')
``` 

Cara lain yang dapat digunakan untuk mengonversi satu bentuk ke bentuk yang lainnya adalah dengan menggunakan K-Map.



## Permasalahan 2
Sederhanakan persamaan tersebut menggunakan metode K-map, jelaskan langkah-langkah yang digunakan

Solusi:

Langkah pertama, buat tabel K-Map dari tabel kebenaran diatas.
Langkah yang dilakukan adalah, melangkahlah ke setiap sel pada K-Map, tentukan sekuens inputnya, acu kembali pada tabel kebenaran, apabila di tabel kebenaran sekuens tersebut menghasilkan nilai 1, maka isi sel tersebut dengan 1, begitu pula sebaliknya.

| ##### | A1,A0 | 00    | 01    | 11    | 10    |
|-------|-------|-------|-------|-------|-------|
| A2    | ##### | ##### | ##### | ##### | ##### |
| 0     | ##### | 1     | 0     | 0     | 1     |
| 1     | ##### | 1     | 1     | 1     | 0     |

Lalu, buatlah kelompok-kelompok dari K-Map berdasarkan kriteria berikut:


1. Kelompok harus memiliki area 2, 4, 8, dst (2 pangkat)
2. Kelompok harus terdiri dari sel bernilai 1 
3. Kelompok merupakan kelompok terbesar yang dapat dibuat
4. Kelompok dibolehkan untuk tumpang tindih
5. Apabila terdapat sel yang belum dikelompokkan, hubungkan dengan sel di posisi yang berlawanan. Bayangkan teselasi dari K-Map tersebut.



| ##### | A1,A0 | 00    | 01    | 11    | 10    |
|-------|-------|-------|-------|-------|-------|
| A2    | ##### | ##### | ##### | ##### | ##### |
| 0     | ##### | 1 @ % | 0     | 0     | 1   % |
| 1     | ##### | 1 @$  | 1  $  | 1  $  | 0     |

Apabila sudah didapatkan kelompok-kelompoknya, buatlah termnya berdasarkan syarat ini:

1. Apabila kelompok tersebut hanya memiliki satu nilai asosiasi terhadap variabel X, dengan nilainya adalah 1, maka catat operand "X".
2. Apabila kelompok tersebut hanya memiliki satu nilai asosiasi terhadap variabel Y, dengan nilainya adalah 0, maka catat operand "Y'".
3. Apabila kelompok tersebut memiliki dua nilai asosiasi terhadap variabel Z, abaikan variabel Z.
4. Ulangi hingga setiap variabel terhitung
5. Jika sudah, ANDkan seluruh operand yang tercatat.
6. hasil dari operasi AND tersebut adalah _Prime Implicant_ dari kelompok tersebut.
7. Sum dari semua _Prime Implicant_ yang didapatkan adalah hasil dari Karnaugh Map.


Kelompok @:




