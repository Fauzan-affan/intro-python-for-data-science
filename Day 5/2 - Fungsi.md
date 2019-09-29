# Fungsi

Sederhananya fungsi adalah sekumpulan perintah yang bisa kita ulang-ulang. Dengan fungsi, kita dapat memecah program besar menjadi sub program yang lebih kecil. Masing-masing fitur pada program dapat kita pecah ke dalam beberapa fungsi yang kita buat. Pada saat kita membutuhkan fitur tersebut, kita tinggal panggil fungsinya saja.

## Struktur fungsi

Fungsi pada *Python*, dibuat dengan kata kunci **`def` kemudian diikuti dengan nama fungsinya**. Struktur fungsi dibuat dengan aturan penulisan sebagai beriku:

```py
def nama_fungsi():
    # Kode program yang dijalankan jika fungsi dipanggil
    # Kode program yang dijalankan jika fungsi dipanggil
```

Sama seperti blok kode yang lain, kita juga harus memberikan identasi (tab atau spasi) untuk menuliskan isi dari fungsi. Setelah kita buat fungsinya, kita bisa memanggil fungsi tersebut dengan memanggil namanya. Dalam contoh fungsi kali ini kita bisa memanggilnya dengan mengetikkan `nama_fungsi()`, setelah itu kode program di dalamnya akan dijalankan.

Contoh lain, kita ingin membuat fungsi untuk menampilkan sesuatu seperti *hellow world* seperti berikut:

```py
# buat fungsi
def hello():
    print('hellow world')

# panggil fungsi
hello() # hellow world
```

## Fungsi dengan Parameter

Apa itu parameter? Parameter adalah variabel yang menampung *value* untuk diproses di dalam fungsi. Jadi, kita bisa memanfaatkan parameter jika ingin memasukkan sesuatu ke dalam fungsi yang telah kita buat.

Fungsi dengan parameter dapat ditulis dengan aturan sebagai berikut:

```py
def nama_fungsi(parameter):
    # Kode program yang dijalankan jika fungsi dipanggil
    # Kode program yang dijalankan jika fungsi dipanggil
```

Parameter diletakan di dalam `()` dari nama fungsi. Penamaan parameter sama seperti ketika membuat variabel. Jika ingin membuat lebih dari satu parameter, bisa dipisahkan dengan tanda koma, contoh `(parameter_1, parameter_2)`. Untuk pemanggilan fungsinya, kita tinggal mengganti parameter dengan *value* yang mau kita isikan ke fungsi. Berikut contoh fungsi menggunakan parameter:

```py
# Membuat fungsi menghitung luas segitiga
def luas_segitiga(alas, tinggi):
    luas = (alas * tinggi) / 2 # karena ada pembagian, hasilnya menjadi desimal
    print('Luas segitiga: ', luas)

# Pemanggilan fungsi
luas_segitiga(4, 6) # Luas segitiga: 12.0
```

## Fungsi dengan Pengembalian Nilai

Kadang kita butuh hasil proses dari fungsi untuk digunakan pada proses berikutnya. Maka fungsi harus mengembalikan nilai dari hasil pemrosesannya. Nah, cara untuk mengembalikan nilai tersebut adalah dengan menggunkan kata kunci `return` lalu diikuti dengan variabel yang akan dikembalikan. Sekarang, kita mau merubah fungsi luas segitiga yang sudah kita buat sebelumnya menjadi seperti ini:

```py
# Membuat fungsi menghitung luas segitiga
def luas_segitiga(alas, tinggi):
    luas = (alas * tinggi) / 2
    return luas # perhatikan bagian ini

# Pemanggilan fungsi
print('Luas segitiga: ', luas_segitiga(4, 6)) # Luas segitiga: 12.0
```

Jika kita perhatikan, kode yang ada di dalam fungsi luas segitiga berubah. Kita mengganti `print()` menjadi `return` di dalam fungsi luas segitiga. Lalu apa bedanya?

Fungsi memang menampilkan *output* yang sama, tetapi perlu diperhatikan kita **bisa menggunakan *output* tersebut untuk pemrosesan selanjutnya**. Perhatikan contoh fungsi menggunakan *return* yang lain untuk menghitung volume persegi berikut ini:

```py
# rumus: sisi x sisi
def luas_persegi(sisi):
    luas = sisi * sisi
    return luas # menggunakan return

# rumus: sisi x sisi x sisi
def volume_persegi(sisi):
    volume = luas_persegi(sisi) * sisi # memanggil fungsi luas_persegi
    print(volume)

# panggil volume_persegi
volume_persegi(10) # 1000
```

Jika kita perhatikan dari contoh di atas,

- Pertama, kita dapat memanggil fungsi di dalam fungsi.
- ke dua, kita bisa menggunakan *output* dari fungsi `luas_persegi` untuk kita kalikan dengan parameter di fungsi `volume_persegi`.

Nah, **jika kita hanya menggunakan `print()` di dalam fungsi `luas_persegi`, kita tidak mendapatkan hasil dari proses fungsi tersebut, sehingga akan terjadi *error* karena tidak bisa menggunakan hasil dari fungsi tersebut untuk pemrosesan di fungsi `volume_persegi`.**

Contoh lain, fungsi untuk menghitung volume persegi yang menggunakan `print()`:

```py
# rumus: sisi x sisi
def luas_persegi(sisi):
    luas = sisi * sisi
    print(luas) # menggunakan print

# rumus: sisi x sisi x sisi
def volume_persegi(sisi):
    volume = luas_persegi(sisi) * sisi
    print(volume)

# panggil volume_persegi
volume_persegi(10) # unsupported operand type(s) for *: 'NoneType' and 'int'
```
