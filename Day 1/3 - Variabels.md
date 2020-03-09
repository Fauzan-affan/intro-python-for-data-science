# Variables

## Hello, World!

Hampir semua bahasa pemrograman punya yang namanya variabel. Tapi sebelum masuk ke pembahasan variabel, sama seperti belajar bahasa pemrograman yang lain, pertama-tama kita akan belajar membuat `Hello world` terlebih dahulu. Kita coba bandingkan pembuatan `Hello world` di bahasa pemrograman Java, Visual Basic .net, dan Python.

Bahasa pemrograman Java:

```java
class HelloWorld
{
    public static void main(String args[])
    {
        System.out.println("Hello, World!");
    }
}
```

Bahasa pemrograman Visual Basic .net:

```vb
Imports System
Module Module1
   Sub Main()
      Console.WriteLine("Hello, World!")
      Console.ReadKey()
   End Sub
End Module
```

Bahasa pemrograman Python:

```py
print("Hello, World!")
```

Ke tiga sintak di atas jika dijalankan, semua *output*-nya sama, yaitu:

```py
Hello, World!
```

## Python Variabel

Variabel di dalam konteks *Python* adalah menamai sesuatu yang merujuk ke data atau *value*. Variabel dapat menampung berbagai jenis data mulai dari huruf, angka, simbol, spasi, dan lain sebagainya. Kita menggunakan notasi `=` untuk memasukkan nilai ke dalam variabel. Untuk menampung nilai yang bentuknya kata atau kalimat, kita bisa menampungnya dengan pembuka dan penutup tanda petik `""`. Misalnya seperti ini:

```Python
variable = "ini adal@h $ebuah str1ng."
```

Data yang kita masukkan ke dalam variabel di atas disebut tipe data *string*.

> Apa itu tipe data ***string***? Tenang, kita akan bahas semua tipe data Python di *lesson* selanjutnya. Biar ga kaget kita kenalan dulu sama ***string***, ***integer***, dan ***float*** di sini.

Selain *string*, kita juga bisa merujuk variabel angka seperti `2` atau angka desimal seperti `2.5`.

```Python
variableAngka = 2
variableDecimal = 2.5
```

Angka `2` juga dikenal dengan istilah tipe data *integer* dan angka desimal `2.5` dikenal dengan tipe data *float*.

Data atau *value* di *Python* juga memiliki tipe yang berbeda-beda dan bekerja dengan cara yang berbeda-beda pula.

- Contohnya, kita tidak bisa menjumlahkan angka dengan huruf karena memang angka dan huruf adalah tipe data yang berbeda.

    ```py
    5 + '5'
    # Traceback (most recent call last):
    # File "<pyshell#1>", line 1, in <module>
    #    5 + '5'
    # TypeError: unsupported operand type(s) for +: 'int' and 'str'
    ```

## Menamai Variabel

Untuk menamai variabel yang valid, kita bisa menggunakan kombinasi antara huruf kapital, huruf kecil, angka, dan *underscore*.

Contoh penamaan variabel yang valid:

```py
name = "Bob"
Age = 54
has_W2 = True
print(name, Age, has_W2)
# Bob 54 True
```

Perhatikan, ***lowercase*** dan ***uppercase*** dari nama variabel tidak sama. Gunakan ***underscore*** untuk memisahkan kata:

```py
age = 1
Age = 2
aGe = 3
AGE = 4
a_g_e = 5
_age = 6
age_ = 7
_AGE_ = 8

print(age, Age, aGe, AGE, a_g_e, _age, age_, _AGE_)
# 1 2 3 4 5 6 7 8
```

Kita tidak boleh menamai variabel dengan **spasi, tanda seru, tanda minus atau karakter-karakter yang bukan alfanumerik**. Kita juga **tidak boleh menamai variabel dimulai dari angka terlebih dahulu**.

Ini adalah salah satu contoh nama variabel yang salah, karena diawali oleh angka:

```py
1099_filed = False
# SyntaxError: invalid token
```
