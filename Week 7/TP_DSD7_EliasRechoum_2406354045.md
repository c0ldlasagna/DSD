---
title: Tugas Pendahuluan - Rangkaian Aritmatika

---

# Tugas Pendahuluan - Gerbang Logika Kompleks

```
Nama  : Elias Rechoum  
NPM   : 2406354045
```

## Teori

### 1. Berdasarkan referensi yang anda gunakan, berikan jawaban untuk pertanyaan-pertanyaan berikut! (10 poin)

- **Definisi Rangkaian Adder dan Subtractor**  
  Rangkaian *Adder* adalah rangkaian logika digital yang digunakan untuk melakukan operasi penjumlahan dua bilangan biner.  
  Sedangkan *Subtractor* adalah rangkaian logika yang digunakan untuk melakukan operasi pengurangan antara dua bilangan biner.

- **Perbedaan fungsionalitas dan gerbang logika penyusunnya**  
  Fungsionalitas Adder adalah untuk menjumlahkan bit-bit biner, sedangkan Subtractor digunakan untuk mengurangkan bit-bit biner.  
  Adder umumnya menggunakan gerbang logika **XOR, AND, OR**, sedangkan Subtractor menggunakan kombinasi **XOR, AND, NOT**, dan terkadang juga menggunakan teknik *2's complement* untuk mengubah pengurangan menjadi penjumlahan.

- **Definisi dari Carry dan Borrow**  
  - *Carry* adalah bit yang dibawa ke digit berikutnya dalam operasi penjumlahan jika hasil penjumlahan melebihi nilai maksimum (misal 1 + 1 = 10, maka carry = 1).  
  - *Borrow* adalah bit yang dipinjam dari digit berikutnya dalam operasi pengurangan jika bit pengurang lebih besar dari bit yang dikurangi.

### Referensi:  
- “Digital Electronics Tutorial,” Tutorialspoint.com, 2021. https://www.tutorialspoint.com/digital-electronics/ (accessed Apr. 14, 2025).

---

### 2. Jelaskan apa perbedaan antara rangkaian half adder atau half subtractor dan full adder atau full subtractor dan jelaskan kelebihan dari rangakaian full baik adder maupun subtractor (10 poin)

- **Perbedaan**:  
  - *Half Adder/Subtractor* hanya bisa menangani dua bit input (misalnya A dan B) tanpa memperhatikan carry/borrow dari bit sebelumnya.  
  - *Full Adder/Subtractor* mampu menangani tiga input (A, B, dan carry-in atau borrow-in) sehingga bisa digunakan untuk operasi bit bertingkat (multi-bit operation).

- **Kelebihan Full Adder/Subtractor**:  
  Full adder/subtractor lebih cocok digunakan untuk rangkaian penjumlahan atau pengurangan multi-bit karena mereka bisa mengakomodasi carry atau borrow dari operasi sebelumnya.


### Referensi:  
- “Digital Electronics Tutorial,” Tutorialspoint.com, 2021. https://www.tutorialspoint.com/digital-electronics/ (accessed Apr. 14, 2025).

---

### 3. Jelaskan apa yang dimaksud dengan ripple carry adder dan ripple borrow adder serta use case dan pembentukannya  (15 poin)

Ripple Carry Adder adalah susunan beberapa full adder yang dihubungkan secara berantai. Carry dari setiap bit akan ripple ke full adder selanjutnya. Digunakan untuk penjumlahan bilangan biner lebih dari 1 bit.

- Use Case: Digunakan dalam prosesor untuk penjumlahan bilangan 4-bit, 8-bit, dsb.

- Pembentukan: Disusun dari beberapa full adder. Output carry dari FA ke-n menjadi input carry untuk FA ke-(n+1).

