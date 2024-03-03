# Tugas Pendahuluan Modul 3
#### Muhammad Pirel Jenar Lubdhaka
#### 2306226681
#### Teknik Elektro 2023

## Permasalahan 1
Jelaskan yang dimaksud dengan minterm dan maxterm! Adakah suatu hubungan antara minterm dan maxterm?

Solusi:
Minterm akan sebanyak n variabel adalah satu suku yang merupakan produk dari sebanyak n literal yang mengandung seluruh n variabel tersebut. Maxterm adalah jumalah/sum suku suku yang terdiri dari n literal dan n variabel tersebut.

![Minterm vs Maxterm](https://homework.study.com/cimages/multimages/16/22may-16766968686860606927.png)



## Permasalahan 2
Representasi fungsi boolean dapat dilakukan dalam bentuk standar yaitu Sum of Products dan Product of Sums, ataupun dengan bentuk kanonik (canonical) yaitu Sum of Minterms dan Product of Maxterms. Jelaskan masing-masing bentuk serta perbedaannya!

Solusi:

Pertama, akan dijelaskan perbedaan antara Sum of Products, Products of Sums, Sum of Minterm, dan Product of Maxterm.

Sum of Product adalah bentuk ekspresi aljabar boolean dimana produk dari literal (hasil dari operasi AND) saling dijumlahkan (hasil dari operasi OR).

Product of Sum adalah kebalikannya, dimana literal literal awalnya di ORkan terlebih dahulu, lalu hasilnya saling di ANDkan.

Berikut adalah contoh dari bentuk Sum of Product:
![Sum of Product](https://media.geeksforgeeks.org/wp-content/uploads/20230828155742/SOP-image.png)
Berikut adalah contoh dari bentuk Product of Sum:
![Product of Sum](https://www.electronics-lab.com/wp-content/uploads/2022/04/eq2.png)

Sum of Minterm pada dasarnya adalah sama dengan Sum of Products, hanya saja banyak literalnya tidak melebihi banyak variabel.

Product of Maxterm pada dasarnya adalah sama dengan Product of Sum, hanya saja banyak literalnya sama dengan banyak variabelnya.

Kedua bentuk tersebut pada dasarnya adalah penyederhanaan dari konsep Sum of Products dan Products of Sum. Bentuk sederhana ini paling sering digunakan sebagai tahap pertama dalam memetakan tabel kebenaran menjadi ekspresi boolean. Bentuk sederhana ini disebut juga sebagai **Bentuk Kanonik**.

![Bentuk Kanonik](https://media.geeksforgeeks.org/wp-content/uploads/11-3.jpg)

