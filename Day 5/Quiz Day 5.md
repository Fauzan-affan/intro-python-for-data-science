# Quiz

Buatlah fungsi dengan pengembalian nilai menggunakan *for* dan *if*, untuk mencari **huruf yang sama**, dari variabel berikut ini:

```py
kata1 = 'swim'
kata2 = 'spam'
```

Jawaban:

```py
# Bahan-bahan (deklarasi variabel global)
kata1 = 'swim'
kata2 = 'spam'
sama = []

# Masak (pemrosesan)
def intersection(kata_pertama,kata_kedua):
    for x in kata_pertama:
        if x in kata_kedua: # in untuk menyortir tiap huruf
            sama.append(x)
    return sama

# Sajikan
huruf_yg_sama = intersection(kata1,kata2)
print(huruf_yg_sama)
```
