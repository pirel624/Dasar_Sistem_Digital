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
