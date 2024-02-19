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
Saya akan menjelaskan cara kerja ini sesuai dengan pola pikir saya saat saya merangkai sirkuit ini. Pertama, saya siapkan _power supply_ dengan tegangan 5 volt. Alasan dari 5 volt itu adalah karena IC AND dan IC OR memiliki nilai tegangan operasi nominal sebesar 5 volt. Berikutnya, saya sambungkan Gnd dan Vcc dari power supply ke _power strips_ breadboard. Saya juga menjembatani _power strips_ sebab _power strips_ terputus di bagian tengah. Seluruh baris _power strips_ dibagian bawah digunakan sebagai acuan tegangan 5 volt dan Ground. Berikutnya saya sambungkan pin _power_ dan _ground_ dari chip IC AND dan IC OR, terletak di pin 14 dan 7 secara berurutan. Kedua pin ini berkerja untuk mendayai komponen internal pada masing masing IC, mereka memerlukan daya untuk mensimulasikan operasi boolean (komponen aktif). Lalu saya pasang saklar 4 DIP di tengah, di antara kedua IC. Saklar ini berguna untuk mengatur 4 bit sinyal yang akan diolah oleh kedual IC. Berikutnya, saya menyambungkan keempat pin saklar 4 DIP ke Vcc pada _power strips_. Lalu pin output 1 dan 2 dari saklar dihubungkan ke pin 12 dan 13 dari IC 7408 (Quad AND). Kemudian pin 11 dihubungkan dengan resistor 1k ohm, yang mana resistor ini dihubungkan dengan lampu LED merah dan Gnd secara seri. Rangkaian ini menyimulasikan perintah bahwa input 1 dan 2 dioperasikan dengan operator AND, dan outputnya diindikasikan dengan nyala lampu LED merah (Menyala = HIGH, Mati = LOW). 
