# Tipe Data Integer

Di Python, bilangan bulat kita sebut dengan tipe data *integer*. Misal, kita bisa melakukan operasi matematika seperti `5 + 5` dan menghasilkan `10`.

```py
5 + 5 # 10
```

Lalu, `2 - 2` akan menghasilkan `0`.

```py
2 - 2 # 0
```

Lalu, `10 * 18` atau sepuluh dikalikan delapan belas menghasilkan `180`.

```py
10 * 18 # 180
```

## Casting Integer

Terkadang kita ingin merubah sebuah variabel dengan spesifik tipe data. Ini biasa dikenal dengan istilah ***casting*** (konversi tipe data). Python pada dasarnya adalah bahasa pemrograman yang menganut tipe paradigma OOP (*Object Oriented Programming*). Sehingga dia membutuhkan sebuah *class* untuk mendefinisikan suatu tipe data, biasanya di dalam *class* akan dibuat sebuah ***constructor*** yang fungsinya untuk membuat sebuah variabel baru dengan tipe data yang diinginkan.

> ***Future Reading:*** Untuk mengenal lebih jauh tentang OOP di Python, silahkan kunjungi [artikel 1](https://medium.com/@denihhandoko/object-oriented-programming-oop-dengan-python-3-9a618df7429e) atau [artikel 2](https://www.pythonindo.com/pemrograman-berorientasi-objek-di-python/)

Oleh karena itu, jika kita ingin merubah ke dalam tipe data *integer* dari variabel yang sudah ada, kita bisa menggunakan *constructor* khusus yang sudah disediakan oleh Python, yaitu:

* `int()` - Ini akan merubah variabel yang ditarget menjadi integer
  * Jika variabel target semula bertipe data ***float***, dia akan dibulatkan ke bawah.
  * Jika variabel target semula bertipe data ***string***, dia hanya akan merubah varibel tersebut (dengan nilai yang sama) ke dalam tipe data *integer* saja.

Contoh penggunaannya adalah sebagai berikut:

```py
x = int(1)   # x akan menjadi 1
y = int(2.8) # y akan menjadi 2
z = int("3") # z akan menjadi 3
```

## Contoh Program Dengan Tipe Data Integer

```py
ktp = 897777100
no_kartu_keluarga = 9000000110
tinggi = 180
umur = 17

print("No KTP = ", ktp)
print("No KK = ", no_kartu_keluarga)
print("Tinggi Badan = ", tinggi)
print("Umur = ", umur)
```
