# Fungsi Bawaan List

Setiap stuktur data dan tipe data biasanya memiliki *build-in function*-nya masing-masing. Berikut kita akan bahas beberapa *build-in function* yang akan sering kita gunakan. Dari tipe data yang nantinya akan sering kita gunakan yaitu *list*.

Kita akan sering menggunakan *list* nantinya. Berikut beberapa *build-in function* yang disediakan *list* yang bisa kita gunakan. Kita sudah pernah menggunakan seperti `append()`, `extend()`, dan banyak lagi. Teman-teman bisa melihat daftarnya [disini](https://docs.python.org/3/tutorial/datastructures.html).

## Index

Pertama, ada `index()` yang akan memberikan kita informasi di indeks ke berapa sebuah item berada dalam sebuah *list*. Indeks selalu dimulai dari 0.

```py
languages = ["python", "javascript", "go", "rust"]
print(languages.index("go")) # 2
```

## Sort

Kita juga bisa menggunakan fungsi bawaan *Python* sudah sering kita gunakan sebelumnya yaitu `sort()` untuk mengatur urutan dari sebuah angka, huruf, *list*, dll selama itu bisa diurutkan. Perlu kita ketahui ada 2 jenis *sort* yang biasa digunakan:

- Pertama, *sort* secara *ascending* (urutan dari kecil ke besar). Sintak yang digunakan adalah:

  ```py
  languages = ["python", "javascript", "go", "rust"]
  languages.sort()
  print(languages) # ['go', 'javascript', 'python', 'rust']
  ```

- Ke dua, *sort* secara *descending* (urutan dari besar ke kecil). Sintaksnya hanya ditambahkan `reverse= True`.

  ```py
  languages = ["python", "javascript", "go", "rust"]
  languages.sort(reverse= True)
  print(languages) # ['rust', 'python', 'javascript', 'go']
  ```
