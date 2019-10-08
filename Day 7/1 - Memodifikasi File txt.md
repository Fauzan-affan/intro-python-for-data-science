# Modifikasi File .txt

Beberapa dari kita mungkin sudah *familiar* dengan istilah *file* di dalam komputer. *File* adalah **sebuah media penyimpanan di dalam komputer atau laptop kita, yang diatur oleh sistem operasi baik itu *windows*, *linux*, *macOS*, dll.**

*Python* memiliki banyak fungsi untuk berinteraksi dengan *file* dan hal-hal yang terkait dengan *file* seperti direktori *(folder)*, informasi *file*, dan masih banyak lagi.

Contohnya dengan fungsi `open()` *Python* bisa membuka *file* yang terhubung dengan *file* yang ada di sistem operasi (maksudnya di dalam komputer).

Setelah kita membuka atau membuat *file* dengan `open()` (kalau nama file yang di-*open* tidak ada, maka akan otomatis membuat *file* baru) kita bisa menambahkan data dalam bentuk *string*.

Dibandingkan dengan strukur data lain yang sudah kita bahas sebelumnya, **struktur data *file* ini sedikit berbeda**. Struktur data *file* bukanlah angka, baris karakter, ataupun pemetaan (himpunan). Struktur data *file* ini tidak dapat melakukan operasi seperti `+` (penambahan) dan `*` (perkalian) sebagaimana dapat dilakukan di struktur data lainnya.

## Tipe File

Pada *Python*, *file* hanya dikelompokkan menjadi dua tipe:

1. ***File Teks:*** *File* yang berisi teks.

    Contohnya File dengan *extension*: TXT, MD, CSV, JSON, dsb.

2. ***File Binary:*** *File* yang bukan teks, hanya bisa diproses oleh program tertentu yang memahami strukturnya.

    Contohnya File dengan *extension*: EXE, JPG, MKV, M4A, 3GP, dsb.

Karena keterbatasan waktu, kita hanya akan membahas cara membaca dan menulis *file* teks dengan *extension* `.txt` saja.

## Membuka Sebuah File

```py
# format penggunaan open()
open('nama_file.txt', 'mode')

# contoh membuka file myfile.txt dengan mode 'w'
open('myfile.txt', 'w')
```

Untuk membuka sebuah *file*, kita menggunakan fungsi `open()` dengan nama *file* sebagai parameter pertama diikuti dengan *mode* yang ingin kita gunakan. Beberapa mode yang sering digunakan adalah:

- `r` untuk mode *read-only*
- `w` untuk membuat dan mengubah *file*
- `a` untuk menambahkan isi *file*
- `b` untuk memasukkan data dalam bentuk *binary*
- `+` untuk membaca dan menulis *file* dalam satu waktu

## Berinteraksi dengan File

Mari kita mulai mencoba berinteraksi dengan *file*. Kita bisa membuka dan menulis isi sebuah *file*. Jangan lupa perhatikan *path* pemanggilan *file*-nya.

```py
myfile = open('myfile.txt', 'w')
myfile.write('halo text file!\n') # 16 adalah panjang karakter termasuk spasi dan baris baru
myfile.write('selamat tinggal text file!\n') # 27
myfile.close()
```

Ketika kita *close*, *Python* akan membuat file baru dengan nama `myfile.txt` dengan mode `w` atau *write*. Apabila sudah ada *file* dengan nama yang sama, maka *python* tidak akan membuat file baru, melainkan menggunakan *file* yang sudah ada tersebut.

Setelah dibuka kita dapat menuliskan isi *file* tersebut dengan fungsi `write()`. Ingat `write()` adalah fungsi, sedangkan `w` adalah mode, kedunya berbeda.

Dan terakhir kita `close()` untuk memastikan apa yang kita tulis tersimpan ke dalam *file* sebenarnya. **Perlu diketahui, selama kita belum memanggil fungsi `close()`, modifikasi pada *file* kita tidak akan tersimpan.** Jadi, jangan lupa menutup *file* yang sudah kita buka sebelumnya, untuk menyimpan perubahan.

## Membaca File dengan readline()

Ketika sebuah *file* dibuat, kita dapat membuka lagi *file* tersebut dengan fungsi `open()` dan kita bisa membaca isinya dengan beberapa fungsi, salah satunya adalah `readline()` yang akan **membaca isi *file* baris per baris**.

```py
myfile = open('myfile.txt')
myfile.readline() # 'halo text file!\n'
myfile.readline() # 'selamat tinggal file!\n'
myfile.readline() # ''
```

Jika kita perhatikan, tidak ada fungsi `close()`. Ini disebabkan karena kita tidak merubah atau menambahkan struktur *file* `myfile.txt` tapi kita hanya ingin membaca isinya saja, untuk itu kita tidak memerlukan fungsi `close()`.

## Membaca File dengan read()

Jika kita ingin membaca seluruh isi *file*, kita bisa menggunakan fungsi `read()`.

```py
# contoh 1
open('myfile.txt').read() # 'halo text file!\nselamat tinggal text file!\n'

# contoh 2
print(open('myfile.txt').read())
# halo text file!
# selamat tinggal text file!
```

## Menyimpan Variabel Python ke dalam File

Kita juga bisa menyimpan variabel *Python* ke dalam *file*. Misalnya saja variabel dengan tipe data *integer*, *string*, *tuple*, *list*, dan yang lainnya. Yang perlu diingat adalah *file* hanya bisa menerima tipe data *string* sehingga kita harus melakukan konveversi variabel dengan tipe data tersebut ke dalam *string* baru kemudian dimasukkan ke dalam *file*.

```py
# deklarasi variabel
x, y, z = 43, 44, 45 # integer
message = 'Spam' # string
data = {'a': 1, 'b': 2} # dictionary
lists = [1, 2, 3] # list

# masukkan variabel ke file
file = open('datafile.txt', 'w')
file.write(message + '\n')
file.write('%s,%s,%s\n' % (x, y, z)) # %s cara lain konversi ke string
file.write(str(lists) + '\n' + '$' + str(data) + '\n')
file.close()
```

Dan ketika *file* sudah kita isi dan kita tutup, sekarang kita bisa melihat hasilnya kembali dengan menggunakan fungsi `open()`.

```py
chars = open('datafile.txt').read()

chars
# "Spam\n43,44,45\n[1, 2, 3]${'a': 1, 'b': 2}\n"

print(chars)
# Spam
# 43,44,45
# [1, 2, 3]
# ${'a': 1, 'b': 2}
```

Kita bisa juga menampilkan seluruh isi *file* tanpa menggunakan fungsi `read()` seperti di atas.
