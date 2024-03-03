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
Jelaskan yang dimaksud dengan prime implicants dan essential prime implicants, serta jelaskan perbedaannya!

Solusi:
Untuk menjelaskan prime implicant, kita akan kembali kepada Kernaugh Map.

Masukan awal dari Kernaugh Map adalah ekspresi aljabar linear berbentuk kanonik. Setelah diterapkan Kernaugh Map, maka ekspresi tersebut tersederhanakan menjadi bentuk yang paling sederhana dari ekspresi tersebut. Ekspresi yang sederhana ini berbentu Sum of Products, dimana ada beberapa suku yang saling di ORkan, dimana tiap suku merupakan operasi AND dari beberapa variabel.

Suku suku tersebut adalah _Prime Implicant_, dikatakan seperti itu karena bentuknya yang paling dasar dan unik. Setiap _Prime Implicant_ merupakan hasil penyederhanaan dari beberapa suku pada bentuk kanonik. Apabila _Implicant_ hanya berupa hasil penyederhanaan dari satu suku dari bentuk kanonik, maka _Implicant_ tersebut dikatakan sebagai _Essential Prime Implicant_.

![Implicant From K-Map](https://cdn1.byjus.com/wp-content/uploads/2022/05/word-image263.png)



## Permasalahan 5
Jelaskan cara menyederhanakan persamaan 3 dan 4 variable menggunakan K-Map!

Solusi:

Pertama, ubah persamaan tersebut menjadi bentuk Sum of Products.

Lalu, sederhanakan menjadi bentuk Sum of Minterm.

Kemudian, indexkan bentuk SoM tersebut.
Setiap suku dari bentuk SoM akan mengeluarkan nilai TRUE apabila variabel inputnya bernilai tertentu, yang apabila dideretkan menjadi sederet digit biner, akan menghasilkan satu nilai, satu index. Setiap suku memiliki indexnya masing-masing. Oleh sebab itu, ekspresi tersebut dapat diwakilkan dengan index indexnya saja

![Indexed Canonical Form](https://www.electronicshub.org/wp-content/uploads/2015/08/Table-for-2n-min-terms-and-amx-terms.jpg)

Jika sudah, catat index mana saja yang digunakan untuk merepresentasikan bentuk kanonik tersebut. Catatlah, nanti akan digunakan saat pemetaan K-Map

Lalu siapkan Kernaugh Mapnya. 
Untuk 3 Variabel, 2 variabel paling insignifikan akan mewakili kolomnya. Sedangkan Variabel paling signifikan akan mewakili barisnya. Atur letak digit-digit dari variabel tersebut sesuai dengan prinsip Gray Code, agar setiap iterasi dari kolom atau baris hanya akan menghasilkan satu perubahan digit saja.

Untuk 4 variabel, langkahnya mirip. 2 variabel paling insignifikan akan mewakili kolomnya, sedangkan 2 variabel paling signifikan akan mewakili barisnya.

Berikut adalag K-Map untuk 4 variabel ABCD:

![4 Var K-Map Construction](https://upload.wikimedia.org/wikipedia/commons/thumb/1/1a/K-map_minterms_A.svg/1280px-K-map_minterms_A.svg.png)

Apabila K-Map sudah dibuat, saatnya mengisi tiap sel.

Untuk setiap sel, tentukan nilai variabel yang berkorespondensi, lalu tentukan indexnya. Untuk referensi, lihat gambar di atas. Jika sudah, acu lah persamaan bentuk index yang telah dibuat. Apabila index pada sel ini ada pada persamaan tersebut, maka isi 1, jika tidak ada isi 0.

Lakukan untuk semua sel.

Jika sudah, grupkan sel-sel yang bernilai 1, dengan syarat:

1. Grup berbentuk persegi/persegi panjang.
2. Grup memiliki luas 1 sel, 2 sel, 4 sel, 8 sel, 16 sel, dst (2 pangkat).
3. Grup boleh saling berhimpit dengan grup lain.
4. Grup tidak memiliki sel 0

Lalu, catat grup yang terbentuk.

Jika sudah, berikut adalah prosedur untuk menerjemahkan grup tersebut:

1. Pada grup tersebut, cek apakah nilai variabel berubah, jika nilai variabel berubah, maka variabel tersebut di nihilkan/tidak dianggap.
2. Jika nilai variabel tetap, dengan nilai HIGH, maka catatlah variabel tersebut.
3. Jika nilai variabel tetap, dengan nilai LOW, maka catatlah komplemen dari variabel tersebut.
4. Lalu, buat produk dari variabel-variabel tersebut, sertakan informasi komplemennya.
5. Voila ! anda telah mendapatkan 1 _Prime Implicant_ dari ekspresi awal.
6. Ulangi untuk setiap grup, tentukan _Prime Implicant_ nya, lalu sumkan/ORkan.

Contoh:

![Kernaugh Implicant](https://upload.wikimedia.org/wikipedia/commons/thumb/0/00/K-map_6%2C8%2C9%2C10%2C11%2C12%2C13%2C14_don%27t_care.svg/800px-K-map_6%2C8%2C9%2C10%2C11%2C12%2C13%2C14_don%27t_care.svg.png)



## Permasalahan 6
Jelaskan kaidah penggunaan kondisi don’t care (x) dalam K-map.

Solusi:

![Dont Care Condition in a K-Map](https://www.allaboutcircuits.com/uploads/articles/logic-function-desired-output.jpg)

Pertama, untuk perlu ditentukan deretan input yang seperti apa saja yang menghasilkan kondisi Dont Care. Sebagai contoh, pada Binary Coded Decimal, panjang input yang digunakan adalah 4 digit (Excess-3), yang berarti walau hanya 10 dari kombinasi yang terdefinisi outputnya, ada total 16 kombinasi. Maka 6 kombinasi tersebut berkondisikan Dont Care.

Apabila sudah ditentukan input seperti apa saja yang bersifat Dont Care, tentukan indexnya, lalu daftarkan pada Kernaugh Map dalam bentuk "x". Sel "x" ini dapat dianggap bernilai 1 atau 0. Hal ini berguna pada tahap pengelompokkan K-Map. apabila satu grup sel-sel 1 mengalami disparitas/perlubangan kecil, dan ternyata lubang-lubang tersebut berupa sel "x"/ sel Dont Care, maka anggap saja sel tersebut sebagai sel 1. Tujuan dari pemanfaatan sifat ini adalah untuk memudahkan pengelompokkan dan penyederhanaan.



## Referensi
1. “Don’t Care Condition - Javatpoint,” _www.javatpoint.com_. https://www.javatpoint.com/dont-care-condition-in-k-map-in-digital-electronics#:~:text=The%20%22Don
2. “Boolean Functions(SOP,POS forms),” _Electronics Hub_, Aug. 07, 2015. https://www.electronicshub.org/boolean-logic-sop-form-pos-form/
3. “What are the essential prime implicants?,” _philosophy-question.com_. https://philosophy-question.com/library/lecture/read/207320-what-are-the-essential-prime-implicants (accessed Mar. 03, 2024).
4. “Canonical and Standard Form,” _GeeksforGeeks_, Oct. 25, 2017. https://www.geeksforgeeks.org/canonical-and-standard-form/











