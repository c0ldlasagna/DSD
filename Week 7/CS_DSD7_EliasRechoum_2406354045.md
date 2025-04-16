---
title: Case Study - Rangkaian Aritmatika

---

# Case Study - Rangkaian Aritmatika

```
Nama  : Elias Rechoum
NPM   : 2406354045
```
## Preambule

Pada Tugas Pendahuluan, tepatnya pada nomor 5, anda telah membuat sebuah rangkaian 2 bit ripple borrow subtractor. Pada CS kali ini, akan dilakukan pengembangan rangkaian sehingga menjadi 3 bit ripple borrow subtractor.

**Namun, operasi pengurangan kali ini dilakukan menggunakan 2's Complement**, sehingga operasi yang dijalankan rangkaian adalah:

A0A1A2 + 2's(B0B1B2)

Contoh:
5 - 7
101 - 111
=> 101 + 001
=> 110
=> Representasi Desimal = (-1 * $2^2$ + 1 * $2^1$ + 0 *$2^0$)
=> -4 + 2 + 0 = **-2**

Metode dan contoh 2's complement lainnya dapat ditinjau kembali di link berikut : 
[Tutorials Point : Two's Complement](https://www.tutorialspoint.com/two-s-complement)

## Ketentuan (IMPORTANT):
**Untuk rangkaian fisik, anda cukup mengerjakan rangkaian Part 1, yaitu pembuatan rangkaian 2's complement sedangkan Rangkaian Part 2 dapat dikerjakan setelah praktikum**

## Gameplay (Part 1 - Fisik) 

Terdapat dua pendekatan yang dapat anda ikuti untuk membentuk rangkaian 2's Complement, yaitu menggunakan K-Map atau Rangkaian yang Dibentuk dari Logika.
**Anda dibebaskan untuk memilih salah satu dari kedua pendekatan ini.** 

**Anda diperbolehkan untuk mengabaikan Carry Out dari penjumlahan Most Significant Bit (MSB)**

## Pendekatan 1 : K-MAP
Karena setiap kombinasi bilangan biner memiliki nilai 2's complement yang unique, maka secara tidak langsung, rangkaian ini dapat dianggap sebagai encoder. 

Maka pembentukan rangkaian mengikuti proses pembentukan rangkaian encoder yang anda lakukan pada modul sebelumnya, yaitu sebagai berikut:

### 1. Melengkapi Truth Table Hasil 2's Complement

| X2  | X1  | X0  | Y2  | Y1  | Y0  |
| --- | --- | --- | --- | --- | --- |
| 0   | 0   | 0   | 0   | 0   | 0   |
| 0   | 0   | 1   | 1   | 1   | 1   |
| 0   | 1   | 0   | 1   | 1   | 0   |
| 0   | 1   | 1   | 1   | 0   | 1   |
| 1   | 0   | 0   | 1   | 0   | 0   |
| 1   | 0   | 1   | 0   | 1   | 1   |
| 1   | 1   | 0   | 0   | 1   | 0   |
| 1   | 1   | 1   | 0   | 0   | 1   |


### 2. Menggunakan K-Map untuk menentukan persamaan untuk Y2, Y1, dan Y0. (*Bentuk K-Map boleh diubah*)

#### K-Map Y2

| X2 \ X1X0 | 00 | 01 | 11 | 10|
| --- | --- | --- | --- | --- |
| **0** | 0 | 1 | 1 | 1|
| **1** | 1 | 0 | 0 | 0|

#### `Y2 = X2' · X0`

---

#### K-Map Y1

|X2 \ X1X0 | 00 | 01 | 11 | 10|
| --- | --- | --- | --- | --- |
| **0** | 0 | 1 | 0 | 1|
|**1** | 1 | 1 | 0 | 1|

#### `Y1 = X2·X1' + X1'·X0 + X1·X0'`

---

#### K-Map Y0

|X2 \ X1X0 | 00 | 01 | 11 | 10|
| --- | --- | --- | --- | --- |
|**0** | 0 | 1 | 1 | 0|
|**1** | 0 | 1 | 1 | 0|

#### `Y0=X0`

### 3. Membentuk rangkaian dari persamaan Y2, Y1, dan Y0 yang didapatkan.

## Pendekatan 2 : Rangkaian Logika

Cara kedua cukup rumit dan memerlukan akal, namun anda dapat mengikuti panduan berikut untuk mempermudah proses pembentukan rangkaian. Disarankan untuk mencoba pembuatan rangkaian di Proteus terlebih dahulu sebelum membuat rangkaian fisik jika anda menggunakan pendekatan ini.

Perhatikan metode untuk mendapatkan 2's Complement:
a. Mengkomplemenkan seluruh bilangan biner untuk mendapatkan 1's complement. Contoh: 101 -> 010
b. Menjumlahkan hasil 1's complement dengan 1 untuk mendapatkan 2's complement. Contoh: 010 -> 011

Maka hasil 2's complement dari contoh (101) adalah nilai 1's complementnya yang dijumlahkan dengan 1 (011)

Maka Rangkaian yang dibentuk dapat mengikuti proses tersebut.

1. Siapkan input yang anda akan komplemenkan (diperbolehkan menggunakan logic state pada proteus)
2. Hubungkan seluruh input anda kedalam gerbang NOT untuk memperoleh 1's complement
3. Anda perlu menjumlahkan hasil tersebut dengan 1, nilai 1 dapat anda representasikan dengan VCC atau POWER pada Proteus
4. Tinjau kembali persamaan pada Half Adder, apakah persamaan untuk Sum, dan apakah persamaan untuk memperoleh carry.
- Rumus untuk memperoleh sum: ...
- Rumus untuk memperoleh carry: ...
5. Gunakan rumus sum untuk memperoleh hasil penjumlahan LSB (least significant bit) input dengan 1 .
6. Gunakan rumus carry untuk memperoleh nilai carry dari hasil penjumlahan LSB input dengan 1.
7. Sekarang anda perlu menyusun logika untuk bit ke-2. Amati bahwa penjumlahan bit ke 2 dilakukan dengan hasil carry dari operasi pertama (langkah nomor 6), maka gunakan rumus sum untuk memperoleh hasil penjumlahan bit ke 2 dengan carry dari operasi pertama.
8. Sekarang anda perlu menyusun logika untuk bit ke-3, amatilah contoh berikut, dapatkah anda simpulkan kapan bit ke 3 akan menghasilkan 1?
![image](https://hackmd.io/_uploads/rJotPuK0Jg.png)![image](https://hackmd.io/_uploads/SkkjwdtC1e.png)![image](https://hackmd.io/_uploads/HkkaPOtC1l.png)
9. Selesaikan rangkaian berdasarkan logika untuk bit ke-3 yang anda peroleh!


---
### Silahkan membuat bentuk fisik dari rangkaian Part 1, Jika sudah selesai silahkan lanjut ke Part 2 menggunakan Proteus


---
## Gameplay (Part 2 - Proteus & Take Home) 

Jika anda mengerjakan tugas tambahan sebelumnya, anda tahu bahwa terdapat IC komersial yang dibuat khusus untuk menjalankan suatu operasi. IC-IC ini juga dapat ditemukan pada operasi aritmatika, yaitu dalam bentuk 4 bit adder / subtractor.

Anda akan menggunakan IC ini dalam menyelesaikan rangkaian Part 2.

1. Jika belum, pindahkan rangkaian fisik anda ke dalam Proteus
2. Gunakan IC 4 Bit adder (IC 74283 pada library Proteus)
3. Tinjau [datasheet](https://www.alldatasheet.com/datasheet-pdf/pdf/51067/FAIRCHILD/74283.html) dari IC 74283 dan **jawablah** pertanyaan berikut:

### 1. Jelaskan secara ringkas deskripsi / fungsi dari IC 74283 
*(5 poin)*

IC74823 adalah sebuah IC *4 bit Full Adder*, yaitu sebuah IC yang mampu menambah 2 bilangan biner 4 bit dengan carry.

### 2. Dari Truth / Function table pada datasheet, jelaskan fungsi pin Carry in dan Carry out - C0 dan C4 
*(5 poin)*

Carry In (C0) menerima bit carry awal dari tahap penjumlahan sebelumnya, sedangkan Carry Out (C4) mengeluarkan bit carry yang terjadi jika hasil penjumlahan 4-bit melebihi kapasitas, dan dapat diteruskan ke unit penjumlah berikutnya.

### 4. Hubungkan nilai input berupa Logic state pada pin A0-A2 dari IC. A3 dapat anda hubungkan dengan ground karena input diasumsikan berukuran 3 bit.
### 5. Ingat kembali rumus dari pengurangan yang digunakan, yaitu penjumlahan dengan 2's complement. Maka hubungkanlah output rangkaian 2's complement pada pin B0-B2 pada IC. B3 dapat anda hubungkan dengan ground karena input diasumsikan berukuran 3 bit.
### 6. Hubungkan pin C0 dengan VCC / GND sehingga hasilnya sesuai yang diinginkan.
### 7. Pastikan output sudah sesuai. Anda dapat menggunakan contoh 5-7 di awal atau contoh lainnya untuk memastikan output rangkaian sudah benar. Bila dipastikan benar, screenshot rangkaian anda.

![alt text](https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%207/image-2.png)

## Analisis

### 1. Berikan analisis dari rangkaian yang telah anda buat, baik pada Part 1 maupun Part 2. Sertakan foto rangkaian fisik part 1 dan Screenshot rangkaian Part 2. *(60 poin berdasarkan nilai rangkaian dan analisis)*

>    Foto Fisik: 

>    Screenshot Proteus:
![alt text](https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%207/image-1.png)

### Analisis Rangkaian:

Rangkaian ini dirancang untuk subtract 2 bilangan 4 bit dengan 2’s complement dari bilangan biner 4-bit. Prosesnya dimulai dengan tahap inversi, di mana setiap masukan dibalik melalui gerbang NOT sehingga menghasilkan 1’s complement. Selanjutnya, hasil tersebut ditambahkan dengan nilai konstan 1 menggunakan rangkaian penjumlahan, dimana proses penjumlahan dilakukan dengan logika yang mengantisipasi carry (dengan mekanisme look-ahead) sehingga carry tidak dihitung secara berantai seperti pada ripple carry adder. Dengan pendekatan ini, delay propagasi berkurang dan perhitungan 2’s complement dapat dilakukan lebih cepat dan efisien, menghasilkan keluaran yang benar dalam waktu singkat dan menampilkannya di 7 segment. Range hasi yang bisa ditampilkan adalah dari -9 ke 9. Kita memakai sebuah multiplexer untuk menampilkan hasil yang benar, antara 2s complement dan hasil biasa tergantung carry out dari full adder.


### 2. Berdasarkan referensi online atau materi pada kelas DSD, definisikan apa itu Propagation Delay *(10 poin)*

Propagation delay dalam parallel adder adalah waktu yang dibutuhkan agar sinyal carry atau sum dari bit paling rendah (LSB) sampai ke bit paling tinggi (MSB). Karena setiap full adder harus menunggu carry-in dari bit sebelumnya, delay akan bertambah seiring jumlah bit yang dijumlahkan.

Semakin banyak bit, semakin panjang waktu delay total — ini disebut ripple carry delay, karena carry merambat seperti gelombang antar bit.

### 3. Propagation delay dapat dicegah dengan menggunakan carry-look ahead adder / subtractor, berdasarkan pemahaman anda, jelaskan rangkaian manakah yang merupakan carry-look ahead adder? Pendekatan 1 atau 2? *(10 poin)*

Pendekatan 2 menghitung bit carry berdasarkan masukan-masukan sebelumnya tanpa harus menunggu hasil carry sebelumnya. Ini sesuai dengan prinsip carry-look ahead adder, yang mempercepat proses penjumlahan dengan menghitung carry lebih awal (look-ahead), bukan secara berantai seperti ripple carry adder.

### 4. Berikan kesimpulan dari CS modul ini dalam bentuk poin-poin *(10 poin)*

- Memahami konsep 2’s complement dalam pengolahan bilangan biner.

- Penggunaan K-Map untuk minimalisasi fungsi logika.

- Implementasi rangkaian untuk menghasilkan 2’s complement.

- Perbedaan antara ripple carry adder dan carry look-ahead adder.

- Pentingnya perhitungan propagation delay dalam desain rangkaian.

- Pendekatan logika dengan penggunaan gerbang NOT dan adder.

- Optimalisasi kinerja rangkaian melalui perhitungan carry secara paralel.

- Metodologi desain yang melibatkan studi kasus dan simulasi (mis. Proteus).

- Relevansi teknik perancangan rangkaian dalam aplikasi digital modern.

- Penerapan prinsip-prinsip dasar sistem digital untuk pengembangan rangkaian yang efisien.
