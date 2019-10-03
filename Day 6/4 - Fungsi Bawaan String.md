# Fungsi Bawaan String

*String* juga memiliki *build-in function* yang bisa kita gunakan. Diantara yang akan kita bahas adalah `capitalize()`, `upper()`, `replace()`, [dan masih banyak lagi yang lainnya](https://docs.python.org/3/library/stdtypes.html#string-methods).

## Capitalize

Untuk membuat sebuah *string* huruf pertamanya menjadi kapital, kita bisa menyeragamkannya menggunakan `capitalize()`:

```py
name = "liza"
print(name) # liza

rubah = name.capitalize()
print(rubah) # Liza
```

## Upper

Untuk mengubah *string* menjadi huruf kapital semua, kita bisa menyeragamkannya menggunakan `upper()`:

```py
name = "liza"
print(name) # liza

rubah = name.upper()
print(rubah) # LIZA
```

## Replace

Dan yang terakhir, `replace()` dapat kita gunakan untuk mencari dan mengganti karakter dalam sebuah *string*.

```py
name = "liza"
print(name) # liza

rubah = name.replace("z", "s")
print(rubah) # lisa
```
