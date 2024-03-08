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

Solusi:






