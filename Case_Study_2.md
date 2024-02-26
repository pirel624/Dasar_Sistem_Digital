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

