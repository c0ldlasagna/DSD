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
- Example Website [Online]. Tersedia: https://www.myWebsite.com/ilovedigilab/. [Diakses: 25-Aug-2024]

---

### 2. Jelaskan apa perbedaan antara rangkaian half adder atau half subtractor dan full adder atau full subtractor dan jelaskan kelebihan dari rangakaian full baik adder maupun subtractor (10 poin)

- **Perbedaan**:  
  - *Half Adder/Subtractor* hanya bisa menangani dua bit input (misalnya A dan B) tanpa memperhatikan carry/borrow dari bit sebelumnya.  
  - *Full Adder/Subtractor* mampu menangani tiga input (A, B, dan carry-in atau borrow-in) sehingga bisa digunakan untuk operasi bit bertingkat (multi-bit operation).

- **Kelebihan Full Adder/Subtractor**:  
  Full adder/subtractor lebih cocok digunakan untuk rangkaian penjumlahan atau pengurangan multi-bit karena mereka bisa mengakomodasi carry atau borrow dari operasi sebelumnya.


### Referensi:  
- Example Website [Online]. Tersedia: https://www.myWebsite.com/ilovedigilab/. [Diakses: 25-Aug-2024]

---

### 3. Jelaskan apa yang dimaksud dengan ripple carry adder dan ripple borrow adder serta use case dan pembentukannya  (15 poin)

- **Ripple Carry Adder** adalah susunan beberapa full adder yang dihubungkan secara berantai. Carry dari setiap bit akan *ripple* ke full adder selanjutnya. Digunakan untuk penjumlahan bilangan biner lebih dari 1 bit.  
  - **Use Case**: Digunakan dalam prosesor untuk penjumlahan bilangan 4-bit, 8-bit, dsb.  
  - **Pembentukan**: Disusun dari beberapa full adder. Output carry dari FA ke-n menjadi input carry untuk FA ke-(n+1).

- **Ripple Borrow Subtractor** bekerja mirip dengan ripple carry adder, tetapi digunakan untuk pengurangan dan menggunakan sinyal borrow alih-alih carry.  
  - **Use Case**: Digunakan untuk pengurangan biner multi-bit.  
  - **Pembentukan**: Disusun dari beberapa full subtractor. Borrow dari satu blok akan diteruskan ke blok berikutnya.


### Referensi:  
- Example Website [Online]. Tersedia: https://www.myWebsite.com/ilovedigilab/. [Diakses: 25-Aug-2024]

---

### 4. Jelaskan metode representasi bilangan biner, yaitu signed dan 2's complement, serta jelaskan perbedaannya! (15 poin)


- **Signed Magnitude** adalah representasi bilangan biner di mana bit pertama menunjukkan tanda (0 untuk positif, 1 untuk negatif), sedangkan bit sisanya menunjukkan nilai absolut dari bilangan tersebut.

- **2's Complement** adalah metode representasi bilangan biner negatif dengan cara menginvers bit-bit dari nilai absolut dan menambahkan 1. Bit paling signifikan (MSB) tetap menunjukkan tanda (1 = negatif).

- **Perbedaannya**:
  - *Signed Magnitude* menyimpan angka negatif secara langsung dengan bit tanda, tetapi memiliki dua representasi untuk nol (positif dan negatif).
  - *2’s Complement* lebih efisien secara logika karena hanya memiliki satu representasi untuk nol dan mendukung operasi penjumlahan/pengurangan tanpa konversi tambahan.


### Referensi:  
- Example Website [Online]. Tersedia: https://www.myWebsite.com/ilovedigilab/. [Diakses: 25-Aug-2024]

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

    45 dalam 2's complement (8-bit): 11010011

    105 dalam biner: 01101001

    105 - 45 menggunakan 2's complement menghasilkan: 00111100

    Hasil akhir: 60
**Sertakan langkah pengerjaan anda**

[your answer here]

### Referensi:  
- Example Website [Online]. Tersedia: https://www.myWebsite.com/ilovedigilab/. [Diakses: 25-Aug-2024]

---

### 6. Menggunakan Proteus, buatlah sebuah 2 bit ripple borrow subtractor! (30 poin) 
*Anda diperkenankan untuk menggunakan logic state dan logic probe dalam menyusun rangkaian tersebut. 
Sertakan screenshot dari proteus dengan mencantumkan nama dan NPM anda pada Rangkaian.*

**Jelaskan Secara ringkas cara kerja dari rangkaian yang telah anda buat**

**Screenshot:**  
[your answer here]

**TIDAK PERLU REFERENSI**
