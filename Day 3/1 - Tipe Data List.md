# Tipe Data List

## Definisi Tipe Data List

Selain *string*, `Python` juga punya struktur data yang akan sering kita gunakan, yaitu *list*. *List,* merupakan kumpulan dari beberapa nilai atau *value*. Buat yang sudah pernah belajar tentang bahasa pemrograman, *list* di bahasa pemrograman lain mirip seperti *array*.

Bedanya *list* dengan *string,* yaitu *list* dapat menampung berbagai jenis tipe data, baik itu angka *(integer atau float),* *string,* *boolean* dan yang lain sebagaianya.

Contoh, misalnya kita punya sebuah ember sebagai variabel. Kalau kita ibaratkan tipe data sebagai *merk* dari ember tersebut. Maka, semua ember yang ber-*merk* *string,* hanya bisa menampung satu jenis isi yaitu *string*. Jika kita ibaratkan *string* sebagai air. Maka, ember yang ber-*merk string* **hanya bisa diisikan dengan air saja**.

Namun, jika kita mempunyai ember dengan *merk* *list*. **Bukan hanya air *(string)* yang bisa diisikan**, tapi kita bisa juga mengisikan tanah *(integer)*, batu *(float)*, dan lain sebagainya ke dalam ember tersebut.

## Cara Membuat List

Untuk membuat sebuah *list* baru, kita bisa gunakan `[]` *square brackets*. Seperti tipe data lainnya, *list* juga dapat dimasukkan ke dalam variabel.

```py
my_list = [1, 2, 3]
print(my_list) # [1, 2, 3]
```

Untuk mengakses masing-masing *value* yang terdapat di dalam *list*, kita bisa menggunakan *indeks*. Indeks selalu dimulai dari 0. Jadi, jika ingin mengakses *list* pertama, kita bisa menuliskannya `nama_list[0]`. Perhatikan contoh berikut:

```py
score = [5,2,3,4,55,21,3]
# [5,2,3,4,55,21,3] <- ini value list
# [0,1,2,3,4,5,6] <- ini indeks list

print(score[0]) # 5
```

## Menggabungkan List

Kita juga bisa menggabungkan *list* menggunakan operasi `+` *(concantination)* dengan syarat **ke dua *operand* harus berupa *list***. Artinya, kita tidak dapat menggabungkan *list* dengan *integer* (bilangan bulat) atau *float* (desimal).

```py
my_list = [1, 2, 3]
print(my_list) # [1, 2, 3]

my_list + 4 # TypeError: can only concatenate list (not "int") to list

my_list + [4, 5] # temporary [1, 2, 3, 4, 5]
print(my_list) # [1, 2, 3]

my_list += [4, 5] # permanently [1, 2, 3, 4, 5]
print(my_list) # [1, 2, 3, 4, 5]
```

## Perkalian List

Mirip seperti *string*, kita ***tidak bisa* melakukan operasi `-` dan `/` di *list***. Tapi, **kita dapat melakukan operasi `*` pada tipe data *list***.

```py
my_list = [1, 2, 3]
print(my_list * 2) # [1, 2, 3, 1, 2, 3]
```

## Menambahkan Value Baru ke Dalam List

### Menggunakan Append

Selain operasi `+` *(concantination)* untuk menambahkan item ke dalam *list*, kita juga bisa memanfaatkan *method* `append()`. *Method* ini akan **menambahkan *value* baru setelah *value* terakhir di dalam *list***.

```py
my_list = [1, 2, 3]
my_list.append(4)
print(my_list) # [1, 2, 3, 4]
```

Dengan *append* kita tidak perlu menggunakan operasi `+` *(concantination)* seperti sebelumnya. Tapi kita hanya bisa memasukkan satu *value* baru saja menggunakan `append()`. Terus, gimana kalau kita mau memasukkan dua atau lebih *value* sekaligus ke dalam sebuah *list?* Kalau kita tetap menggunakan `append()` hasilnya akan *error* seperti di bawah ini.

```py
my_list = [1, 2, 3]
my_list.append(4, 5) # TypeError: append() takes exactly one argument (2 given)
```

Pada contoh di atas, kita tidak bisa menggunakan `append()` karena *method* *append* berisi dua buah *value*. Bagaimana kalau kita coba *append* tipe data *list* ke dalam *list* yang sudah kita masukkan ke dalam variabel?

```py
my_list = [1, 2, 3]
my_list.append([ 4, 5 ])
print(my_list) # [1, 2, 3, [4, 5]]
```

### Menggunakan Extend

Pada contoh sebelumnya yang menggunakan `append()`, malah jadi ada *list* di dalam *list* dong? Kita tidak mau hasilnya seperti itu. Nah, untuk memasukkan banyak data sekaligus cara yang benar adalah menggunakan *method* `extend()`.

```py
my_list = [1, 2, 3]
my_list.extend([ 4, 5, 6 ])
print(my_list) # [1, 2, 3, 4, 5, 6]
```

## Menghapus Value di Dalam List

Selain menambahkan *value*, kita juga bisa menghapus *value* yang sudah ada di dalam *list*. Caranya sangat mudah, kita bisa menggunakan *method* `remove()` yang disediakan *Python*. Kita harus memasukkan *value* yang ingin kita hapus dari *list*. Misalnya kita ingin menghapus angka `4` dari `my_list`.

```py
my_list = [1, 2, 3, 4, 5, 6]
my_list.remove(4)
print(my_list) # [1, 2, 3, 5, 6]
```

Atau kita juga bisa menghapus *list* `[4,5,6]` yang ada di dalam *list* seperti di bawah ini.

```py
my_list = [1, 2, 3, [ 4, 5, 6 ]]
my_list.remove([4, 5, 6])
print(my_list) # [1, 2, 3]
```
