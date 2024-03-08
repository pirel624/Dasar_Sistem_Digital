# Tugas Tambahan 1
#### Muhammad Pirel Jenar Lubdhaka
#### 2306226681
#### Teknik Elektro 2023

Win memiliki sebuah ide baru. Ia ingin membuat sebuah rangkaian digital yang dapat memeriksa apakah nilai yang dimasukkan sebagai input merupakan bilangan ganjil atau genap. Berikut adalah ketentuan dari rangkaian tersebut:

Rangkaian terdiri dari 4 input switch yaitu:
- E (Even) 🡪 Switch ini digunakan untuk memeriksa apakah input merupakan bilangan genap 
- O (Odd) 🡪 Switch ini digunakan untuk memeriksa apakah input merupakan bilangan ganjil 
- I0 (Input 0) 🡪 Switch ini digunakan untuk merepresentasikan nilai MSB dari input 2-bit 
- I1 (Input 1) 🡪 Switch ini digunakan untuk merepresentasikan nilai LSB dari inpujt 2-bit

Rangkaian memiliki output berupa LED, yaitu: 
- C 🡪 LED yang akan memeriksa apakah input yang dimasukkan pada I1 dan I0 merupakan bilangan genap/ganjil (sesuai dengan switch E/O yang bernilai HIGH)

Jika switch input E dan O keduanya bernilai sama, maka LED akan mati



## Permasalahan 1
Lengkapi tabel kebenaran (truth table) berikut sesuai logika yang terdapat pada ketentuan soal di atas!

Solusi:

| E | O | I0 | I1 | C |
|---|---|----|----|---|
| 0 | 0 | 0  | 0  | 0 |
| 0 | 0 | 0  | 1  | 0 |
| 0 | 0 | 1  | 0  | 0 |
| 0 | 0 | 1  | 1  | 0 |
| 0 | 1 | 0  | 0  | 0 |
| 0 | 1 | 0  | 1  | 1 |
| 0 | 1 | 1  | 0  | 0 |
| 0 | 1 | 1  | 1  | 1 |
| 1 | 0 | 0  | 0  | 1 |
| 1 | 0 | 0  | 1  | 0 |
| 1 | 0 | 1  | 0  | 1 |
| 1 | 0 | 1  | 1  | 0 |
| 1 | 1 | 0  | 0  | 0 |
| 1 | 1 | 0  | 1  | 0 |
| 1 | 1 | 1  | 0  | 0 |
| 1 | 1 | 1  | 1  | 0 |



## Permasalahan 2
Buatlah K-map untuk menentukan persamaan dari output sesuai dengan truth table di atas! Tuliskan persamaan yang didapatkan! 

Solusi:

Berikut adalah K-Map yang didapatkan:


| ##### | I0I1  | 00    | 01    | 11    | 10    |
|-------|-------|-------|-------|-------|-------|
| EO    | ##### | ##### | ##### | ##### | ##### |
| 00    | ##### | 0     | 0     | 0     | 0     |
| 01    | ##### | 0     | 1     | 1     | 0     |
| 11    | ##### | 0     | 0     | 0     | 0     |
| 10    | ##### | 1     | 0     | 0     | 1     |

\
\
Berikut adalah pengelompokkan Implicant dari K-Mapnya:

| ##### | I0I1  | 00    | 01    | 11    | 10    |
|-------|-------|-------|-------|-------|-------|
| EO    | ##### | ##### | ##### | ##### | ##### |
| 00    | ##### | 0     | 0     | 0     | 0     |
| 01    | ##### | 0     | 1 @   | 1 @   | 0     |
| 11    | ##### | 0     | 0     | 0     | 0     |
| 10    | ##### | 1 %   | 0     | 0     | 1 %   |

\
\
Kelompok @:

1. E tidak mengalami perubahan nilai, dengan nilai 0. E'.
2. O tidak mengalami perubahan nilai, dengan nilai 1. O.
3. I0 mengalami perubahan nilai, abaikan.
4. I1 tidak mengalami perubahan nilai, dengan nilai 1. I1.
5. Term yang didapatkan = E'OI1

Kelompok %:

1. E tidak mengalami perubahan nilai, dengan nilai 1. E.
2. O tidak mengalami perubahan nilai, dengan nilai 0. O'.
3. I0 mengalami perubahan nilai, abaikan.
4. I1 tidak mengalami perubahan nilai, dengan nilai 0. I1'.
5. Term yang didapatkan = EO'I1'

Persamaan akhir:

```
F = E'OI1 + EO'I1'
```



## Permasalahan 3
Buatlah rangkaian berdasarkan persamaan yang diperoleh melalui K-map! Sertakan foto rangkaian dan link Tinkercad!

Solusi:

