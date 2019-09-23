# Tipe Data Tuple

Struktur data terakhir namanya *tuple*. Cara kerjanya sebenarnya sangat mirip dengan *list*. Bedanya, *tuple* tidak bisa diubah *(immutable)*. *Tuple* ini menggunakan `()` *(parenthesis)* sebagai pembuka dan penutup dari sebuah *tuple*.

```py
# list
people_list = ['anang','heransyah']
people_list[0] = 'masyu'
people_list[0]

# tuple
people_list = ('anang','heransyah')
people_list[0] = 'masyu' # 'tuple' object does not support item assignment

# cara membuat tuple
manusia = ('fauzan',('raka','tiana'))
print(manusia) # ('fauzan', ('raka', 'tiana'))

kategori = tuple('spam') # split perhuruf
print(kategori) # ('s', 'p', 'a', 'm')
```

Untuk mengakses informasi di dalam *tuple*, kita bisa menggunakan indeks mirip seperti *list*.

```py
people = ('Angga', ('dev', 'manager'))
print(people[0]) # 'Angga'
print(people[1]) # ('dev', 'manager')
print(people[1][0]) # 'dev'
```

Informasi di dalam *tuple* dapat juga digabungkan atau dikombinasikan dengan operator `+` *(concantination)* sama seperti penggabungan *string* yang sudah kita pelajari sebelumnya. Selain itu *tuple* juga dapat melakukan repetisi dengan operator `*` dan juga proses *slicing* atau dapat dipecah dan digabungkan dengan cukup mudah.

```py
(1 + 2 ) + (3 + 4) # (1, 2, 3, 4)
(1, 2) * 3 # (1, 2, 1, 2, 1, 2)
numbers = (1, 2, 3, 4, 5, 6, 7)
new_numbers = numbers[0], numbers[1:5] # [1:5] parameter pertama sesuai indeks, parameter ke dua sebelum indeks
print(new_numbers) # (1, (2, 3, 4, 5))
print(numbers) # (1, 2, 3, 4, 5, 6, 7)
```

Selain bentuk dan sintaks yang berbeda, penggunaan *tuple* sebenarnya sangat identik dengan *list* dan juga *string*. Bedanya ketika penggunaan operasi `+`, multiplikasi dengan operasi `*`, dan juga proses *slicing* yang akan menghasilkan *tuple* baru (karena *tuple* bersifat *immutable*) seperti di atas.

*Method-method* yang dimiliki oleh *tuple* juga berbeda dengan *method-method* yang disediakan oleh struktur data *list* dan juga *string*. Kalau teman-teman ingin melakukan *sorting* terhadap *tuple* yang bisa kita lakukan adalah konversi terlebih dahulu *tuple* menjadi *list* dan baru lakukan proses *sorting*.

```py
email_attr = ('to', 'from', 'cc', 'bcc', 'subject', 'body')
email_attr_list = list(email_attr) # konversi ke list
email_attr_list.sort() # mengurutkan list
print(email_attr_list) # ['bcc', 'body', 'cc', 'from', 'subject', 'to']
```

Dan semenjak *Python* versi `3.0`, *tuple* tidak memiliki *build-in method* lagi sehingga operasi seperti *sort* dan lain sebagainya dilakukan via *list* seperti contoh di atas.
