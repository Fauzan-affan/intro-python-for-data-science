# Fungsi Bawaan Module

Apa itu *module?*, setiap *file* yang kita buat dengan ekstensi `.py` merupakan *module*. Berikutnya kita akan mulai menggali lebih dalam tentang *module* di *Python*.

*Module* dapat digunakan untuk mengelola kode kita menjadi paket-paket kecil yang dapat digunakan berulang-kali baik oleh kita, tim, atau orang lain. Apabila *module* tersebut di-*publish*, *module* dapat digunakan oleh orang banyak.

Kita bisa memanggil *module* yang berbeda ke dalam sebuah *module Python* yang lain dengan sintaks `import` ataupun `from`.

## Import

`Import` digunakan untuk mengambil *module* seluruhnya. Contoh:

Anggaplah kita memiliki tiga *file Python*: a.py, b.py dan c.py. *File* a.py merupakan file utama. File b.py dan c.py merupakan *module* yang akan digunakan di *file* utama kita.

***File* a hanya akan memanggil *file* b, tidak ada hubungannya dengan *file* c. Sementara *file* b dan *file* c saling berhubungan.**

Dan berikut isi dari *file* c:

```py
def add(a, b):
  return a + b
```

Dan berikut isi dari *file* b:

```py
import c

def logger(text):
  print('# File b')
  print('Log: ', text)
  print('Kamsha hamida \n')

  print('# File c')
  print('Log: ', c.add(5,5), '\n')

def error(text):
  print('Error: ', text)
```

Dengan asumsi *file* a ingin menggunakan *file* b, kita bisa memanggilnya dengan perintah *import*.

```py
import b
b.logger("Dipanggil dari a.py!!")
b.error("Tidak ada error")
```

Jika kita perhatikan di *file* b sudah ada *import* dr *file* c. Selanjutnya, kita tinggal melakukan *import file* b. Artinya,

* Kita membuka *file* b dan **mendapatkan akses ke semua fungsi yang ada di *file* b**.
* Kita **mendapatkan akses ke *file* c melalui *file* b**.

> Dengan demikian, setiap kali kita ingin menggunakan fungsi dari *file* b dan c, kita bisa gunakan ***dot (.) notation.***

Contoh, misalkan kita ingin memanggil fungsi `logger` yang terdapat pada *file* b, maka sintak-nya menjadi seperti berikut:

* `b.logger()`

*File* b bisa juga bisa menggunakan fungsi yang ada di *file* c. Contohnya, panggil fungsi `add` yang terdapat pada *file* c, maka sintak-nya menjadi seperti berikut:

* `c.add(5,5)`

## From

`From` digunakan untuk **mengambil sebagian saja dari sebuah *module***. Secara keseluruhan alangkah lebih baik apabila kita menggunakan fungsi-fungsi yang kita butuhkan saja dari file yang kita import karena, menggunakan `from` sangat dianjurkan dalam rangka **efisiensi**. Atau istilah kerennya adalah *selective import*.

> Jika kita mengimport seluruh isi yang ada di dalam suatu file, dan ternyata isinya sangat banyak, maka **secara tidak langsung aplikasi kita akan terasa agak lemot**, tergantung banyaknya isi dari *file* yang kita *import*.

Tambahkan *file* a yang sebelumnya menggunakan *import*, menjadi menggunakan *from*. Dan ambil fungsi yang kita butuhkan saja. Contohnya dalam kasus kali ini, kita mengambil fungsi `logger` yang terdapat pada *file* b:

```py
from b import logger
logger("Dipanggil dari a.py!!")
```

Dengan menggunakan `from`, sekarang kita tidak lagi menggunakan *dot (.) notation* untuk memanggil fungsi `logger`. Seolah-olah `logger` didefinisikan di dalam *file* a.
