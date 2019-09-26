# Quiz

Buatlah *output* *dictionary* satuan panjang dari milimeter ke kilometer seperti ini **menggunakan perulangan**:

```py
{'Satuan panjang': {'mm': 10, 'cm': 100, 'dm': 1000, 'm': 10000, 'dam': 100000, 'hm': 1000000, 'km': 10000000}}
```

Dari variabel *tuple* berikut ini:

```py
variabel = ('km','hm','dam','m','dm','cm','mm',10,1000,100,10000,100000,10000000,1000000)
```

Jawaban:

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
## (balik dr indeks ke 6 sampai indeks ke 0) menggunakan while
label = []
h = len(satuan_panjang) # h = 7

while h > 0: # selama isi satuan_panjang msh ada perulangan akan terus dilakukan
    label.append(satuan_panjang[h-1]) # masukkan satuan panjang dari mulai indeks terakhir yaitu ke 6
    # print(label)
    h = h - 1

## urutkan value angkanya
angka.sort()

## isikan setiap value ke dalam dictionary dengan key 'Satuan panjang' menggunakan for
j = 0
for i in label:
    dictionary['Satuan panjang'].update({label[j]:angka[j]})
    j = j + 1

# Sajikan!

## Tampilkan hasil
print(dictionary)
```
