# Case Study Modul 3
#### Muhammad Pirel Jenar Lubdhaka
#### 2306226681
#### Teknik Elektro 2023



## Truth Table:



| A 2 | A 1 | A 0 | 0 |
|-----|-----|-----|---|
| 0   | 0   | 0   | 1 |
| 0   | 0   | 1   | 0 |
| 0   | 1   | 0   | 1 |
| 0   | 1   | 1   | 0 |
| 1   | 0   | 0   | 1 |
| 1   | 0   | 1   | 1 |
| 1   | 1   | 0   | 0 |
| 1   | 1   | 1   | 1 |



## Permasalahan 1
Apakah persamaan tersebut di dalam bentuk SOM atau POM? Apa yang membedakan keduanya dan bagaimana cara mengkonversi dari 1 bentuk ke bentuk lainnya?

Solusi:

Persamaan tersebut ada dalam bentuk Sum of Minterm. Yang membedakan keduanya adalah bahwa pada SOM setiap suku menyatakan salah satu kondisi dimana outputnya akan bernilai HIGH, sementara pada POM setiap suku menyatakan salah satu syarat agar outputnya bernilai HIGH.

Salah satu cara untuk mengonversi bentuk POS ke SOM dan sebaliknya adalah dengan memanfaatkan prinsip _De Morgan_.

```
F  = xy' + yz'
F' = (xy' + yz')'
   = (xy')'(yz')'
   = (x'+y)(y'+z)
   = x'y' + x'z + yy' + yz
   = x'y' + x'z + yz
F  = F''
   = (x'y'+x'z+yz)'
   = (x'y')'(x'z)'(yz)'
   = (x+y)(x+z')(y'+z')
   = (x+y)(y'+z')
``` 


