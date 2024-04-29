# Case Study 8 DSD
#### Muhammad Pirel Jenar Lubdhaka
#### 2306226681
#### Teknik Elektro 2023



## Permasalahan 1
Input: Memasukkan Foto button input (Hanya button dan pengkabelannya saja). Jelaskan cara kerja pull down dan pull up button.

Solusi:

Gambar Rangkaian:
![T Flip Flop, Physical](https://github.com/pirel624/Dasar_Sistem_Digital/blob/8d925305bcb44099b39a27421d1df82dd9688682/XOR%20Aided%2C%20Toggleified%20Flip%20Flop.jpg)

![Pull Down Button, Physical](https://github.com/pirel624/Dasar_Sistem_Digital/blob/98fd0ec6af827d7ee817bb2ceb0c796d6b690019/Pull%20Down%20Button.jpg)

Video Penjelasan Rangkaian:
[T Flip Flop, Physical, Video Explanation](https://github.com/pirel624/Dasar_Sistem_Digital/blob/8d925305bcb44099b39a27421d1df82dd9688682/XOR%20Aided%2C%20Toggleified%20Flip%20Flop%2C%20Video%20Explanation.mp4)

Penjelasan Peran Pull Up/ Pull Down Button:

Pull Up/ Pull Down Button adalah rangkaian button, resistor, Vcc, Gnd, dan beban. Idenya disini adalah bahwa kebanyakan rangkaian digital sangatlah sensitif terhadap arus yang tinggi, bahkan sebagian akan rusak atau terbakar. Apabila Vcc 5V+ langsung dihubungkan dengan button, lalu dihubungkan dengan input digital, misalnya pada IC 7474, maka komponen internal dari IC tersebut akan rusak.

Pada rangkaian Pull Button, akan ada resistor yang juga dihubungkan dengan button. 

Pada rangkaian Pull Up Button, Resistor dihubungkan seri dengan beban, atau dalam kasus ini IC digital. Tujuan dari resistor ini adalah untuk membatasi arus yang masuk ke IC tersebut. Cara kerja pembatasan ini dapat dijelaskan dengan hukum Ohm. Resistansi tambahan akan menghasilkan arus yang lebih kecil untuk tegangan yang sama.

Pada rangkaian Pull Down Button, Resistor dihubungkan dengan secara paralel dengan beban IC digital. Tujuan dari resistor ini adalah untuk mengatur arus yang mengalir ke IC. Cara kerja rangkaian ini adalah dengan menggunakan prinsip current divider, resistor "pull down" ini akan menentukan seberapa besar arus yang di "buang" ke ground, dan seberapa besar yang akan mengalir ke beban. Keuntungan dari rangkaian ini adalah beban akan selalu dialiri tegangan yang sama dengan yang ada pada VCC.

Pada kasus spesifik DSD 8 ini, rangakaian Pull Down digunakan sebagai input ke flip flop, tanpa perlu mengkhawatirkan resiko terbakar.

Sekian.



## Permasalahan 2
Jelaskan mengapa Ini merupakan rangkaian sekuensial.

Solusi:

Rangkain ini merupakan rangkaian sekuensial karena untuk setiap pin input dan output dari rangkaian digital, dalam kasus ini, T Flip Flop, memiliki korelasi variabel yang lebih dari satu jika dijabarkan dalam bentuk Truth Table atua persamaan aljabar boolean.

Sebagai contoh:
![T FF Truth Table, Javatpoint](https://static.javatpoint.com/tutorial/digital-electronics/images/t-flip-flop5.png)

Q dan Q', baik pada _State_ _Previous_ maupun _Next_ memiliki korelasi pin fisik yang sama. Yang membuat mereka dapat dilihat sebagai dua variabel boolean yang berbeda adalah bahwa pin tersebut ada di "dua ruang temporal yang berbeda".

Singkatnya, pada rangkaian sekuensial, konsep waktu dan urutan memengaruhi operasi, dimana _State_ dari periode sebelumnya akan dilempar kembali pada periode sekarang menjadi input yang baru.

Dan rangkain ini dapat disebut rangkaian sekuensial karena _State_ sebelumnya memengaruhu _State_ setelahnya. T Flip Flop.



## Permasalahan 3
Jelaskan mengapa T Flip-Flop Bisa toggle, dan apa perbedaan menggunakan T Flip-Flop dibanding flip-flop lain.

Solusi:

Mari kita lihat rangkaian di bawah ini:
![All About Electronics, Toggle Flip Flop](https://www.allaboutcircuits.com/uploads/articles/Figure_11_FFC4(1).jpg)

Pada T Flip Flop, ada operasi Exclusive Or yang dilakukan pada input T dan Output Q. Untuk menjelaskan lebih mudah, saya akan narasikan cara kerja T Flip Flop, saat Clock aktif.

1. SAAT TOGGLE MATI, T = 0.
2. Q1 = 0, T1 = 0.
3. XOR(Q1, T1) = 0 = D1.
4. D1 = 0.
5. Q2 = 0.
6. Q2 = 0, T2 = 0. ad infinitum.
7. SAAT TOGGLE NYALA, T = 0.
8. Q3 = 0, T3 = 1.
9. XOR(Q3, T3) = 1 = D3.
10. D3 = 1 = Q4.
11. Q4 = 1.
12. Q4 = 1, T4 = 1.
13. XOR(Q4, T4) = 0 = D4.
14. D4 = 0 = Q5.
15. Q5 = 0.
16. Q5 = 0, T5 = 1. ad infinitum.

Seperti yang dapat dilihat pada runtutan operasi di atas, gerbang XOR memungkinkan adanya perilaku "_Toggling_" untuk setiap transisi dari satu periode ke periode berikutnya, atau saat clock mengirim impulse ACTIVE nya.

Perbedaan T Flip Flop dengan flip flop lain adalah perilaku "_Toggling_" tersebut. Pada flip flop biasa, output state Q akan mengikuti input state T, mengabaikan keadaan Q pada periode sebelumnya.



## Permasalahan 4
Berikanlah analisis terhadap rangkaian yang dibuat. Sertakan foto rangkaian fisik yang telah dibuat!

Solusi:

Gambar Rangkaian:
![T Flip Flop, Physical](https://github.com/pirel624/Dasar_Sistem_Digital/blob/8d925305bcb44099b39a27421d1df82dd9688682/XOR%20Aided%2C%20Toggleified%20Flip%20Flop.jpg)

Video Penjelasan Rangkaian:
[T Flip Flop, Physical, Video Explanation](https://github.com/pirel624/Dasar_Sistem_Digital/blob/8d925305bcb44099b39a27421d1df82dd9688682/XOR%20Aided%2C%20Toggleified%20Flip%20Flop%2C%20Video%20Explanation.mp4)

Mengingat prinsip operasi dari Toggle Flip Flop telah dijelaskan pada Permasalahan 3, saya hanya akan menjelaskan wiring yang kami lakukan.

Pertama, karena kami tidak memiliki akses terhadap IC XOR, kami memutuskan bahwa satu gerbang XOR dapat dibuat dari 4 gerbang NAND, dan kebetulan, satu IC 7400 memiliki 4 gerbang NAND. Jadi, kami rerangkai pin pin IC 7400 sehingga dapat menyimulasikan satu gerbang XOR.

Berikut adalah skema yang kami jadikan acuan untuk melakukan konversi ini:
![XOR from NAND](data:image/png;base64,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)

Berikutnya, untuk menyimulasikan J Flip Flop, kami menggunakan IC 7474. IC ini kemudian kami rangkai dengan gerbang XOR yang telah kami buat, sesuai dengan skema di bawah ini:
![All About Electronics, Toggle Flip Flop](https://www.allaboutcircuits.com/uploads/articles/Figure_11_FFC4(1).jpg)

Untuk menyimulasikan Clock, kami menggunakan _Integrated Clock_ yang terdapat pada papan Vulcan 1, dan untuk menyimulasikan _Toggle_, kami menggunakan _Switch Built In_ yang ada pada papan tersebut. Untuk menampilkan _State_ Q dari T Flip Flop Kami, kami sambungkan pin 3 (pin Q dari IC 7474) dengan slot _Logic Probe_ yang ada pada Vulcan 1.

Secara keseluruhan, rangkaian yang kami buat berjalan dengan sempurna.



## Permasalahan 5
Soal 2: Masukkan truth table dari Soal 2 dan Berikan Analisis apakah hasil akhir sama dengan Soal 1.

Solusi:

| LOCKDOWN | TOGGLE | CLOCK | OUTPUT Q | INVERTED Q |
|---|---|---|----|----|
| 0 | 0 | 0 | 0  | 0  |
| 0 | 0 | 1 | 1  | 1  |
| 0 | 1 | 0 | 0  | 0  |
| 0 | 1 | 1 | 1  | 1  |
| 1 | 0 | 0 | 0  | 0  |
| 1 | 0 | 1 | 0  | 1  |
| 1 | 1 | 0 | 1  | 1  |
| 1 | 1 | 1 | 1  | 0  |

Iya, hasil akhir sama dengan yang pada nomor 1, diasumsikan _Output Q_ di lempar kembali ke _LOCKDOWN_



## Permasalahan 6
Berikan kesimpulan dari praktikum dalam bentuk poin-poin!

Solusi:

1. Flip Flop dari satu jenis dapat diubah menjadi jenis lainnya dengan bantuan gerbang logika universal yang disambungkan secara eksternal.
2. J Flip Flop dapat diubah menjadi T Flip Flop dengan bantuan satu (1= one) gerbang
3. Prinsip Pull Up/Pull Down resistor sangat berguna apabila bertanganan dengan komponen daya/arus rendah, seperti IC digital dan lampu LED.
4. Sistem Sekuensial dapat diartikan sebagai sistem yang dapat menerka keadaan sistem tersebut pada periode sebelumnya, dan dapat menggunakan bacaan tersebut untuk menghasilkan output yang baru.
5. Sekuensialitas juga dapat dilihat diartikan sebagai keadaan pada rangkaian digital dimana perbedaan waktu/periode dapat menghasilkan 2 atau lebih korelasi variabel boolean dari satu pin rangkaian.
6. Prinsip utama yang memungkinkan adanya T Flip Flop adalah perilaku "_Toggling_" yang dimungkinkan oleh gerbang _Exclusive Or_.
7. Clock dapat disimulasikan dengan IC 555 dalam konfigurasi _Monostable_.





