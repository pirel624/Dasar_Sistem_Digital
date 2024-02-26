# Case Study Modul 2
#### Muhammad Pirel Jenar Lubdhaka
#### 2306226681
#### Teknik Elektro 2023

## Permasalahan 1
Tuliskan persamaan di atas dalam bentuk yang paling sederhana! Tuliskan langkah-langkah penyederhanaan dan kaidah yang digunakan! Setelah itu, buatlah rangkaiannya (sertakan foto rangkaian)!

Solusi:

O1 = B1 . !B2 + B2\
O1 = !!(B1 . !B2) + B2 **Prinsip Negasi Ganda**\
O1 = !(!B1 + B2) + B2 **Prinsip De Morgan 1**\
!O1 =  (!B1 + B2) . !B2\
!O1 = !B1 . !B2 + B2 . !B2 **Prinsip Distributif**\
!O1 = !B1 . !B2 **Prinsip Komplementasi 1**\
O1 = B1 + B2

O2 = !B1 . B3 + B1 . B3\
O2 = B3 . (!B1 + B1) **Prinsip Distributif**\
O2 = B3 **Prinsip Komplementasi 2**

O3 = !B1 + B2. !B3 + B1 . !B3\
O3 = (!B1 + B1 . !B3) + B2 . !B3 **Prinsip Asosiatif**\
O3 = !!(!B1 + B1 . !B3) + B2 . !B3 **Prinsip Negasi Ganda**\
O3 = !(B1 . (!B1 + B3)) + B2 . !B3 **Prinsip De Morgan 2**\
O3 = !(B1 . !B1 + B1 . B3) + B2 . !B3 **Prinsip Distributif**\
O3 = !(B1 . B3) + B2 . !B3 **Prinsip Komplementasi 1**\
O3 = !B1 + !B3 + B2 . !B3 **Prinsip De Morgan 2**\
O3 = !B1 + !B3 . (1 + B2) **Prinsip Distribusi**\
O3 = !B1 + !B3

