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

```py
variabel = ('km','hm','dam','m','dm','cm','mm',10,1000,100,10000,100000,10000000,1000000)

list_variabel = list(variabel)

desc = list_variabel[7:14]
desc.sort()

dictionary = {'Satuan panjang' : {}}
dictionary['Satuan panjang'].update({list_variabel[6]:desc[0]})
dictionary['Satuan panjang'].update({list_variabel[5]:desc[1]})
dictionary['Satuan panjang'].update({list_variabel[4]:desc[2]})
dictionary['Satuan panjang'].update({list_variabel[3]:desc[3]})
dictionary['Satuan panjang'].update({list_variabel[2]:desc[4]})
dictionary['Satuan panjang'].update({list_variabel[1]:desc[5]})
dictionary['Satuan panjang'].update({list_variabel[0]:desc[6]})

print(dictionary)
```
