# Tugas Tambahan 2 DSD
#### Muhammad Pirel Jenar Lubdhaka
#### 2306226681
#### Teknik Elektro 2023



## Permasalahan 1
Berdasarkan yang sudah kalian pelajari selama ini, apa peran dari menggunakan gerbang logika kompleks dan universal? Mengapa hal tersebut dapat membantu kita dalam merangkai rangkaian digital?

Solusi:
Gerbang logika, baik yang universal maupun yang kompleks, mewakili operasi logika biner dasar. Mengingat bahwa tujuan dari pelajaran ini adalah untuk memahami setiap lapisan abstraksi yang ada pada instrumen komputasi digital, dan bahwa setiap lapisan abstraksi tersebut secara fundamental berdiri dari beberapa operasi _binary_ dasar saja, gerbang gerbang logika yang ada berguna sebagai implementasi fisik dari operasi operasi tersebut. Gerbang tersebut, baik secara virtual (misalnya dalam aplikasi Proteus), maupun fisik (dalam bentuk DIP IC), memberikan kami, mahasiswa, kemampuan untuk bereksperimen dengan logika biner secara langsung (tidak dengan formulasi matematis, di kertas hvs A4).

Selain itu, gerbang logika tersebut mempermudah kita melakukan eksperimen laboratorium. Mengingat bahwa asalnya operasi logika elektronik adalah transistor (Vacuum Tube pun bisa), dan memang dasarnya adalah transistor, adalah kemudahan bagi mahasiswa bahwa kami tidak perlu merancang rangkain transistor dan resistor.



## Permasalahan 2
Apa saja contoh penggunaan dalam kehidupan sehari hari untuk Encoder, Decoder, Multiplexer, dan Demultiplexer?

Solusi:
Salah satu kegunaan Encoder adalah pada Keyboard komputer. Pada keyboard, terdapat puluhan _keys_ dan setiap keys berkorespondensi satu-satu dengan suatu pin input Encoder. Encoder ini kemudian akan mengubah bacaan _keys_ menjadi data serial dengan _bus length_ yang lebih kecil sehingga dapat ditransfer melalui protokol standar, seperti USB atau PS/2.

Kegunaan lain encoder adalah pada _pads_ _dance floor_, yang biasa kita temui di tempat bermain di mall. _Pads_ tersebut berkorespondensi dengan _state_ tertentu, dengan pin input tertentu. Encoder berfungsi untuk mengubah bacaan tersebut menjadi data serial yang dapat lebih mudah dikirim ke CPU dari console permainan tersebut.

Decoder, karena kemiripannya, juga digunakan pada alat yang mirip, seperti router jaringan. Data internet yang masuk ke router, masuk sebagai data dari satu channel saja, walau tujuan akhir data tersebut adalah gawai yang berbeda beda. Pada setiap _packet_ data internet, akan disertai _metadata_ seperti IP, yang akan digunakan untuk "membelokkan" data ke gawai yang benar. Instrumen utama pembelokan ini adalah decoder.

Kegunaan utama Multiplexer adalah pada sistem memori, seperti RAM, EEPROM, dll. Sistem memori pada dasarnya adalah kumpulan "kontainer", setiap kontainer menyimpan "state", "data". Data ini bisa berukuran berapa saja (secara standar, setiap kontainer yang memiliki address unik menyimpan 8 bit/ 1 byte data, 256 permutasi _state_). Kontainer ini masing masing memiliki alamat, yang dinyatakan secara numerik. Ada beberapa cara untuk mengakses data dari setiap kontainer, satu per satu, tanpa tabrakan. Cara paling mudah adalah dengan menghubungkan setiap _state_ dengan satu pin data. Tetapi akibat dari keputusan ini adalah, diperlukan ribuan, jutaan, bahkan miliaran "kabel" untuk menghubungkannya dengan sistem pengolah, CPU. Cara kedua adalah dengan menggunakan multiplexer. Kita bisa menyuplai multiplexer dengan address dari kontainer yang ingin kita baca, dan multiplexer akan menolak segala data kecuali data dari kontainer tersebut. Akibatnya, arsitektur komputer dapat jauh lebih sederhana.

Kegunaan Demultiplexer adalah kebalikannya. Apabila kita memiliki data serial yang ingin mengaktifkan ribuan, jutaan aktuator, seperti led pada layar komputer, maka demultiplexer adalah alat yang digunakan. Misal, pada kasus grafik dan tampilan, saat GPU telah selesai mengolah data _vertex_, _lightmap_, _texture mapping_, _normal mapping_, dan sebagainya, yang dihasilkan adalah data _RGB_ untuk setiap pixel pada layar. Tentu, data ini dikirim ke layar melalui kabel VGA/HDMI sebagai satu kesatuan data. Tetapi saat tiba di layar, demux dan segala firmwarenya akan mengubah data mentah tersebut menjadi input untuk matrix pixel layar, mana yang menyala, mana yang mati, intensitas RGB, dll.



## Permasalahan 3
![school](https://static.wikia.nocookie.net/youkoso-jitsuryoku-shijou-shugi-no-kyoushitsu-e/images/1/10/School_Landscape.jpg/revision/latest/scale-to-width-down/1200?cb=20170818020625)

  

Selamat! Anda sudah diterima di Digilab Metropolitan Advanced Nurturing High School. Di sekolah ini, terdapat 4 kelas yang masing-masing kelasnya memiliki 10 siswa. Setiap kelas memiliki 1 guru yang mengajar. Guru tersebut akan memberikan tugas kepada murid-muridnya. Tugas yang diberikan oleh guru tersebut adalah membuat rangkaian digital, yaitu membuat sebuah *priority encoder* yang dapat menerima 16 input dan mengeluarkan 4 output. Setiap kelas akan diberikan tugas yang sama.

  

Seperti yang anda ketahui, *priority encoder* adalah rangkaian yang dapat menerima input data dari beberapa sumber dan mengeluarkan kode biner yang sesuai dengan input yang memiliki prioritas tertinggi. Dan *priority encoder* yang beredar di toko komponen elektronik hanya mampu menerima 8 input dan mengeluarkan 3 output.

Karena keterbatasan tersebut, sehingga tugas ini semakin menantang. Namun, anda sebagai siswa yang cerdas dan kreatif, ingin membuat rangkaian *priority encoder* yang mampu menerima 16 input dan mengeluarkan 4 output. Buatlah rangkaian *priority encoder* tersebut!

Solusi:

Gambar Rangkaian:
![Gambar Encoder](https://github.com/pirel624/Dasar_Sistem_Digital/blob/caf7b03cbd869acec2428d616c2de43a05d264f2/16%20Bit%20Priority%20Encoder.jpg)

File Rangkaian:
[File Encoder](https://github.com/pirel624/Dasar_Sistem_Digital/blob/caf7b03cbd869acec2428d616c2de43a05d264f2/16%20Bit%20Priority%20Encoder.pdsclip)

_