Berikut adalah foto dari rangkaian yang dibuat:
![Foto Rangkaian](https://github.com/pirel624/Dasar_Sistem_Digital/blob/b9b18f623178ba6bb4e7cb833b4651ca65ac8aba/Foto%20Rangkaian.jpg)
![Gambar Rangkaian](https://github.com/pirel624/Dasar_Sistem_Digital/blob/9b2731da984bb2196a5440b05625652931d8dd00/Gambar%20Rangkaian.png)

[Link Tinkercad](https://www.tinkercad.com/things/aPLK7aeoMgD-pirel-2306226681-cs2)



## Permasalahan 2
Berdasarkan rangkaian yang telah dibuat, lengkapi tabel kebenaran berikut! 

| Input 3 | Input 2 | Input 1 | Output 3 | Output 2 | Output 1 |
|---------|---------|---------|----------|----------|----------|
| 0       | 0       | 0       |          |          |          |
| 0       | 0       | 1       |          |          |          |
| 0       | 1       | 0       |          |          |          |
| 0       | 1       | 1       |          |          |          |
| 1       | 0       | 0       |          |          |          |
| 1       | 0       | 1       |          |          |          |
| 1       | 1       | 0       |          |          |          |
| 1       | 1       | 1       |          |          |          |

Solusi:


| Input 3 | Input 2 | Input 1 | Output 3 | Output 2 | Output 1 |
|---------|---------|---------|----------|----------|----------|
| 0       | 0       | 0       | 1        | 0        | 0        |
| 0       | 0       | 1       | 1        | 0        | 1        |
| 0       | 1       | 0       | 1        | 0        | 1        |
| 0       | 1       | 1       | 1        | 0        | 1        |
| 1       | 0       | 0       | 1        | 1        | 0        |
| 1       | 0       | 1       | 0        | 1        | 1        |
| 1       | 1       | 0       | 1        | 1        | 1        |
| 1       | 1       | 1       | 0        | 1        | 1        |



## Permasalahan 3
Sebutkan jenis IC yang digunakan beserta jumlahnya! Bandingkan dengan jumlah IC yang dibutuhkan jika rangkaian dibuat berdasarkan persamaan boolean yang belum disederhanakan!

Solusi:

Sebelum Penyederhanaan:

O1 = B1 . !B2 + B2\
O2 = !B1 . B3 + B1 . B3\
O3 = !B1 + B2. !B3 + B1 . !B3\
O3 = (!B1 + B2. !B3) + (B1 . !B3)

Dari persamaan diatas dapat dilihat bahwa Lampu 1 (O1) akan memerlukan 3 gerbang logika, yaitu 1 OR, 1 AND, dan 1 NOT.

Dari Persamaan diatas dapat dilihat bahwa Lampu 2 (O2) akan memerlukan 4 gerbang logika, yaitu 1 OR, 2 AND, dan 1 NOT

Dari Persamaan diatas dapat dilihat bahwa Lampu (O3) akan memerlukan 7 gerbang logika, 2 OR, 2 AND, dan 3 NOT.

Maka, sebelum penyederhanaan, dibutuhkan 4 gerbang OR, 5 gerbang AND, dan 5 gerbang NOT.

Mengasumsikan IC yang digunakan adalah yang dari seri 74xx, maka diperlukan 1 IC7432, 2 IC7408, dan 1 IC 7404, dengan total 4 IC.

Setelah Penyederhanaan:

O1 = B1 + B2\
O2 = B3\
O3 = !B1 + !B3

Dari persamaan diatas dapat dilihat bahwa Lampu 1 (O1) akan memerlukan 1 gerbang logika, yaitu 1 OR.

Dari Persamaan diatas dapat dilihat bahwa Lampu 2 (O2) akan memerlukan 0 gerbang logika.

Dari Persamaan diatas dapat dilihat bahwa Lampu (O3) akan memerlukan 3 gerbang logika, 1 OR, dan 2 NOT.

Maka, setelah penyederhanaan, dibutuhkan 2 gerbang OR, 0 gerbang AND, dan 2 gerbang NOT.

Mengasumsikan IC yang digunakan adalah yang dari seri 74xx, maka diperlukan 1 IC7432, dan 1 IC 7404, dengan total 2 IC.



## Permasalahan 4
Berikan analisa terhadap percobaan yang telah dilakukan!

Solusi:

Analisa akan dilakukan sesuai dengan alur perakitannya.

1. Tegangan 5 Volt dihubungkan dengan _Power Strips_ terdalam, sementara Ground dihubungkan dengan _Power Strips_ terluar. Pada kasus ini, sumber dari Gnd dan Vcc adalah board _Arduino Uno_. Bagian ini berfungsi sebagai Voltage Driver utama dan Ground Utama dari rangkaian.
2. IC 7432 dan IC 7404 dipasang pada _divider_ board. Satu sisi chip akan terhubung dengan _Terminal Strips_ bawah, dan sisi lainnya akan terhubung dengan _Terminal Chips_ atas. Konstruksi seperti ini berfungsi untuk memberikan akses besar terhadap keseluruh 14 pin dari kedua IC tersebut.
3. Untuk setiap IC, sambungkan pin 7 dengan Gnd dan pin 14 dengan Vcc (5 V) tanpa resistansi apa apa. Sambungan ini berfungsi untuk menjalankan IC sehingga logika NOT dan OR dapat dijalankan. Sudah imperatif bahwa Vcc harus stabil di 5 V, apabila tegangan kelebihan dapat menyebabkan malfungsi, apabila tegangan kekurangan gerbang logika tidak akan berjalan.
4. Siapkan 3 Lampu Merah, Hijau dan Biru untuk mewakili O1, O2, dan O3. Sambungkan pin negatif ke Gnd, lalu gabungkan seri dengan resistor 1k ohm sehingga terhubung dengan _Terminal Strips_. Lampu ini akan menjadi indikator dari output rangkaian gerbang logika. **RESISTOR WAJIB DIGUNAKAN. SATU LAMPU LED 5mW 550NM TIDAK DAPAT MENANGANI WALAU HANYA 3 VOLT TEGANGAN**
5. Siapkan 3 kabel jumper, masing masing masukkan ke pin 8, 9, dan 10 dari arduino, masing masing berkorespondensi dengan Input 1, 2, dan 3. Kabel ini berfungsi sebagai Input 1, 2, dan 3. 
6. Ketiga kabel tersebut, hubungkan pada _Terminal Strips_ tanpa saling kontak. _Terminal Strips_ yang berkontak dengan ketiga kabel tersebut akan menjadi tempat percabangan/asal dimana setiap rangkaian boolean akan mengambil inputnya dari sini
7. Hubungkan Input 1 dan 2 dengan pin 1 dan 2 dari IC 7432. Sambungkan pin 3 dari IC 7432 dengan lampu O1.
8. Hubungkan Input 3 dengan lampu O2.
9. Hubungkan Input 1 dan 3 dengan pin 1 dan 3 dari IC 7404. Kemudian, hubungkan pin 2 dan 4 dari IC 7404 dengan pin 4 dan 5 dari IC 7432. Kemudian, hubungkan pin 6 dari IC 7432 dengan lampu O3.
10. Ketiga rangkaian diatas menyimulasikan operasi boolean yang telah disederhanakan pada Permasalahan 1.



## Permasalahan 5
Buatlah kesimpulan terhadap keseluruhan praktikum dalam bentuk poin-poin!  

Solusi:

1. Pada dasarnya, gerbang AND dapat disubstitusi apabila didapati gerbang NOT dan gerbang OR.
2. Sederhanakan logika/aljabar boolean. Penyederhanaan dapat mengurangi banyak gerbang logika dan IC yang diperlukan. Dalam konteks komersil, hal ini dapat mengurangi harga manufaktur chip dan harga operasionalnya.
3. Prinsip De Morgan dan Negasi Ganda adalah dua prinsip yang paling berguna saat menyederhanakan aljabar boolean.
4. Ada banyak IC pengganti untuk kebutuhan yang sama, dengan model yang berbeda dan manufakturer yang berbeda. Bacalah datasheet dari setiap komponen yang digunakan.



## Referensi
1. G. Boole,  _The Mathematical Analysis of Logic Being an Essay Towards a Calculus of Deductive Reasoning_. 2011. Available: https://www.gutenberg.org/ebooks/36884
2. “7432 Gate Datasheet pdf - OR Gate. Equivalent, Catalog,”  _datasheetspdf.com_. https://datasheetspdf.com/pdf/245534/FairchildSemiconductor/7432/1
3. “7408 datasheet,”  _datasheetspdf.com_. https://datasheetspdf.com/pdf-file/500074/Fairchild/7408/1

‌

‌

‌