Ripple Borrow Subtractor adalah rangkaian yang digunakan untuk melakukan pengurangan biner multi-bit. Secara tradisional, dapat dibentuk dari beberapa full subtractor yang dihubungkan secara berantai, di mana sinyal borrow dari satu blok diteruskan ke blok berikutnya. Namun, secara umum juga bisa dibuat menggunakan full adder dengan pendekatan komplemen dua (2's complement), yaitu dengan menginvers bit-bit bilangan pengurang dan menambahkan 1.

- Use Case: Digunakan dalam ALU atau sistem digital lain yang memerlukan pengurangan bilangan biner.

- Pembentukan:

  - Metode 1 (Full Subtractor): Disusun dari beberapa full subtractor yang mengoperasikan setiap bit dan meneruskan borrow.

  - Metode 2 (Full Adder + 2’s Complement): Invers bit-bit operand B, tambahkan 1 (membentuk komplemen dua), lalu gunakan ripple carry adder untuk menjumlahkan dengan operand A.


### Referensi:  
- “Digital Electronics Tutorial,” Tutorialspoint.com, 2021. https://www.tutorialspoint.com/digital-electronics/ (accessed Apr. 14, 2025).

---

### 4. Jelaskan metode representasi bilangan biner, yaitu signed dan 2's complement, serta jelaskan perbedaannya! (15 poin)


- **Signed Magnitude** adalah representasi bilangan biner di mana bit pertama menunjukkan tanda (0 untuk positif, 1 untuk negatif), sedangkan bit sisanya menunjukkan nilai absolut dari bilangan tersebut.

- **2's Complement** adalah metode representasi bilangan biner negatif dengan cara menginvers bit-bit dari nilai absolut dan menambahkan 1. Bit paling signifikan (MSB) tetap menunjukkan tanda (1 = negatif).

- **Perbedaannya**:
  - *Signed Magnitude* menyimpan angka negatif secara langsung dengan bit tanda, tetapi memiliki dua representasi untuk nol (positif dan negatif).
  - *2’s Complement* lebih efisien secara logika karena hanya memiliki satu representasi untuk nol dan mendukung operasi penjumlahan/pengurangan tanpa konversi tambahan.


### Referensi:  
- “Signed Binary Numbers and Two’s Complement used in Binary,” Basic Electronics Tutorials, Aug. 20, 2018. https://www.electronics-tutorials.ws/binary/signed-binary-numbers.html

---

### 5. X dan Y adalah 2 angka terbelakang dari NPM anda (contoh 2206059591, X = 9, Y = 1), dengan kedua nilai tersebut, Selesaikan 105 - XY dengan: (20 poin)

```
XY = 45

105 - 45 = 60
```

105 dalam Sign Magnitude:

Angka positif, jadi tanda 0, dan nilai biner 105 = `01101001` (8 bit).

45 dalam Sign Magnitude:

Angka positif, jadi tanda 0, dan nilai biner 45 = `00101101` (8 bit).

Pengurangan:

Kita lihat apakah 105 lebih besar dari 45. Karena lebih besar, hasilnya positif.

Sekarang kita tinggal mengurangkan nilai biner tanpa memperhitungkan tanda:

```
105 = 01101001
45  = 00101101
-------------
60  = 00111100 (Hasil biner)
```

Hasil Akhir:

Hasilnya adalah 60, dengan tanda positif, jadi hasil akhirnya adalah 60.

2’s Complement:

- 45 dalam 2's complement (8-bit): `11010011`

105 dalam biner: `01101001` 

```
  01101001   (105)
+ 11010011   (-45)
-----------
  00111100   (Hasil: 60)
```

Hasil akhir: 60

### Referensi:  
- “Signed Binary Numbers and Two’s Complement used in Binary,” Basic Electronics Tutorials, Aug. 20, 2018. https://www.electronics-tutorials.ws/binary/signed-binary-numbers.html

---

### 6. Menggunakan Proteus, buatlah sebuah 2 bit ripple borrow subtractor! (30 poin) 
*Anda diperkenankan untuk menggunakan logic state dan logic probe dalam menyusun rangkaian tersebut. 
Sertakan screenshot dari proteus dengan mencantumkan nama dan NPM anda pada Rangkaian.*

**Jelaskan Secara ringkas cara kerja dari rangkaian yang telah anda buat**

2 bit ripple borrow subtractor menggunakan 2 Full Adder dengan mengambil 2s complement dari input B untuk menghasilkan output A+(~B). Cin pertama harus 1 untuk dapat 2s complement dari bit B pertama.

Langkah 1: Ambil 2's complement dari bit B1 dengan membalikkan bit B1 dan menambahkan 1. Tambahkan 2's complement dari B1 ini dengan A1. Hasilnya adalah bit pertama dari selisih (S1) dan carry bit (C1) yang akan diteruskan ke input carry pada langkah berikutnya.

Langkah 2: Full subtractor kedua menggunakan C1 untuk ditambahkan dengan A2 dan 2's complement dari B2 untuk menghasilkan bit selisih kedua (S2) dan carry bit C2.

**Screenshot:**  
![alt text](https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%207/image.png)

**TIDAK PERLU REFERENSI**
