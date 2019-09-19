# Quiz

Buatlah *output* (tanpa tanda kutip), seperti:

```Python
Integer: 18, Float: 20.0, String: 22, Boolean: True
```

Dari variabel berikut ini:

```Python
i = 3
f = 40
s = "22"
b = False
```

Jawaban:

```py
a = "Integer: {}, Float: {}, String: {}, Boolean: {}"
print(a.format(i*6,f/2,s,not b))
```

```Py
print("Integer: " + str(i*6) + ", " + "Float: " + str(f/2) + ", " + "String: " + s + ", " + "Boolean: " + str(not b))
```
