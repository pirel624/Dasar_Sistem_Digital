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
Jelaskan mengapa sebaiknya menggunakan ripple carry adder dibanding membuat rangkaian menggunakan truth table dan k-map (Hint: apa yang terjadi jika range input diperbesar)

Solusi:
Ripple Carry Adder, dan aturan yang menyarankan penggunaannya, diadakan untuk menyelesaikan masalah bahwa semakin besar _bus length_ dari suatu ADDER, maka akan semakin besar pula Truth Tablenya, membesar secara eksponensial. Jadi idenya adalah, bagaimana bila hanya dibuat beberapa set ADDER dengan _bus length_ yang terstandar (3 bit (octal), 8 bit (c_word), 16 bit (hexadecimal)), dan apabila diperlukan suatu ADDER dengan _bus length_ yang lebih besar, maka ADDER standar tadi dapat digabungkan dengan menggunakan Ripple Carry ADDER.



## Permasalahan 3
Berikanlah analisis terhadap rangkaian yang dibuat. Sertakan foto rangkaian fisik dan rangkaian Proteus yang telah dibuat!

Solusi:

Secara abstrak, rangkaian yang telah kami buat terdiri dari 2 Full Adder yang digabungkan, menghasilkan Adder yang dapat menerima 2 operand 2 bit, dan menghasilkan hasil summasi 3 bit. Penggabungan ini dilakukan dengan cara mengubungkan CARRY dari Full Adder 1 (bit _Least Significant_) dengan Cin dari Full Adder 2 (bit _Most Significant_).
SUM dari Full Adder 1 mewakili bit _Least Significant_ dari output (bit ketiga jika menggunakan standar Big Endian), SUM dari Full Adder 2 mewakili bit kedua, dan CARRY dari Full Adder 2 mewakili bit _Most Significant_ dari output.

Untuk setiap Full Adder, kami menggunakan gerbang AND, OR, dan XOR.

Berikut adalah implementasi Full Adder kami dengan menggunakan gerbang gerbang diatas:

![Full Adder Logic Circuit](data:image/png;base64,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)

Untuk mengimplementasikan gerbang AND, kami menggunakan IC 7408, untuk mengimplementasikan gerbang OR, kami menggunakan IC 7432, dan untuk mengimplementasikan gerbang XOR, kami menggunakan IC 7486.

Untuk mengimplementasikan sistem input, kami hanya menggunakan _jumper wires_ yang dihubungkan dari Vcc terhadap input. Input yang kami pilih adalah  11 + 01.

Untuk mengimplementasikan output, kami menggunakan 3 lampu LED 3mm dengan ketiga pin negatifnya dihubungkan dengan satu resistor 1k ohm yang terhubung dengan ground. Lampu yang menyala (Paling atas menyala, 2 dibawahnya mati), mengindikasikan output bernilai 4 (100). Secara keseluruhan, kami berhasil membuat Full Adder 2 bit.

Berikut adalah foto dari rangkaian yang telah kami buat:

![2 Bit Full Adder Physical](https://github.com/pirel624/Dasar_Sistem_Digital/blob/eb52e204819a523d49be5769d872a6fd1f61289c/Ranngkaian_Fisik_2Bit_Full-Adder.png)





## Permasalahan 4
Soal Bonus



## Permasalahan 5
Jika anda tidak memiliki akses internet atau buku referensi. Bagaimana cara mendapat rangkaian full adder dan half adder.

Solusi:
Apabila saya tidak mendapatkan akses terhadap internet, yang pertama saya lakukan adalah membuat truth table dari semua kombinasi input dan output dari half adder dan full adder 1 bit. Ini dapat dilakukan secara realistik sebab _bus length_ dari kedua adder hanyalah 1 bit, sehingga Truth Table yang dihasilkan cukuplah kecil.

Berikutnya, saya akan menggunakan Kernaugh Map untuk mendapatkan persamaan aljabar boolean sederhana untuk setiap output dan input dari setiap adder.

Setelah mendapatkan persamaannya, saya akan mengimplementasikannya dengan 3 gerbang logika universal (AND, OR, dan NOT).

Hasilnya adalah rangkaian Half Adder dan Full Adder. Dari ini saya dapat membuat rangkain ADDER n bit lengkap.



## Permasalahan 6
Berikan kesimpulan dari praktikum dalam bentuk poin-poin!

Solusi:
1. Truth Table dan Kernaugh Map dapat digunakan untuk merancang Half Adder seandainya akses terhadap internet diputus.
2. Half Adder dapat digunakan untuk merancang Full Adder.
3. Full Adder dapat digabungkan untuk menghasilkan Adder dengan berbagai ukuran _bus length_.


