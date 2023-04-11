# BD-Praktikum1
- Buat sebuah database dengan nama latihan1!
```
CREATE DATABASE latihan1;
```
![image](https://user-images.githubusercontent.com/115551911/230502648-26bdaf80-5d47-4556-8a95-fd61186fde58.png)
- Untuk melihat basis data yang ada pada server database MySQL, gunakan perintah: 
```
SHOW DATABASES;
```
![image](https://user-images.githubusercontent.com/115551911/230502840-0b51e6c2-9d30-4e05-84e1-f7a881ffa757.png)
- Buat sebuah tabel dengan nama biodata (nama, alamat) didalam database latihan1!
```
CREATE TABLE siswa (nama VARCHAR(100), alamat TEXT);
```
![image](https://user-images.githubusercontent.com/115551911/230502906-39293619-8aef-4eae-bb67-666b5be3a500.png)
- Tambahkan sebuah kolom keterangan (varchar 15), sebagai kolom terakhir!
```
ALTER TABLE siswa ADD COLUMN keterangan varchar(15) AFTER alamat;
```
![image](https://user-images.githubusercontent.com/115551911/230502951-f18c21ac-4f5e-4b36-8dfb-503388fbea25.png)
- Tambahkan kolom id (int 11) di awal (sebagai kolom pertama)!
```
ALTER TABLE siswa ADD COLUMN id int(11) First;
```
![image](https://user-images.githubusercontent.com/115551911/230503013-59ca6501-3031-4866-9914-c248574aa156.png)
- Sisipkan sebuah kolom dengan nama phone (varchar 15) setelah kolom alamat!
```
ALTER TABLE siswa ADD COLUMN phone varchar(15) after alamat;
```
![image](https://user-images.githubusercontent.com/115551911/230503060-f5223e93-c821-431e-ba6c-006aa1257fe1.png)
- Ubah tipe data kolom id menjadi char(11)!
```
ALTER TABLE siswa MODIFY COLUMN id VARCHAR(11);
```
![Screenshot 2023-04-07 051352](https://user-images.githubusercontent.com/115551911/230503907-be351bc3-98ff-4a44-84df-08188631e511.png)
- Ubah nama kolom phone menjadi hp (varchar 20)!
```
ALTER TABLE siswa CHANGE COLUMN phone hp varchar(20);
```
![Screenshot 2023-04-07 051437](https://user-images.githubusercontent.com/115551911/230504065-ababa271-7da7-4f2b-b465-0a1ba72fa000.png)
- Tambahkan kolom email setelah kolom hp
```
ALTER TABLE siswa ADD COLUMN email text after hp;
```
![Screenshot 2023-04-07 051515](https://user-images.githubusercontent.com/115551911/230504133-2364e919-c61e-4341-996d-d3c19f7633b2.png)
- Hapus kolom keterangan dari tabel!
```
ALTER TABLE siswa DROP keterangan;
```
![Screenshot 2023-04-07 051541](https://user-images.githubusercontent.com/115551911/230504212-e7588c6d-2c16-4836-9746-043943500308.png)
- Ganti nama tabel menjadi data_mahasiswa!
```
ALTER TABLE siswa RENAME data_mahasiswa;
```
![Screenshot 2023-04-07 051607](https://user-images.githubusercontent.com/115551911/230504578-07ee927e-28af-43b7-b59a-06350932d899.png)

```
ALTER TABLE data_mahasiswa CHANGE COLUMN id nim varchar(11);
```
![Screenshot 2023-04-07 051631](https://user-images.githubusercontent.com/115551911/230504347-16363552-6d56-4bad-874a-0e689feac12c.png)
- Jadikan nim sebagai PRIMARY KEY!
```
ALTER TABLE data_mahasiswa ADD PRIMARY KEY(nim);
```
![Screenshot 2023-04-07 051646](https://user-images.githubusercontent.com/115551911/230504410-6e0880aa-3cf3-4d90-abb9-55c1e39a9dae.png)
- Jadikan kolom email sebagai UNIQUE KEY
```
ALTER TABLE data_mahasiswa ADD CONSTRAINT email unique KEY(email);
```
![Screenshot 2023-04-07 051703](https://user-images.githubusercontent.com/115551911/230504647-f01e138d-30b1-457d-8403-f440f35b2cf1.png)
## Evaluasi dan pertanyaan
- Apa maksud dari int (11)?
```
int (11) nunjukkan bahwa kolom memiliki tipe data bilangan bulat (integer) dengan ukuran 11 digit 
```
- Ketika kita melihat struktur tabel dengan perintah desc, ada kolom Null yang berisi Yes dan No. Apa maksudnya ?
```
Jika kolom "Null" adalah "YES", itu berarti kolom tersebut diizinkan untuk memiliki nilai NULL.

Jika kolom "Null" adalah "NO", maka kolom tersebut tidak diizinkan untuk memiliki nilai NULL
```
