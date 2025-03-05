c---
title: Case Study - Karnaugh Map (Reg)
---
---

title: Case Study - Karnaugh Map (Reg)

---

# Case Study - Karnaugh Map

Nama : Elias Rechoum

NPM : 2406354045

Kelompok : A13

Rekan Kerja : Altaf Farzana (2406355754)

## 1. Praktikum (60 poin)

Zakuro berkeinginan untuk membuat rangkaian untuk mengecek kesamaan biner. Cara kerja dari rangkaian tersebut adalah sebagai berikut:

- Rangkaian menerima input biner 4 bit
- Rangkaian hanya akan menghasilkan output 1 (high) apabila bit pertama memiliki ketidaksamaan dengan bit terakhir DAN bit kedua memiliki kesamaan dengan bit ketiga
- Contoh input-output
  - 0011 -> 0, meskipun bit 1 berbeda dengan bit 4, seharusnya bit 2 sama dengan bit 3
  - 0111 -> 1, bit 1 dan 4 berbeda, dan bit kedua dan ketiga sama
  - 0110 -> 0, bit  2 dan 3 sama, namun seharusnya bit bit 1 dan 4 berbeda

### Truth Table


| A | B | C | D | Output |
| - | - | - | - | ------ |
| 0 | 0 | 0 | 0 | 0      |
| 0 | 0 | 0 | 1 | 1      |
| 0 | 0 | 1 | 0 | 0      |
| 0 | 0 | 1 | 1 | 0      |
| 0 | 1 | 0 | 0 | 0      |
| 0 | 1 | 0 | 1 | 0      |
| 0 | 1 | 1 | 0 | 0      |
| 0 | 1 | 1 | 1 | 1      |
| 1 | 0 | 0 | 0 | 1      |
| 1 | 0 | 0 | 1 | 0      |
| 1 | 0 | 1 | 0 | 0      |
| 1 | 0 | 1 | 1 | 0      |
| 1 | 1 | 0 | 0 | 0      |
| 1 | 1 | 0 | 1 | 0      |
| 1 | 1 | 1 | 0 | 1      |
| 1 | 1 | 1 | 1 | 0      |

### Karnaugh Map


| AB\CD  | 00 | 01 | 11 | 10 |
| ------ | -- | -- | -- | -- |
| **00** |    |  1 |    |    |
| **01** |    |    |  1 |    |
| **11** |    |    |    |  1 |
| **10** |  1 |    |    |    | 

### Persamaan Boolean

`F(A,B,C,D) = AB'C'D'+A'B'C'D+A'BCD+AB'CD'`

### Rangkaian tersebut mungkin bersifat kompleks dan memerlukan biaya yang besar. Oleh sebab itu, sederhanakan rangkaian tersebut agar menggunakan gerbang logika kompleks. Ingat bahwa pada TP, gerbang XOR dan XNOR dapat digunakan untuk pemeriksaan biner

Hint: Sederhanakan mengenai Boolean Algebra, lalu konversi kebentuk XOR dan XNOR~~~~

### Persamaan Boolean Dengan Gerbang Kompleks

`F(A,B,C,D) = ((A XOR D) NAND (B XNOR C)) NAND ((A XOR D) NAND (B XNOR C))`

### Dengan rumus Boolean ini, buat rangkaian yang sesuai dan screenshot seluruh kombinasi input yang menyebabkan lampu LED untuk menyala!

|  A  |  B  |  C  |  D  | Output | Foto Rangkaian |
| :-: | :-: | :-: | :-: | :----: | :------------: |
|  0  |  0  |  0  |  0  |   0    |                |
|  0  |  0  |  0  |  1  |   1    |                |
|  0  |  0  |  1  |  0  |   0    |                |
|  0  |  0  |  1  |  1  |   0    |                |
|  0  |  1  |  0  |  0  |   0    |                |
|  0  |  1  |  0  |  1  |   0    |                |
|  0  |  1  |  1  |  0  |   0    |                |
|  0  |  1  |  1  |  1  |   1    |                |
|  1  |  0  |  0  |  0  |   1    |                |
|  1  |  0  |  0  |  1  |   0    |                |
|  1  |  0  |  1  |  0  |   0    |                |
|  1  |  0  |  1  |  1  |   0    |                |
|  1  |  1  |  0  |  0  |   0    |                |
|  1  |  1  |  0  |  1  |   0    |                |
|  1  |  1  |  1  |  0  |   1    |                |
|  1  |  1  |  1  |  1  |   0    |                |


(Ganti dengan foto sirkuit Anda!)

## 2. Berdasarkan yang telah anda lakukan, berikan analisa mengenai peran gerbang logika kompleks dalam praktikum anda (15 poin)

## 3. Bagaimana bentuk persamaan anda jika dirangkai dengan gerbang universal? Turunkan persamaannya dan jelaskan kelebihan dan kekurangan dari bentuk universal tersebut! (15 poin)

### Cukup lakukan penurunan persamaan aljabar kedalam bentuk NAND atau NOR (Pilih salah satu), tidak diwajibkan, namun diperbolehkan untuk mengubah kedalam bentuk rangkaian untuk memastikan kecocokan jawaban.

## 4. Buatlah kesimpulan dari praktikum kali ini! (Buat dalam bentuk poin-poin!) (10 poin)
