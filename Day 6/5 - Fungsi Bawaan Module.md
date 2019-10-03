# Fungsi Bawaan Module

Apa itu *module?*, setiap *file* yang kita buat dengan ekstensi `.py` merupakan *module*. Berikutnya kita akan mulai menggali lebih dalam tentang *module* di *Python*.

*Module* dapat digunakan untuk mengelola kode kita menjadi paket-paket kecil yang dapat digunakan berulang-kali baik oleh kita, tim, atau orang lain. Apabila *module* tersebut di-*publish*, *module* dapat digunakan oleh orang banyak.

Kita bisa memanggil *module* yang berbeda ke dalam sebuah *module Python* yang lain dengan sintaks `import` ataupun `from`.

## Import

`Import` digunakan untuk mengambil *module* seluruhnya. Contoh:

Anggaplah kita memiliki tiga *file Python*: a.py, b.py dan c.py. *File* a.py merupakan file utama. File b.py dan c.py merupakan *module* yang akan digunakan di *file* utama kita.

*File* a hanya akan memanggil *file* b, tidak ada hubungannya dengan *file* c. Sementara *file* b dan *file* c saling berhubungan.

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

Dan berikut isi dari *file* c:

```py
def add(a, b):
  return a + b
```

Dengan asumsi *file* a ingin menggunakan *file* b, kita bisa memanggilnya dengan perintah *import*.

```py
import b
b.logger("Dipanggil dari a.py!!")
b.error("Tidak ada error")
```

Jika kita perhatikan di *file* b sudah ada *import* dr *file* c. Selanjutnya, kita tinggal melakukan *import file* b. Artinya kita membuka *file* b dan mendapatkan akses ke semua atribut seperti fungsi dan variabel yang ada di *file* b serta akses ke *file* c. Dengan demikian setiap kali kita ingin menggunakan atribut dari *file* b dan c, kita bisa gunakan *dot (.) notation* seperti `b.logger()` dan file b bisa menggunakan fungsi yang ada di *file* c yaitu `c.add(5,5)`.

## From

`From` digunakan untuk mengambil sebagian saja dari sebuah *module*. Secara keseluruhan alangkah lebih baik apabila kita menggunakan atribut yang kita butuhkan saja, dengan kata lain menggunakan `from` sangat dianjurkan dalam rangka efisiensi. Atau istilah kerennya adalah *selective import*.

Apabila *file* a yang sebelumnya menggunakan *import* kita ubah menggunakan *from* akan menghasilkan kode seperti berikut.

```py
from b import logger
logger("Dipanggil dari a.py!!")
```

Dengan menggunakan `from`, sekarang kita tidak lagi menggunakan *dot (.) notation* untuk memanggil fungsi `logger`. Seolah-olah `logger` didefinisikan di dalam *file* a.
