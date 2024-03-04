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

1. Ada perubahan pada A2, abaikan
2. Tidak ada perubahan pada A1, bernilai 0, A1'
3. Tidak ada perubahan pada A0, bernilai 0, A0'
4. Minterm -> A1'A0'

Kelompok $:

1. Tidak ada perubahan pada A2, bernilai 1, A2
2. Ada perubahan pada A1, abaikan
3. Ada perubahan pada A0, abaikan
4. Minterm -> A2

Kelompok %:

1. Tidak ada perubahan pada A2, bernilai 0, A2'
2. Ada perubahan pada A1, abaikan
3. Tidak ada perubahan pada A0, bernilai 0, A0'
4. Minterm -> A2'A0'

Hasil:
```
F = A1'A0' + A2 + A2'A0'
F = A0'(A1' + A2') + A2
```



## Permasalahan 3
Jelaskan perbedaan proses penyederhanaan melalui aljabar boolean dan K-map, apakah hasil persamaan akhir yang diperoleh akan sama?

Solusi:

Tidak ada perbedaaan hasil akhir dari kedua metode tersebut. Perbedaan utama dari keduanya adalah bahwa K-Map memiliki algoritmanya tersendiri, memiliki prosedur jelasnya tersendiri, sehingga analisis yang dilakukan bersifat replicable dan prosedural. Sementara penyederhanaan menggunakan prinsip dasar aljabar memerlukan kognisi yang lebih berat lagi.

Analogi yang dapat saya ajukan adalah, apabila disiplin ilmu Aljabar Linear memiliki metode Gauss-Jordan sebagai alat utama untuk menyederhanakan sistem persamaan linear, Ilmu Logika memiliki K-Map sebagai alat utama untuk menyederhanakan proposisi logika boolean.



## Permasalahan 4
Berikan analisis rangkaian yang telah dibuat, apakah kombinasi input-output pada rangkaian sama dengan truth table? Sertakan foto dari rangkaian fisik yang dibuat saat praktikum!

Solusi:

![Rangkaian](https://github.com/pirel624/Dasar_Sistem_Digital/blob/39d4e276e37b4d6c3b584f9d16a5bcfb1b144995/CaseStudy3.jpg)

Analisis akan diberi sebagaimana rangkaian disusun.

Pertama, sumber daya 5V dihubungkan dengan bagian terluar _Power Strips_ dan Gnd, dihubungkan dengan yang terdalam. Bagian ini akan digunakan sebagai Vcc dan Gnd untuk seluruh rangkaian.

Berikutnya, chip IC7404, IC7408, dan IC7432 dipasang di tengah breadboard, sehingga setiap pinoutnya dijabarkan oleh baris-baris _Terminal Strips_. Rangkaian seperti ini berguna untuk mengakses pin-pin tersebut dengan mudah.

Berikutnya, pin 7 dan 14 dari masing masing chip dihubungkan dengan Gnd dan Vcc secara berurutan. Rangkain ini berfungsi untuk "mengaktifkan" fungsi ketiga IC tersebut.

Siapkan kabel jumper hijau, biru, dan orange, masing masing merepresentasikan input A, B, dan C.

Sambungkan input A dengan pin 1 dari IC7404, lalu sambungkan pin 2 dengan pin 1 dari IC7408. Sambungkan input C dengan pin 2 dari IC7408. Rangkain ini mewakili operasi A'C, dan outputnya terdapat pada pin 3 dari IC7408.

Sambungkan input A dan B dengan pin 4 dan pin 5 dari IC7408.
Sambungkan input C dengan pin 3 dari IC7404, kemudian sambungkan pin 4 dari IC7404 dengan pin 13 dari IC7408. Sambungkan pin 6 IC7408 dengan pin 12 IC7408. Rangkain ini mewakili operasi AC'B. Output dari operasi ini pada pin 11 dari IC7408.

Sambungkan pin 11 dan pin 3 dari IC 7408 dengan pin 1 dan 2 dari IC7432. Rangkain ini adalah penghujung dari ekspresi boolean yang diinginkan, pin 3 dari IC7432 adalah outputnya.

Sambungkan output tadi dengan lampu led dan resistor 1k ohm, secara seri, Lampu ini akan menjadi indikator nilai output (MENYALA = HIGH, MATI = LOW).

Sayangnya, rangkaian tidak mengikuti Truth Table. Kami menyangka bahwa ada kesalahan saat menyederhanakan bentuk kanonik yang diberikan oleh Truth Table.



## Permasalahan 5
Berikan kesimpulan dari keseluruhan percobaan dalam bentuk poin-poin!

Solusi:

Kesimpulan terbesar yang dapat kami ambil adalah bahwa K-Map adalah alat yang sangat berguna untuk menyederhanakan bentuk kanonik dari ekspresi boolean. Case Study ini mirip dengan Case Study 2, hanya saja kali ini kami menyederhanakan ekspresi boolean dengan menggunakan K-Map, dengan lebih mudah dan lebih cepat.

1. K-Map adalah alat analisis aljabar boolean yang sangat efisien
2. K-Map sering kali adalah alat yang paling optimal untuk menyederhakankan ekspresi boolean
3. Debugging pada setiap tahap perangkain sangatlah penting, agar tidak terjadi seperti pada kami.



