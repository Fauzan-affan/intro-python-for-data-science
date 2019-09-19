# Tipe Data Float

Mari sekarang kita bermain-main dengan tipe data *float*. Jika kita menjumlahkan bilangan desimal `5.0` dengan `2.5` kita akan mendapatkan `7.5`. Jika kita mengurangi `2.5` dengan `0.5` kita akan menghasilkan `2.0`. Ini menarik, `2.0` sebenarnya bisa dikategorikan *integer* kan ya karena hasilnya adalah bilangan bulat. Tapi karena operan adalah *float* maka hasilnya pun *float*. Apabila teman-teman ingin mendapatkan hasil berupa *integer*, kita bisa menggunakan *sintaks round* (pembulatan).

```Python
5.0 + 2.5 # 7.5
2.5 - 0.5 # 2.0
round(2.5 - 0.5) # 2
```

Kita juga bisa menggunakan operasi bagi dengan tanda *slash* atau `/`. Misalnya `8` dibagi `2` akan menghasilkan `4.0`. Jika diperhatikan operasi tambah, kali, dan kurang selalu menghasilkan *integer*, selama *operand*-nya juga tipe data *integer*. **Khusus untuk operator bagi selalu menghasilkan *float***. Namun, operator `/` atau bagi yang selalu menghasilkan *float* **hanya berlaku di *Python 3***. Untuk *Python versi 2* hasil tergantung *operand* dan hasil pembagiannya.

```Python
8 / 2 # 4.0
```
