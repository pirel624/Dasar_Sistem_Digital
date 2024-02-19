# Case Study Modul 1
#### Muhammad Pirel Jenar Lubdhaka
#### 2306226681
#### Teknik Elektro 2023

## Permasalahan 1
Screenshot hasil rangkaian yang telah dibuat dan berikan analisis terhadap cara kerja rangkaian yang telah dibuat! 

Solusi:
1.  Screenshot:
![Rangkaian_AndState](https://github.com/pirel624/Dasar_Sistem_Digital/blob/7c25670e59bd2f8524e3f741e29b17b08e595d9f/Rangkaian_AndState.png)
![Rangkaian_OrState](https://github.com/pirel624/Dasar_Sistem_Digital/blob/7c25670e59bd2f8524e3f741e29b17b08e595d9f/Rangkaian_OrState.png)
![Rangkaian_AndOrState](https://github.com/pirel624/Dasar_Sistem_Digital/blob/7c25670e59bd2f8524e3f741e29b17b08e595d9f/Rangkaian_AndOrState.png)
_Catatan: Kabel kuning terhubung dengan lampu merah, kabel hijau terhubung dengan lampu biru, dan kabel torqoise terhubung dengan lampu orange_
2. [Link Projek](https://www.tinkercad.com/things/1rwUEIEPUse-pirel-2306226681-cs1)
3. Analisis Cara Kerja:
Saya akan menjelaskan cara kerja ini sesuai dengan pola pikir saya saat saya merangkai sirkuit ini. Pertama, saya siapkan _power supply_ dengan tegangan 5 volt. Alasan dari 5 volt itu adalah karena IC AND dan IC OR memiliki nilai tegangan operasi nominal sebesar 5 volt. Berikutnya, saya sambungkan Gnd dan Vcc dari power supply ke _power strips_ breadboard. Saya juga menjembatani _power strips_ sebab _power strips_ terputus di bagian tengah. Seluruh baris _power strips_ dibagian bawah digunakan sebagai acuan tegangan 5 volt dan Ground. Berikutnya saya sambungkan pin _power_ dan _ground_ dari chip IC AND dan IC OR, terletak di pin 14 dan 7 secara berurutan. Kedua pin ini berkerja untuk mendayai komponen internal pada masing masing IC, mereka memerlukan daya untuk mensimulasikan operasi boolean (komponen aktif). Lalu saya pasang saklar 4 DIP di tengah, di antara kedua IC. Saklar ini berguna untuk mengatur 4 bit sinyal yang akan diolah oleh kedual IC. Berikutnya, saya menyambungkan keempat pin saklar 4 DIP ke Vcc pada _power strips_. Lalu pin output 1 dan 2 dari saklar dihubungkan ke pin 12 dan 13 dari IC 7408 (Quad AND). Kemudian pin 11 dihubungkan dengan resistor 1k ohm, yang mana resistor ini dihubungkan dengan lampu LED merah dan Gnd secara seri. Rangkaian ini menyimulasikan perintah (a) bahwa input 1 dan 2 harus dioperasikan dengan operator AND, dan outputnya diindikasikan dengan nyala lampu LED merah (Menyala = HIGH, Mati = LOW). Berikutnya, hal yang sama terjadi pada IC 7432 (Quad OR), yaitu pin 12 dan 13 dari IC 7432 dihubungkan dengan output 3 dan 4 dari saklar 4 DIP. Kemudian pin 11 dari IC 7432 dihubungkan dengan sebuah resistor 1k ohm, yang mana juga dihubungkan dengan lampu LED biru dan GND secara seri. Kegunaan dari resistor pada ketiga lampu adalah mengurangi tegangan yang akhirnya tiba pada lampu LED (lampu ini mudah terbakar, 2 volt tegangan operasi disarankan). Rangkaian ini menyimulasikan perintah (b) bahwa input 3 dan 4 harus dioperasikan dengan operator OR, dan outputnya diindikasikan dengan nyala lampu LED biru (Menyala = HIGH, Mati = LOW). Terakhir, pin output 3 dan 4 dari saklar 4 DIP dihubungkan dengan pin 9 dan 10 dari IC 7408 (Quad AND). Kemudian, pin output 1 dari saklar 4 DIP beserta pin 8 dari IC 7408 dihubungkan dengan pin 9 dan 10 dari IC 7432 (Quad OR). Lalu, pin 8 dari IC 7432 dihubungkan dengan resistor 1k ohm, yang mana resistor ini juga dihubungkan dengan lampu LED orange dan Ground secara seri. Rangkaian ini menyimulasikan perintah (c), dimana input 1, 2, dan 3 harus dioperasikan [(2 AND 3) OR 1] dengan keluarannya (dari pin 9 IC 7432) diindikasikan dengan nyala lampu LED orange (Menyala = HIGH, Mati = LOW).

## Permasalahan 2
Apa itu anode dan katode pada LED. Pada komponen fisik, bagaimana cara membedakan anode dan katode dari LED?

Solusi:
Anoda adalah pin positif dari LED, sedangkan katoda adalah pin negatif dari LED. Arus harus sesuai dengan polaritas pin, arus positif harus mengalir ke anoda terlebih dahulu, dan sebaliknya. Ini sangat penting karena LED merupakan dioda merupakan semikonduktor, yang berarti kedua sisinya berbeda dan memiliki perannya masing masing. Jika aturan ini tidak diikuti, maka LED berpotensi besar untuk malfungsi/terbakar.

Untuk membedakan mana pin positif dan mana pin negatif lihat panjang kaki pinnya. Pin yang panjang adalah pin positif, sementara pin yang pendek adalah pin negatif. Cara lainnya untuk menentukan, apabila pin terpotong, adalah dengan melihat strip konduktor yang ada di dalamnya. pin yang terhubung dengan strip yang lebih besar adalah pin negatif, dan pin yang terhubung dengan strip yang paling kecil adalah pin positif.

Gambar:

![Pin LED](https://www.electroduino.com/wp-content/uploads/2020/08/LED-or-Light-Emitting-Diode-Pinout.jpg)



## Permasalahan 3
Dari informasi pada datasheet tentang IC yang digunakan selama praktikum, gambarlah skema IC dan tunjukkan pin mana saja yang berupa output.

Solusi:

1. Gambar:
![Pinout_7408](https://netsonic.fi/en/wp-content/uploads/2021/07/9093138730d267e574c0a83debdc23c8.jpg)
![Pinout_7432](https://robotechshop.com/wp-content/uploads/2015/12/7432.jpg)
2. Pin Output:
Kedua IC tersebut memiliki kode pin yang sama. Pin yang dijadikan output adalah pin 3, 6, 8, dan 11.


## Permasalahan 4
Dari skema IC yang telah digambarkan, terdapat pin VCC dan Ground (GND). Apa input yang sesuai untuk VCC dan GND? Apa efek pada IC jika terjadi kesalahan dan input dipasangkan secara terbalik?

Solusi:
Pada kasus diatas, input yang sesuai untuk Vcc adalah +5 volt dan input yang sesuai untuk Gnd adalah 0 volt (kutub negatif). Jika terjadi kesalahan pada pemasangan, maka dapat terbakar (misalnya pada tegangan Vcc berlebihan (> 5.5 volt)), atau tidak berfungsi (tegangan Vcc < 4.5 volt).

Jika pemasangan terbalik, maka IC tidak akan bekerja, atau lebih buruk, dapat terbakar. Hal ini disebabkan komponen internal dari IC bersifat memiliki polaritas (transistor, dioda), dan juga karena rangakainnya sendiri sudah didesain dengan pin Vcc dan Gnd yang spesifik.



## Permasalahan 5
Bagaimana anda membedakan posisi dari pin IC pada IC fisik?

Solusi:
![DIP IC with notch](https://media.springernature.com/lw685/springer-static/image/chp%3A10.1007%2F978-3-319-66775-1_2/MediaObjects/394404_1_En_2_Fig18_HTML.png)

Untuk menentukan posisi pin dengan manufaktur _Dual In-Line_ (Seperti pada gambar diatas), ikuti prosedur berikut:

1. Cari takik pada badan IC
2. Arahkan takik ke atas/utara
3. Mulai dari sebelah kiri, pin pertama yang anda temukan adalah pin pertama (pin 1)
4. Lanjutkan ke pin-pin berikutnya, mengikuti arah berlawanan jarum jam
5. Konsultasikan nomor pin dengan datasheet
6. Selesai



## Permasalahan 6
Berikan kesimpulan dari praktikum dalam bentuk poin-poin

Solusi:

1. Untuk menyimulasikan gerbang AND, salah satu IC yang dapat digunakan adalah IC 7408
2. Untuk menyimulasikan gerbang OR, salah satu IC yang dapat digunakan adalah IC 7432
3. Untuk membedakan pin positif dari pin negatif pada LED kaki, lihan panjang pinnya. Pin yang panjang adalah pin positif, sementara pin yang pendek adalah pin negatif. Cara lainnya adalah dengan melihat strip konduktor yang ada di dalam tabung LED. Strip yang paling kecil terhubung dengan pin positif, strip yang paling besar terhubung dengan pin negatif.
4. IC 7408 dan IC 7432 memiliki 14 pin. Pin 7 dan 14 masing masing adalah pin ground dan Vcc. Sementara pada kedua IC tersebut, letak output dari gerbang logikanya adalah pada pin 3, 6, 8, dan 11.
5. Komponen aktif, seperti komponen semikonduktor (IC, LED, Dioda, dll) memiliki polaritas (arah kutub positif dan negatif). Arah tersebut wajib dipatuhi, jika tidak, malfungsi akan terjadi.
6. Untuk menentukan lokasi pin pada IC, lihat takik pada badan IC. Lalu, mulai dari pin pertama yang ada di sebelah kiri (itu pin 1), bergeraklah berlawanan arah jarum jam untuk menentukan berturut turut nomor pinnya. Jika sudah, konsultasikan nomor pin dengan dokumentasi pada datasheet.
