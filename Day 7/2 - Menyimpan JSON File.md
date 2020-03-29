# Menyimpan JSON FIle

*JavaScript Object Notation* atau JSON adalah **salah satu format yang sangat populer untuk pertukaran data**. *Python* tidak memiliki tipe data *object* seperti halnya bahasa pemrograman lain, tapi *Python* memiliki tipe data *dictionary* yang sangat mirip dengan JSON. Contohya seperti berikut:

```py
name = dict(first='Angga', last='Ramadhan')

rec = dict(name=name, job=['dev', 'senior'], age=22.5)
# name berisi variabel name
# job berisi list
# list berisi float atau desimal

rec
# {'name': {'first': 'Angga', 'last': 'Ramadhan'}, 'job': ['dev', 'senior'], 'age': 22.5}
```

Untuk menyimpan data dalam format JSON, kita **bisa menggunakan *dict* dan kemudian kita gunakan *module* bawaan *Python* yang namanya `json`**.

```py
import json # memanggil module json
```

## Serialization

*Serialization* sama dengan *encoding*. Sederhananya, ***encoding* berarti kita bisa menuliskan sesuatu ke dalam *file* json yang kita punya**. Nah, fungsi bawaan ***module* json** yang disediakan oleh *Python* untuk menulis data adalah `dumps()`. Perhatikan contoh berikut ini:

```py
dump = json.dumps(rec)
```

Penjelasan dari kode di atas adalah:

1. Kita memasukkan variabel `rec` yang sudah diisi sebelumnya ke dalam parameter dari fungsi `dump`, kemudian dimasukkan kembali ke sebuah variabel dengan nama `dump` juga
2. Karena kita tidak menggunakan `from` pada saat `import`, maka untuk menggunakan fungsi `dumps` yang ada di dalam *module* json, kita menulisnya menggunakan *dot (.) notation* seperti ini `json.dumps(rec)`
3. `rec` adalah variabel berisi *dictionary*, yang telah kita buat sebelumnya

## Deserialization

*Deserialization* sama dengan *decoding*. Sederhananya, ***decoding* berarti kita bisa membaca isi dari *file* json**. Fungsi bawaan *module* json yang disediakan oleh *Python* untuk membaca data tersebut adalah `loads()`. Perhatikan contoh berikut ini:

```py
load = json.loads(dump)
```

Kode di atas digunakan untuk membaca variabel `dump` yang berisi variabel `rec` atau *dictionary*. Lalu, kita tampung ke dalam variabel dengan nama `load`.

Jika kita gunakan operator perbandingan `==` pada dua variabel `load` dan `rec` hasilnya akan bernilai `True` karena, ke dua variabel tersebut *value* atau isinya sama.

```py
load == rec # True
```

## Menyimpan Variabel ke dalam File

Kalau sebelumnya kita sudah berhasil meng-*encode* dan men-*decode* *dictionary* kita ke dalam sebuah variabel, sekarang kita akan mencoba memasukkan *dictionary* tersebut ke dalam *file* dengan *extension* json. Untuk menggunakan fungsi `dump()` dan `load()` jangan lupa `import json` terlebih dahulu.

> ***Tips & trick:*** `json.dump(value, nama_file)`

```py
# deklarasi variabel
name = dict(first='Angga', last='Ramadhan')
rec = dict(name=name, job=['dev', 'senior'], age=22.5)

# membuat file baru untuk diencode dictionary rec
write_file = open('test.json', 'w')
json.dump(rec, write_file)
write_file.close()
```

Setelah *encoding* kita lihat seluruh isi *file* `test.json` menggunakan fungsi `read()`. Jangan lupa `open` terlebih dahulu:

```py
json_file = open('test.json')
print(json_file.read())

# {
#   "name": {
#       "first": "Angga",
#       "last": "Ramadhan"
#   },
#   "job": [
#       "dev",
#       "senior"
#   ],
#   "age": 22.5
# }
```

Kita juga bisa membaca *file* json tersebut menggunakan `load()`. Ke duanya fungsi (`read()` dan `load()`) dalam hal ini kegunaannya sama, sama-sama dipergunakan untuk *decoding file* json.

```py
json_file = open('test.json')
loadfile = json.load(json_file)

# print
loadfile

# {
#   "name": {
#       "first": "Angga",
#       "last": "Ramadhan"
#   },
#   "job": [
#       "dev",
#       "senior"
#   ],
#   "age": 22.5
# }
```
