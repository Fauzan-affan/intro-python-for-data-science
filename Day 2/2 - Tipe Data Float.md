# Tipe Data Float

Di Python, bilangan desimal kita sebut dengan tipe data *float* atau *floating-point*. Mari sekarang kita bermain-main dengan tipe data *float*. Jika kita menjumlahkan bilangan desimal `5.0` dengan `2.5` kita akan mendapatkan `7.5`.

```py
5.0 + 2.5 # 7.5
```

Jika kita mengurangi `2.5` dengan `0.5` kita akan menghasilkan `2.0`.

```py
2.5 - 0.5 # 2.0
```

Ini menarik, `2.0` sebenarnya ini bisa dikategorikan *integer* karena hasilnya bisa dibulatkan. Tapi karena ke dua variabel adalah *float* maka hasilnya pun menjadi *float*. Apabila teman-teman ingin mendapatkan hasil berupa *integer*, kita bisa menggunakan sintak selain `int()`, yaitu:

* `round()` - pembulatan ke bawah untuk tipe data *float* atau bilangan desimal

    ```Python
    round(2.5 - 0.5) # 2
    ```

> Perbedaaan `round()` dengan `int()` terletak pada cara penggunaannya yang tidak merubah variabel target menjadi tipe data *integer*, melainkan **hanya membulatkannya saja**. Contoh, kita tidak bisa merubah variabel dengan tipe data *string* menjadi variabel dengan tipe data integer menggunakan `round()`

Kita juga bisa menggunakan operasi bagi dengan tanda *slash* atau `/`. Misalnya `8` dibagi `2` akan menghasilkan `4.0`.

```Python
8 / 2 # 4.0
```

> Jika diperhatikan operasi tambah, kali, dan kurang selalu menghasilkan *integer*, selama *variabel*-nya juga bertipe data *integer*. **Khusus untuk operator bagi selalu menghasilkan *float***. Namun, operator `/` yang selalu menghasilkan *float* **hanya berlaku di *Python 3***. Untuk *Python versi 2* hasil tergantung *variabel* dan hasil pembagiannya.

## Casting Float

Sama seperti *integer*, *float* juga memiliki *casting*-nya sandiri yang sudah disedikan oleh Python, yaitu:

* `float()` - Ini akan merubah variabel yang ditarget menjadi *float*
  * Jika variabel target semula bertipe data ***float*** atau ***string***, dia hanya akan merubah varibel tersebut (dengan nilai yang sama) ke dalam tipe data *float* atau bilangan desimal saja.

Contoh penggunaannya adalah seperti berikut:

```py
x = float(1)     # x akan menjadi 1.0
y = float(2.8)   # y akan menjadi 2.8
z = float("3")   # z akan menjadi 3.0
w = float("4.2") # w akan menjadi 4.2
```

> Selama ini kita selalu merubah angka di *string* ke dalam *integer* atau *float*, bagaimana jika karakter di *string* seperti `print(float("one"))` kita *casting* ke *number*? Kira-kira apa yang akan terjadi? Sudah pernah coba?

## Contoh Program dengan Tipe Data FLoat

```py
variabel1 = input("Masukkan bilangan desimal pertama: ")
variabel2 = input("Masukkan bilangan desimal ke dua: ")

v1 = float(variabel1)
v2 = float(variabel2)

print("Hasil penjumlahan ", v1, " dengan ", v2, " adalah: ", v1+v2)
```

> ***Futur Reading:*** Untuk informasi tambahan di dalam tipe data float terdapat potensial *bug* yang mungkin bisa menyulitkan kita dalam pengembangan ke depan, informasinya dapat dibaca pada [artikel ini](https://docs.python.org/3.6/tutorial/floatingpoint.html)
