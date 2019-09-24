# Quiz

Buatlah *output* *dictionary* seperti ini:

```py
{1: 'km', 2: 'hm', 3: 'dam', 4: 'm', 5: 'dm', 6: 'cm', 7: 'mm'}
```

Dari varibel *tuple* berikut ini:

```py
variabel = ('km','hm','dam','m','dm','cm','mm')
urutan = (1,3,2,4,5,7,6)
```

Jawaban:

```py
variabel = ('km','hm','dam','m','dm','cm','mm')
urutan = (1,3,2,4,5,7,6)
list_variabel = list(variabel)
list_urutan = list(urutan)
list_urutan.sort(reverse = True)

list_urutan[0] /= 1
list_urutan[1] /= 1
list_urutan[2] /= 1
list_urutan[3] /= 1
list_urutan[4] /= 1
list_urutan[5] /= 1
list_urutan[6] /= 1

dictionary = {}
dictionary.update({list_urutan[0]:list_variabel[0]})
dictionary.update({list_urutan[1]:list_variabel[1]})
dictionary.update({list_urutan[2]:list_variabel[2]})
dictionary.update({list_urutan[3]:list_variabel[3]})
dictionary.update({list_urutan[4]:list_variabel[4]})
dictionary.update({list_urutan[5]:list_variabel[5]})
dictionary.update({list_urutan[6]:list_variabel[6]})

print(dictionary)
```