Berikut adalah gambar dari rangkaian yang telah dibuat:

![Raw](https://github.com/pirel624/Dasar_Sistem_Digital/blob/22d6989b5cd0ed1a96b5cac05f1af19d84e88f91/TugasTambahan1RawCircuit.png)

\

![Diagram](https://github.com/pirel624/Dasar_Sistem_Digital/blob/22d6989b5cd0ed1a96b5cac05f1af19d84e88f91/TugasTambahan1DiagramCircuit.png)

Berikut adalah link dari project TinkerCad tersebut:

[TinkerCad Pirel](https://www.tinkercad.com/things/3SM00f29YXs-tt1-pirel-2306226681)



## Permasalahan 4
Apakah bentuk persamaan yang diperoleh merupakan Product of Sum atau Sum of Product? Bila merupakan SOP, maka ubahlah menjadi POS, begitu juga sebaliknya!

Solusi:
Ya, bentuk persamaan yang dihasilkan oleh K-Map pada permasalahan 2 adalah Sum of Products.

Berikut adalah versi Product of Sums nya:

```
F = E'OI1 + EO'I1'
F' = (E'OI1 + EO'I1')'
F' = (E + O' + I1')(E' + O + I1)




F = [ (E + O' + I1')(E' + O + I1) ]'
```



## Permasalahan 5
Berikan analisis terhadap rangkaian yang telah dibuat, serta berikan kesimpulan dalam bentuk poin-poin!

Solusi:

Analisis akan diberikan sesuai dengan "alur" dari input logika.

Power Supply yang digunakan memiliki tegangan independen ideal sebesar 5 volt, dan arus independen ideal 1500 mA.

Gerbang logika OR, AND, dan NOT disimulasikan dengan IC 7432, IC 7408, dan IC 7404 secara berurutan. Setiap pin diletakkan ditengah breadboard agar keempat belas pin dapat diakses dengan mudah. Pin 14 adalah Vcc dari IC tersebut, sementara pin 7 adalah Gnd IC tersebut. Vcc dihubungkan dengan tegangan independen ideal 5 volt. Gnd dihubungkan dengan kutub negatif / Ground dari Power Supply.

Input dimulai dari saklar DIP 4x. Pin 1, 2, 3, 4, masing masing berkorespondensi dengan E, O, I0, I1 secara berturut turut.

Pin 1 saklar terhubung dengan pin 13 dari IC 7404. Pin 12 dari IC 7404 terhubung dengan pin 13 dari IC 7408. Pin 2 saklar terhubung dengan pin 12 dari IC 7408. Pin 11 dan 10 dari IC 7408 saling digabungkan. Pin 4 saklar dihubungkan dengan pin 9 dari IC 7408.  Rangkain ini merepresentasikan operasi E'OI1. Pin 8 dari IC 7408 adalah keluaran dari operasi ini.

Pin 2 saklar terhubung dengan pin 3 dari IC 7404. Pin 4 dari IC 7404 terhubung dengan pin 2 dari IC 7408. Pin 1 saklar terhubung dengan pin 1 dari IC 7408. Pin 3 dan 4 IC 7408 saling terhubung. Pin 4 saklar terhubung dengan pin 5 dari IC 7404. Pin 6 IC 7404 terhubung dengan pin 5 dari IC 7408.  Rangkain ini merepresentasikan operasi E'OI1. pin 11 dari IC 7408 adalah keluaran dari operasi ini. Pin 6 dari IC 7408 adalah keluaran dari operasi ini.

Pin 6 IC 7408 terhubung dengan pin 1 dari IC 7433. Pin 8 dari IC 7408 terhubung dengan pin 1 dari IC 7432. Rangkaian ini merepresentasikan operasi E'OI1 + EO'I1'. Keluaran dari operasi ini ada pada pin 3 dari IC 7432.

Pin 3 IC 7432 kemudia dihubungkan dengan lampu LED merah, yang kemudian dihubungkan dengan Ground dengan perantara resistor 1000 Ohms. LED bertindak sebagai indikator nilai keluaran (Menyala = HIGH, Mati = LOW). Resistor berguna untuk membagi tegangan 5 volt, sehingga LED menerima tegangan yang tidak berlebihan.

Kesimpulan:

1. Untuk setiap deskripsi sistem logika boolean, buatlah Truth Tablenya untuk mendapatkan definisi matematis yang lebih tepat atas sistem tersebut.
2. Gunakan K-Map untuk mendapatkan ekspresi aljabar boolean yang sederhana atas Truth Table tersebut.
3. Lakukan tes bug pada setiap tahap perangkaian sirkuit.
4. Prinsip De Morgan dapat digunakan untuk mengubah bentuk POS ke SOP, begitu juga sebaliknya.






