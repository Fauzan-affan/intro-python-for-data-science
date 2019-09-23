# Tipe Data Dictionary

Sekarang, kita akan membahas struktur data yang lebih fleksibel di *Python*, yaitu *dictionary*. *Dictionary* ini sifatnya adalah kombinasi *key* dan *value*.

*Dictionary Python* berbeda dengan *list* ataupun *tuple* (yang nanti akan kita bahas selanjutnya). Karena, setiap urutanya berisi *key* dan *value*. Setiap ***key* dipisahkan dari *value*-nya oleh titik dua (`:`)**, **item dipisahkan oleh koma**, dan **semuanya tertutup dalam `{}` *(brackets)***. *Dictionary* kosong tanpa *value* ditulis hanya dengan *brackets*, seperti ini: `{}`.

*Value* *dictionary* **bisa berupa tipe data apapun (sama seperti *list*)**, namun ***key*-nya harus berupa tipe data yang tidak berubah** seperti *string*, *angka*, atau *tupel*.

Kalau teman-teman sudah pernah berkenalan dengan *JavaScript Object Notation* *(JSON)*, *dictionary* mirip dengan *JSON*. Berikut contoh penggunaan *dictionary*.

```py
myDictionary = {}
myDictionary = {'nama':'fauzan', 'biodata': {
    'umur': 18,
    'hobi': 'mancing'
    }}
print(myDictionary) # {'nama': 'fauzan', 'biodata': {'umur': 18, 'hobi': 'mancing'}}
```

Seperti *string* yang bisa dideklarasikan dengan `str()`, kita juga dapat mendeklarasikan *dictionary* dengan menggunakan `dict()`.

```py
student = dict(name='fauzan',age=30)
print(student) # {'name': 'fauzan', 'age': 30}
```

Untuk mengakses *dictionary*, kita bisa menggunakan *square brackets* seperti ini `[]`.

```py
student = {} # dictionary kosong
student = {'name': 'John', 'age': 18}
employee = {'cto': {
    'name': 'Jane',
    'age': 33
    }}
print(employee['cto']) # {'name': 'Jane', 'age': 33}
```

Sama seperti *list*, *dictionary* juga merupakan struktur data yang sifatnya *mutable*, artinya isi dari *dictionary* bisa diubah, ditambah, ataupun dikurangi. Untuk mengganti isi dari *dictionary* tinggal menggunakan `=` *(equal sign)*.

```py
student = {'name': 'John', 'age': 18}
student['age'] = 19

print(student) # {'name': 'John', 'age': 19}
```

Kita juga bisa menghapus spesifik item atau seluruh *dictionary* menggunakan perintah `del` dan menghapus semua item dengan `clear`.

```py
diariku = {'Name': 'Zara', 'Age': 7, 'Class': 'First'}
del diariku['Name']; # hapus 1 item dengan key 'Name'
print(diariku) # {'Age': 7, 'Class': 'First'}

diariku.clear(); # hapus semua items di dalam dictionary
print(diariku) # {} artinya tidak ada items

del diariku ; # hapus semua dictionary
print(diariku) # NameError: name 'diariku' is not defined
```

Kita juga bisa mengetahui *key* apa saja yang ada di dalam sebuah *dictionary* dengan menggunakan *method* `keys()` dan juga kita bisa menggunakan `values()` untuk mendapatkan semua *value* yang terkandung di dalam sebuah *dictionary*.

```py
student = {} # dictionary kosong
student = {'name': 'John', 'age': 18}
employee = {'cto': {'name': 'Jane', 'age': 33}}

print(student.keys()) # dict_keys(['name', 'age'])
print(student.values()) # dict_values(['John', 18])

print(employee['cto'].keys()) # dict_keys(['name', 'age'])
print(employee['cto'].values()) # dict_values(['Jane', 33])
```
