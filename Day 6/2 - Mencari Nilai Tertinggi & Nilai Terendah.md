# Mencari Nilai Terbesar & Nilai Terendah

Kemudian *Python* juga punya `max()` dan `min()` yang dapat kita gunakan untuk mencari nilai terbesar dan juga nilai terendah dari kumpulan data, baik itu *list*, *tuple*, atau barisan angka yang kita berikan. Perhatikan contoh berikut ini:

```py
# LIST
numbers = [1, 2, 3]
print(max(numbers)) # 3
print(min(numbers)) # 1

# TUPLE
t_nums = (1, 3, 5, 7)
print(max(t_nums)) # 7
print(min(t_nums)) # 1

# BARIS ANGKA
print(max(1, 5, 9)) # 9
print(min(1, 5, 9)) # 1
```

Selain kumpulan angka, `max()` dan `min()` juga bisa digunakan untuk kumpulan huruf atau simbol. Dengan catatan, **simbol selalu berada paling rendah dibandingkan huruf**.

```py
# Contoh 1
alphas = ['a', 'b', 'z', '@']
print(max(alphas)) # z
print(min(alphas)) # @
```
