# Percabangan

Kita akan membahas struktur percabangan dalam bahasa *Python*. Dibuka dengan bentuk percabangan yang paling sederhana, yakni kondisi *if*.

## Kondisional If

*If* merupakan statement kunci untuk percabangan *(branching)*, seleksi, dan membandingkan nilai dengan nilai lainnya. *Statement if* ini juga erat kaitannya dengan tipe data *boolean* karena dia akan mengecek apakah sebuah perbandingan *True* atau *False*.

Format penulisan *if* ini mirip-mirip dengan bahasa pemrograman lain. Menggunakan bahasa *Python*, struktur *if* dibuat dengan aturan penulisan sebagai berikut:

```py
if condition:
  # Kode program yang dijalankan jika condition bernilai True
  # Kode program yang dijalankan jika condition bernilai True
```

Bagian *condition* berperan sebagai penentu dari struktur percabangan. **Jika *condition* terpenuhi (menghasilkan nilai *True*), lalu blok kode program akan dijalankan. Jika *condition* tidak terpenuhi (menghasilkan nilai *False*), blok kode program tidak akan dijalankan.** *Condition* biasanya terdiri dari operasi perbandingan, misalnya apakah variabel *a* berisi angka `10`, atau variabel *password* berisi string `‘rahasia’`.

Biasanya *statement* *if* juga diikuti dengan *else* ataupun *else if.* ***Else if* digunakan apabila ada banyak kemungkinan kondisi yang bisa terjadi**. Di *Python* *else if* menggunakan sintaks `elif`. ***Else* digunakan sebagai *default* kondisi.**

```py
kondisi1 = 0
kondisi2 = 0

if kondisi1: # kondisi pertama
    pass
elif kondisi2: # kondisi ke dua
    pass
else: # default kondisi
    pass
```

Kita coba membuat *if* dengan kondisinya angka `1`. Perlu diingat angka `1` sama dengan *boolean* *True*, jadi kondisi sama saja dengan `if True:`.

```py
if 1: # 1 artinya true (boolean)
    print('true') # true
```

Mari kita lanjutkan kode di atas dengan menambahkan *else* dan kita tambahkan negasi sebelum kondisinya.

```py
if not 1: # 1 artinya not true (boolean)
    print('true')
else:
    print('false')

# False
```

Karena kondisi menghasilkan nilai *False* (`not True == False`) maka blok kode yang akan dieksekusi adalah blok kode ke dua, yaitu `print('false')`.

## If menggunakan Elif dan Else

Ketika kita membuat aplikasi, jarang sekali hanya menggunakan satu percabangan *if* saja. Seringkali, kita dihadapkan oleh banyak kemungkinan yang terjadi yang megharuskan kita memeriksa beberapa kondisi. Karena itu, kita butuh *tools* yang dapat menyaring beberapa kondisi tersebut. Di *Python* kita menggunakan *statement* `elif`.

Mari kita lihat contoh *statement* `elif` dengan membuat sebuah aplikasi sederhana. Aplikasi ini akan menghitung umur pengguna dalam satuan hari, kemudian memberikan saran kepada pengguna tersebut sesuai dengan umurnya. Berikut adalah contohnya:

```py
umur = 25

if umur * 365 > 20000: # menyaring kondisi pertama
    print('Waktunya istirahat :)') # ditampilkan jika umur x 365 = lebih besar dari 20.000 hari (> 54 tahun)
elif umur * 365 > 10000: # menyaring kondisi ke dua
    print('Tenang, kamu masih punya waktu') # ditampilkan jika umur x 365 = lebih besar dari 10.000 hari TAPI kurang dari 20.000 hari (> 27 tahun)
else:
    print('Mari mulai mengukir masa depan!') # default kondisi atau jika umur < 10.000 hari (< 28 tahun)
```

## If dengan Operator

### Operator Logika

Operator logika adalah **operator yang digunakan untuk membuat kesimpulan logis dari 2 kondisi *boolean*: *True* atau *False***. Dalam bahasa *Python* terdapat 3 operator logika:

| Operator | Penjelasan                                 | Contoh        | Hasil |
|----------|--------------------------------------------|---------------|-------|
| and      | True jika ke dua operand bernilai True     | True and True | True  |
| or       | True jika salah satu operand bernilai True | True or False | True  |
| not      | True jika operand bernilai False           | not False     | True  |

### Operator Perbandingan

Operator perbandingan dipakai untuk **membandingkan 2 buah nilai, apakah nilai tersebut sama besar, lebih kecil, lebih besar, dll.** Hasil dari operator perbandingan ini adalah *boolean* *True* atau *False*. Biasanya operator perbandingan digunakan bersamaan dengan operator lain. Di dalam bahasa *Python*, terdapat 6 operator perbandingan:

| Operator | Penjelasan                   | Contoh | Hasil |
|----------|------------------------------|--------|-------|
| ==       | Sama dengan                  | 5 == 5 | True  |
| !=       | Tidak sama dengan            | 5 != 5 | False |
| >        | Lebih besar                  | 5 > 6  | False |
| <        | Lebih kecil                  | 5 < 6  | True  |
| >=       | Lebih besar atau sama dengan | 5 >= 3 | True  |
| <=       | Lebih kecil atau sama dengan | 5 <= 5 | True  |

### Gabungan If, Operator Logika, dan Operator Perbandingan

Sekarang kita coba rubah contoh aplikasi sederhana yang pernah kita buat untuk menghitung umur pengguna dalam satuan hari, menjadi seperti ini:

```py
umur = 25
total_hari = umur * 365

if total_hari >= 20000:
    print('Waktunya istirahat :)')
elif total_hari >= 10000 and total_hari < 20000: # menggunakan operator logika and
    print('Tenang, kamu masih punya waktu')
else:
    print('Mari mulai mengukir masa depan!')
```
