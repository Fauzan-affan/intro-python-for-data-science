# Quiz

Buatlah *output* *dictionary* satuan panjang dari milimeter ke kilometer seperti ini:

```py
{'Satuan panjang': {'mm': 10, 'cm': 100, 'dm': 1000, 'm': 10000, 'dam': 100000, 'hm': 1000000, 'km': 10000000}}
```

Dari variabel *tuple* berikut ini:

```py
variabel = ('km','hm','dam','m','dm','cm','mm',10,1000,100,10000,100000,10000000,1000000)
```

*Tanpa menggunakan perulangan

Jawaban:

Sebagai seorang data analis, memproses suatu data itu **sama seperti ketika kita ingin memasak.**

- Pertama, mau **masak apa?**

- Ke dua, kita harus **menyiapkan bahan-bahanya** terlebih dahulu.

- Ke tiga, setelah semua bahannya terkumpul kita bisa **mulai memasak sesuai dengan perintah dari resep masakan** yang mau kita buat.

- Ke empat, setelah semua selesai dimasak, **sajikan** dengan cantik.

```py
variabel = ('km','hm','dam','m','dm','cm','mm',10,1000,100,10000,100000,10000000,1000000)

# masak apa?

## Buat dictionary satuan panjang dari milimeter ke kilometer

# Menyiapkan bahan-bahanya (deklarasi)

## buat dictionary satuan panjang
dictionary = {'Satuan panjang' : {}}
## konversi tuple ke list
list_variabel = list(variabel)
## pisahkan satuan panjang
satuan_panjang = list_variabel[0:7]
## pisahkan angka
angka = list_variabel[7:14]

# Mulai memasak sesuai dengan perintah dari resep masakan

## Resep masakanya ga ada (ga ada step by step), artinya harus manual
## Buatlah output dictionary (sudah dideklarasikan)
## Satuan panjang dari milimeter ke kilometer (urutkan variabel)

## urutkan satuan panjang
## (balik dr indeks ke 6 sampai inkes ke 0)
label = []
label.append(satuan_panjang[6])
label.append(satuan_panjang[5])
label.append(satuan_panjang[4])
label.append(satuan_panjang[3])
label.append(satuan_panjang[2])
label.append(satuan_panjang[1])
label.append(satuan_panjang[0])

## urutkan value angkanya
angka.sort()

## isikan setiap value ke dalam dictionary dengan key 'Satuan panjang'
dictionary['Satuan panjang'].update({label[0]:angka[0]})
dictionary['Satuan panjang'].update({label[1]:angka[1]})
dictionary['Satuan panjang'].update({label[2]:angka[2]})
dictionary['Satuan panjang'].update({label[3]:angka[3]})
dictionary['Satuan panjang'].update({label[4]:angka[4]})
dictionary['Satuan panjang'].update({label[5]:angka[5]})
dictionary['Satuan panjang'].update({label[6]:angka[6]})

# Sajikan!

## Tampilkan hasil
print(dictionary)
```
