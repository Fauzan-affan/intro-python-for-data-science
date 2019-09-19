# Tipe Data String

*String* adalah kumpulan karakter, angka, spasi, emoji, dan karakter-karakter lainnya yang dibungkus oleh tanda petik. Kita bisa menggunakan **petik satu** ataupun **petik dua** selama itu **konsisten**. Contoh:

```Python
variable = "ini adal@h $ebuah str1ng."
```

**Yang harus diperhatikan** kita harus membuka dan menutup *string* dengan tanda petik yang sama.

Misalnya, kita menggunakan tanda petik satu artinya *string* harus ditutup juga dengan tanda petik satu. Jika kita membuka dengan petik satu dan menutup dengan petik dua, kita akan mendapatkan *syntax error* dan juga sebaliknya. Apabila kita butuh petik satu di dalam *string*, gunakan petik dua untuk sebagai pembuka dan penutup. Begitu juga sebaliknya.

```Python
# Benar
fruit = "apple"
fruit = 'apple'

message = "He's right!"

# Salah
fruit = "apple' # syntax error

message = 'He's right!' # syntax error
```

Atau kita bisa gunakan *escaping character*. *Escaping character* biasa digunakan untuk memunculkan simbol-simbol atau karakter-karakter yang menyebabkan *error* di *Python*. Terdapat 2 cara *escaping character*. Pertama, menggunakan **`\` *(back slash)***.

```Python
message = 'He\'s right!' # escaping characther \

print(message) # ketika diprint akan memunculkan ' (kutip satu)
```

Cara lain yang lebih *modern* adalah dengan menggunakan **petik satu atau petik dua sebanyak tiga kali**. Dengan cara ini kita bisa menggunakan petik satu, petik dua, bahkan baris baru juga bisa.

```Python
long_message = """Here's a new line!


It's right there mate!"""
print(long_message)
```

Kita bisa memastikan tipe variabel dengan sintaks `type()`.

```Python
variable = "ini adal@h $ebuah str1ng."
type(variable) # <class 'str'>
```

Kita juga bisa gunakan sintaks `str()` untuk mengkonversi *value* ke dalam tipe *string*.

```Python
angka_string = str(17)
type(angka_string) # coba di repl
print(angka_string)
```

Gimana kalau kita sudah punya satu atau beberapa *string* dan ingin membuat *string* baru dengan mengkombinasikan beberapa *string* tersebut? Seperti tipe data *integer* dan *float*, kita bisa menggunakan operator `+` *(concantination)*.

```Python
print('Hello' + "world") # Helloworld
print('Hello ' + "world") # Hello world
```

Yang perlu diingat untuk operator `+` adalah kita **tidak bisa menambahkan *string* dengan angka** dan juga sebaliknya. ***Operand* di ke dua sisi harus sama tipe datanya**. Jika tipe datanya angka, harus dijumlahkan dengan angka juga. Jika tipe datanya *string* maka *operand* ke dua dan seterusnya juga harus *string*.

```Python
# Salah
age = 17
message = "My age is: "
print(message + age) # TypeError

# Benar
age = "17" # tipe datanya string karena dibungkus kutip dua
message = "My age is: "
print(message + age) # My age is: 17
```

Kita bisa konversi variabel `age` menjadi *string* menggunakan `str()`.

```Python
age = 17
message = "My age is: "
print(message + str(age)) # age dikonversi menjadi string
```

Kita juga tidak dapat menggunakan operator `-` dan `/` di tipe data *string*. Tapi, melakukan perkalian menggunakan `*` bisa dilakukan.

```Python
print("=" * 20) # ====================
```

Yang menarik lagi dari *Python*, ada yang namanya *placeholder* menggunakan `{}` *brackets (non-square)* yang membuat *value* yang kita punya menjadi dinamis.

Contoh kita punya *value* variabel seperti berikut:

```Python
pesan = 'ada 10 orang sedang online'
```

Jika kita ingin merubah angka `10` dan kata `orang`, kita tinggal mengganti angka dan kata tersebut dengan `{}`. Lalu, mengganti angka dan kata tersebut melalui *method* `format()` menjadi seperti ini:

```Python
pesan = 'ada {} {} sedang online'
print(pesan.format(8,'gamers')) # kita bisa mengganti 10 dan orang menjadi 8 dan gamers
```
