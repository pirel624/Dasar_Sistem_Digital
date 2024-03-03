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



## Permasalahan 3
Jelaskan apa yang dimaksud dengan K-Map beserta kegunaannya!

Solusi:

K-Map atau Karnaugh Map adalah metode yang dikembangkan untuk menyederhanakan ekspresi boolean yang berbentuk kanonik. 

Inti dari Karnaugh Map adalah bahwa dalam bentuk kanonik dari suatu ekspresi boolean, setiap sukunya saling memiliki kesamaan logika/_redundancy_, secara efek memungkinkan beberapa _term_ dari ekspresi tesebut untuk direpresentasikan dengan satu _term_saja. Karnaugh Map disini berguna sebagai alat untuk memproseduralkan perubahan representasi tersebut.

Cara kerja Karnaugh Map adalah dengan memetakan output tiap term dari ekspresi yang berbentuk kanonik tersebut pada tabel yang baris dan kolomnya berkorespondensi dengan digit index dari term tersebut. Kemudian, input-input ini dikelompokkan, lalu dibuatkan satu term yang mewakili logikanya, sesuai dengan kriteria-kriteria Kernaugh Map. Salu, seluruh term tersebut dijumlahkan, lalu disederhanakan dengan prinsip dasar aljabar boolean (De Morhan, dll).

Berikut adalah prosedur penggunaak Kernaugh Map:

1. Konversikan persamaan Boolean yang diketahui ke dalam bentuk persamaan SOP-nya (Sum of Product). Gunakan Tabel Kebenaran sebagai alat bantu. 
2. Gambarlah K-map, dengan jumlah sel jumlah variabel input.
3. Isi sel K-map sesuai dengan minterm pada Tabel Kebenaran . 
4. Cover minterm-minterm bernilai 1 yang berdekatan, dengan aturan : - hanya minterm berdekatan secara vertikal atau horizontal yang boleh di-cover. - Jumlah minterm berdekatan yang boleh di-cover adalah : 2. 4, 8, 16, 32 
5. Buat persamaan SOP baru sesuai dengan hasil peng-cover-an minterm.

Kernaugh Map:
![Kernaugh Map](https://upload.wikimedia.org/wikipedia/commons/thumb/0/02/K-map_6%2C8%2C9%2C10%2C11%2C12%2C13%2C14_anti-race.svg/1200px-K-map_6%2C8%2C9%2C10%2C11%2C12%2C13%2C14_anti-race.svg.png)

Kegunaan dari Kernaugh Map adalah untuk mengoptimisasi ekspresi logika yang perlu digunakan untuk mewakili suatu tabel kebenaran. Sering kali tabel kebenaran memiliki _redundancy_, dimana tiap entrynya tidak jauh beda dengan entry lainnya, dan beberapa entry dapat disederhankan. Optimisasi sangat penting untuk meningkatkan performa dari divais dan mengurangi harga manufaktur dan operasinya.



## Permasalahan 4


