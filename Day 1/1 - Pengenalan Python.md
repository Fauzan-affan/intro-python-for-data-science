# Pengenalan Python

## Apa itu Python?

Karena kita menggunakan Python untuk *data science*, sebelum kita membahas lebih jauh tentang *data science*, kita harus mempunyai dasar terlebih dahulu tentang bahasa pemrograman Python. Karena kita akan banyak sekali berhubungan dengan sintak atau kode yang dibuat menggunakan Python pada tahapan eksplorasi datanya nanti. Lalu, apa itu Python?

Python adalah sebuah bahasa pemrograman yang populer dan sering digunakan untuk keperluan data analisis, statistik, data science, big data dan juga digunakan di bidang lainnya seperti web, *internet of things* (IoT) dan masih banyak lagi.

Salah satu keunikan bahasa pemrograman Python adalah menggunakan tabulasi atau *whitespace* sebagai pengganti kurung kurawal atau *do-end* blok di bahasa pemrograman lain. Hal ini membuat Python berbeda dan menjadi bahasa pemrograman yang clean dan "enak" dibaca.

```py
n = 5
while n > 0:
    n -= 1
    if n == 2:
        break
    print(n)
print('Loop ended.')
```

Selain itu Python adalah bahasa pemrograman tingkat tinggi atau *high-level* dan dinamis, dan juga multi paradigma. Dengan Python kamu dapat menulis kode dengan gaya OOP *(Object Oriented Programming)* ataupun prosedural.

Python juga dikenal sebagai bahasa yang fleksibel yang membuat bahasa ini menjadi salah satu bahasa pemrograman favorit untuk mengembangkan aplikasi dengan cepat atau *rapid application development* dan juga dapat digunakan sebagai *scripting language* yang dapat dijalankan baik di terminal maupun di *browser*.

## Kenapa memilih Python?

Jika kita ingin membuat sebuah program, ada banyak sekali pilihan bahasa pemrograman yang bisa dipilih. Lalu, kenapa memilih Python? Di bawah ini adalah beberapa alasan kenapa kita memilih Python:

1. ***Python is Populer***

    Pyhton menjadi cukup populer di beberapa tahun belakangan ini. [Developer Survey Result 2019](https://insights.stackoverflow.com/survey/2019) yang dibuat oleh [Stackoverflow.com](https://stackoverflow.com/) pada tahun 2019 kemarin menunjukkan bahwa, Python menduduki peringkat ke - 4 sebagai teknologi yang paling populer dan menduduki peringkat ke - 1 sebagai teknologi yang paling banyak dicari. Programmer di perusahaan bertaraf internasinal juga banyak yang menggunakan Python dalam keseharian mereka, seperti [Google, Facebook, Instagram, Spotify, dll](https://realpython.com/world-class-companies-using-python/).

2. ***Python is Interpreted***

    Banyak bahasa pemrogramana di-*compile* untuk menjalankannya. Artinya, kode-kode yang telah kita buat butuh untuk di-*translate* terlebih dahulu dalam bahasa mesin, bahasa yang dibaca oleh *processor* komputer kita, baru setelah itu kode-kode bisa dijalankan. Tetapi beda untuk Python karena dia *interpreted*, kode-kode bahasa *interpreted* tidak memerlukan itu.

    Ini membuat Python lebih cepat dalam proses pengkodeannya, karena kita hanya tinggal membuat kode *and run it*, tidak usah di-*translate*.

    Karena Python *interprated* dan tidak di-*compile* ke dalam bahasa mesin, kode yang ditulis dalam satu *platform* juga akan bekerja di banyak *platform* lainnya yang terinstal Python di dalamnya.

    > ***Future reading:*** Silahkan cari di internet untuk mengetahui lebih jauh tentang [perbedaan antara *interprated* dan *compiled* *language*](https://en.wikipedia.org/wiki/Interpreted_language)

3. ***Python is Free***

    Python dikembangkan oleh para kontributor *open source*, oleh karena itu Python gratis untuk diinstal, digunakan, didistribusikan, dan dimanfaatkan walaupun untuk kebutuhakn komersial.

## Menggunakan Python

Python saat ini memiliki dua versi yang umumnya dikenal, versi 2 dan versi 3. Secara sintaks ke dua versi ini hampir-hampir sama akan tetapi ada beberapa perbedaan yang tidak terlalu *compatible* antar versi-nya. Oleh karena itu, kita hanya akan belajar versi 3 saja.

Khusus untuk pengguna macOS, sebenarnya Python sudah ter-*install* secara otomatis hanya saja masih menggunakan versi 2. Jadi kita tetap perlu melakukan instalasi untuk yang versi 3. Bagaimana cara instalasinya? Kita akan menggunakan *package* Python *for data science* supaya lebih mudah untuk di-*install* di komputer masing-masing, yang bernama [**Anaconda**](https://www.anaconda.com/). Pada *lesson* berikutnya kita akan bahas bagaimana langkah-langkah instalasinya. Sampai jumpa pada *lesson* berikutnya!
