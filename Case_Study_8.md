# Case Study 8 DSD
#### Muhammad Pirel Jenar Lubdhaka
#### 2306226681
#### Teknik Elektro 2023



## Permasalahan 1
Input: Memasukkan Foto button input (Hanya button dan pengkabelannya saja). Jelaskan cara kerja pull down dan pull up button.

Solusi:

Gambar Rangkaian:
![T Flip Flop, Physical](https://github.com/pirel624/Dasar_Sistem_Digital/blob/8d925305bcb44099b39a27421d1df82dd9688682/XOR%20Aided%2C%20Toggleified%20Flip%20Flop.jpg)

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
