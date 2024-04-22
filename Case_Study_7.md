# Case Study Modul 7 DSD
#### Muhammad Pirel Jenar Lubdhaka
#### 2306226681
#### Teknik Elektro 2023



## Permasalahan 1
Berapa bit yang dibutuhkan untuk kedua input, dan berapa jumlah bit yang dibutuh untuk output agar tidak ada data yang hilang. Jelaskan jawaban anda.

Solusi:
Didapatkan dari perintah soal bahwa dua variabel yang akan dijadikan operand memiliki nilai maksimal 3 (0 - 3). Berarti, setiap variabel memiliki 4 permutasi _state_, yang berarti setiap variabel berdigit 2 bit.

Maka: Input = 2 x 2 bit

Dalam dari seluruh kemungkinan nilai yang dapat didapat dari menjumlahkan kedua variabel tersebut, nilai yang terbesar adalah 6 (110). Maka, untuk mengakomodasi output, diperlukan _bus length_ sebesar 3 bit.

Maka: Output = 1 x 3 bit.

Catatan:
Dari ini kita juga dapat membuat generalisasi bahwa untuk setiap ADDER dengan input n bit, maka outputnya sepanjang n + 1 bit.



## Permasalahan 2
 
