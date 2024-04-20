# Tugas Pendahuluan 7 DSD
#### Muhammad Pirel Jenar Lubdhaka
#### 2306226681
#### Teknik Elektro 2023



## Permasalahan 1
Jelaskan apa itu half adder, half subtractor, full adder and full subtractor! 

Solusi:
Untuk menjelaskan apa itu half adder, mari kita awali dengan penjumlahan biner.

01 A
00 B
-------+
01 C

Pada operasi diatas, tiap operand digitnya dapat kita bedakan menjadi digit _Least Significant_ (paling kanan) dan _Most Significant_ (paling kiri). 
Dari operasi di atas, kita mungkin dapat menarik kesimpulan bahwa jumlah (SUM) dari setiap bit akan berakhir di posisi bit yang sama pula.

Tetapi kesimpulan ini kurang tepat. Mari kita ambil kasus penjumlahan lain.

01 A
01 B
-------+
10 C

Pada kasus diatas, hasil jumlah bit paling kanan adalah 2 (10 dalam biner). Tetapi karena setiap digit biner hanya dapat mengakomodasi 2 permutasi nilai, maka nilai tambahan "dilempar" ke bit berikutnya, yaitu bit _Most Significant_. 
Dari ini dapat ditarik kesimpulan bahwa setiap operasi penjumlahan biner diawali dengan SUMmmation. Apabila nilai melebihi ambang batas (overflow), maka nilai dilempar ke bit yang lebih signifikan berikutnya, atau CARRYover.

HALF ADDER bekerja dengan cara yang sama.
Pada HALF ADDER, terdapat 2 input, yang mewakili bit YANG_TERTAMBAH dan bit YANG_MENAMBAH. Terdapat pula 2 output, yang mewakili _SUM_ dan _CARRY_. Andaikata output hasil penjumlahan adalah 2 digit biner, maka _SUM_ berkorespondensi dengan bit _Least Significant_ nya, dan _CARRY_ berkorespondensi dengan bit _Most Significant_ nya.

Half Substractor bekerja dengan prinsip yang sama.
Saat pengurangan dilakukan, akan dicek apakah bit YANG_DIKURANG dapat mengalami pengurangan oleh bit YANG_MENGURANG, atau harus meminjam (BORROW) nilai dari bit yang lebih signifikan. Jika pengurangan dapat dilakukan, maka akan didapatkan nilai perbedaannya (DIFFERENCE).

01
00
---- (-)
01
(1 dapat dikurangi 0)
(Maka tak perlu meminjam, BORROW = 0)
(Perbedaan 1 dengan 0 adalah 1)
(Maka, DIFFERENCE = 1)

10
01
------ (-) 
01
(0 tak dapat dikurangi 1)
(Maka perlu meminjam, BORROW = 1)
(Perbedaan 2 dengan 1 adalah 1)
(Maka DIFFERENCE = 1)

HALF SUBSTRACTOR bekerja dengan cara yang sama.
Terdapat 2 bit input, YANG_DIKURANG dan YANG_MENGURANG. Terdapat 2 bit output, _DIFFERENCE_ dan _BORROW_.

Perbedaan versi full dengan half dari kedua operator tadi hanya pada banyak inputnya. HALF ADDER dan HALF SUBSTRACTOR hanya dapat mengolah operasi antara 1 bit input saja. Sementara FULL ADDER/SUBSTRACTOR dapat mengoperasikan lebih dari 1 bit input. Hal ini dapat dicapai dengan saling merangkai sirkuit versi half masing masing.

Berikut contohnya.

Apabila CARRY dari HALF ADDER 1 dihubungkan dengan YANG_DITAMBAHKAN dari HALF ADDER 2, maka overflow dari input bit pertama dapat ditangani oleh operasi pada bit kedua. Dan apabila CARRY dari HALF ADDER 2 dihubungkan dengan YANG_DITAMBAH dari HALF ADDER 3, maka overflow dari operasi bit kedua dapat ditangani oleh operasi bit ke 3.

Secara teori, 9 HALF ADDER dapat menjumlahkan 2 variabel 8 bit (C_Word)
17 HALF ADDER dapat menjumlahkan 2 variabel 16 bit (C_Short)
Dan Seterusnya.



## Permasalahan 2
Jelaskan perbedaan antara half adder dan full adder!

Solusi:
Seperti yang telah dipaparkan pada permasalahan 1, full adder adalah gabungan dari beberapa half adder, sehingga operasi penjumlahan dapat dilakukan pada variabel dengan lebih dari 1 bit tanpa overflow ( Terdapat 1 half adder yang mengendalikan _Most Significant_ bit yang mana nilai CARRY nya selalu 0).

Untuk FULL ADDER operasi 1 bit, dibutuhkan 2 HALF ADDER
Untuk FULL ADDER operasi 2 bit, dibutuhkan 3 HALF ADDER
dan seterusnya.



## Permasalahan 3
Jelaskan perbedaan antara half subtractor dan full subtractor!

Solusi:
Seperti yang telah dipaparkan pada permasalahan 1, full substractor adalah gabungan dari beberapa half substractor, sehingga operasi pengurangan dapat dilakukan pada variabel dengan lebih dari 1 bit tanpa overflow ( Terdapat 1 half adder yang mengendalikan _Most Significant_ bit yang mana nilai BORROW nya selalu 0).

Untuk FULL SUBSTRACTOR operasi 1 bit, dibutuhkan 2 HALF SUBSTRACTOR
Untuk FULL SUBSTRACTOR operasi 2 bit, dibutuhkan 3 HALF SUBSTRACTOR
dan seterusnya.



## Permasalahan 4
Apa itu ripple carry adder dan ripple borrow subtractor? Jelaskan!

Solusi:
Untuk menjelaskannya, mari kita bayangkan deretan HALF ADDER yang tadi disinggung pada permasalaghan 1. Pada dasarnya, setiap HALF ADDER pada rangkaian FULL ADDER akan memiliki satu input yang berasal dari CARRY HALF ADDER sebelumnya. Fenomena ini, dimana nilai overflow, nilai CARRY, dilemparkan ke HALF ADDER berikutnya disebut dengan efek RIPPLE CARRY.

RIPPLE CARRY ADDER pada dasarnya adalah FULL ADDER yang mana salah satu input pada bit _Least Significant_ nya merupakan RIPPLE CARRY dari FULL ADDER lainnya. Secara efek, RIPPLE CARRY ADDER berfungsi untuk mengekstensi _bus size_ dari ADDER yang akan dibuat.

RIPPLE BORROW SUBSTRACTOR juga bekerja seperti prinsip ini.



## Permasalahan 5
Gambarkan rangkaian half adder dan half subtractor (dalam bentuk gerbang logika sederhana) serta truth table-nya!

Solusi:

Berikut adalah gambar dari rangkaian yang telah saya buat:
![Image_Circuit](https://github.com/pirel624/Dasar_Sistem_Digital/blob/8d0c6454cd7bf6d63f0e81114db2c00e6018c25d/HALF_ADDER_SUBSTRACTOR_CIRCUIT.png)

Berikut adalah Truth Table dari HALF ADDER:
```markdown
| YANG_DITAMBAHKAN | YANG_MENAMBAH | SUM | CARRY |
|------------------|---------------|-----|-------|
| 0                | 0             | 0   | 0     |
| 0                | 1             | 1   | 0     |
| 1                | 0             | 1   | 0     |
| 1                | 1             | 0   | 1     |
```




