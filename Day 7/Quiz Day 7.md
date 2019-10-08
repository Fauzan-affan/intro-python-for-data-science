# Quiz

Buatlah biodata diri anda yang berisi nama, jenis kelamin, dan umur menggunakan *dictionary*. Kemudian, masukkan ke dalam *file* berekstensi json.

Jawaban

```py
import json
biodata = dict(nama='Angga', jenis_kelamin='laki - laki', umur='17')

write_file = open('biodata.json', 'w')
json.dump(biodata, write_file)
write_file.close()

json_file = open('biodata.json')
json.load(json_file)
```
