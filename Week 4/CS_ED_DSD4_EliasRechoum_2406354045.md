# Case Study - Karnaugh Map

```txt
Nama : Elias Rechoum

NPM : 2406354045

Kelompok : A13

Rekan Kerja : Altaf Farzana (2406355754)
```

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
| :----: | :-: | :-: | :-: | :-: |
| **00** |    |  1 |    |    |
| **01** |    |    |  1 |    |
| **11** |    |    |    |  1 |
| **10** |  1 |    |    |    |

### Persamaan Boolean

`F(A,B,C,D) = AB'C'D'+A'B'C'D+A'BCD+AB'CD'`

### Rangkaian tersebut mungkin bersifat kompleks dan memerlukan biaya yang besar. Oleh sebab itu, sederhanakan rangkaian tersebut agar menggunakan gerbang logika kompleks. Ingat bahwa pada TP, gerbang XOR dan XNOR dapat digunakan untuk pemeriksaan biner

### Persamaan Boolean Dengan Gerbang Kompleks

`F(A,B,C,D) = ((A XOR D) NAND (B XNOR C)) NAND ((A XOR D) NAND (B XNOR C))`

### Dengan rumus Boolean ini, buat rangkaian yang sesuai dan screenshot seluruh kombinasi input yang menyebabkan lampu LED untuk menyala!

|  A  |  B  |  C  |  D  | Output | Foto Rangkaian |
| :-: | :-: | :-: | :-: | :----: | :------------: |
|  0  |  0  |  0  |  0  |   0    |          ![WhatsApp Image 2025-03-05 at 10 55 24_e0b599e5](https://github.com/user-attachments/assets/592f959e-8d18-4f50-a686-3f133866f862)      |
|  0  |  0  |  0  |  1  |   1    |     ![WhatsApp Image 2025-03-05 at 10 55 35_f5a0b894](https://github.com/user-attachments/assets/82a64ad2-1186-4fff-b5c7-7c3b5bf7e3c2)           |
|  0  |  0  |  1  |  0  |   0    |      ![WhatsApp Image 2025-03-05 at 10 55 51_044a51a4](https://github.com/user-attachments/assets/441508c3-5554-4cec-92f0-bb04696dfff3)          |
|  0  |  0  |  1  |  1  |   0    |    ![WhatsApp Image 2025-03-05 at 10 56 10_718f8b63](https://github.com/user-attachments/assets/7e11c736-1854-4d3c-bd08-ab240a01b2ab)            |
|  0  |  1  |  0  |  0  |   0    |   ![WhatsApp Image 2025-03-05 at 10 56 43_95bea503](https://github.com/user-attachments/assets/1cc41726-ff5b-4fbc-a261-6b763c196f0e)             |
|  0  |  1  |  0  |  1  |   0    |     ![WhatsApp Image 2025-03-05 at 10 57 00_c74ef3ec](https://github.com/user-attachments/assets/d005ba08-a2e1-421e-ac44-bdc8ac123d61)           |
|  0  |  1  |  1  |  0  |   0    |  ![WhatsApp Image 2025-03-05 at 10 57 17_9eb4371c](https://github.com/user-attachments/assets/e2c5d665-9026-42de-b46e-995439fb01e7)              |
|  0  |  1  |  1  |  1  |   1    |   ![WhatsApp Image 2025-03-05 at 10 57 26_010a07dc](https://github.com/user-attachments/assets/6856c562-f766-4696-9aab-42009fdb5c41)             |
|  1  |  0  |  0  |  0  |   1    |     ![WhatsApp Image 2025-03-05 at 10 57 48_12cefc03](https://github.com/user-attachments/assets/09c634df-bf42-4c19-91e0-192138690f53)           |
|  1  |  0  |  0  |  1  |   0    |     ![WhatsApp Image 2025-03-05 at 10 58 04_cd3d1e58](https://github.com/user-attachments/assets/7bed4e16-7089-4b9c-894d-fde972956d5c)           |
|  1  |  0  |  1  |  0  |   0    |       ![WhatsApp Image 2025-03-05 at 10 58 23_a4e279f8](https://github.com/user-attachments/assets/31f8b26e-a771-4660-b299-a6e27f9effaa)         |
|  1  |  0  |  1  |  1  |   0    |    ![WhatsApp Image 2025-03-05 at 10 58 34_c3500fc1](https://github.com/user-attachments/assets/09a4cc6e-f335-483c-a6a3-a7f3613a8b69)            |
|  1  |  1  |  0  |  0  |   0    |       ![WhatsApp Image 2025-03-05 at 10 59 01_6d8dafd1](https://github.com/user-attachments/assets/46d45f65-d032-4f23-b380-d7b963f17ed8)         |
|  1  |  1  |  0  |  1  |   0    |     ![WhatsApp Image 2025-03-05 at 10 59 12_f2998950](https://github.com/user-attachments/assets/a72fe792-e812-4b2c-aa53-ab0a9aa2db72)           |
|  1  |  1  |  1  |  0  |   1    |     ![WhatsApp Image 2025-03-05 at 10 59 36_2c5f0955](https://github.com/user-attachments/assets/1c425b61-beb9-49ca-8ec9-1a6c84593c74)           |
|  1  |  1  |  1  |  1  |   0    |     ![WhatsApp Image 2025-03-05 at 11 00 13_962dfc15](https://github.com/user-attachments/assets/2421015d-4c37-40a5-ab05-e6bcfa417416)           |

## 2. Berdasarkan yang telah anda lakukan, berikan analisa mengenai peran gerbang logika kompleks dalam praktikum anda (15 poin)

Peran gerbang logka kompleks dalam praktikum ini adalah untuk meyederhanakan kompleksitas rangkaian. Jika kita merakit rangkaian ini dengan gerbang logika unviversal saja, rangkaian akan memiliki biaya yang sangat tinggi.

## 3. Bagaimana bentuk persamaan anda jika dirangkai dengan gerbang universal? Turunkan persamaannya dan jelaskan kelebihan dan kekurangan dari bentuk universal tersebut! (15 poin)

>### Cukup lakukan penurunan persamaan aljabar kedalam bentuk NAND atau NOR (Pilih salah satu), tidak diwajibkan, namun diperbolehkan untuk mengubah kedalam bentuk rangkaian untuk memastikan kecocokan jawaban.

#### Persamaan dengan gerbang logika kompleks:

1. `(A XOR D) AND (B XNOR C)`

#### Konversi ke NOR

```bash
- X = A XOR D = (A NOR D) NOR ((A NOR A) NOR (D NOR D))

- Y = B XNOR C = ( (B NOR (B NOR C) ) NOR (C NOR (B NOR C) ) )

- X AND Y = ( (X NOR X) NOR (Y NOR Y) )

F(A,B,C,D):
( ((A NOR D) NOR ((A NOR A) NOR (D NOR D)) NOR (A NOR D) NOR ((A NOR A) NOR (D NOR D))) NOR (( (B NOR (B NOR C) ) NOR (C NOR (B NOR C) ) ) NOR ( (B NOR (B NOR C) ) NOR (C NOR (B NOR C) ) )) )
```

## 4. Buatlah kesimpulan dari praktikum kali ini! (Buat dalam bentuk poin-poin!) (10 poin)

Pada Praktikum hari ini, saya:

- Mempelajari peran gerbang kompleks dalam mengurangi biaya sebuah rangkaian.

- Mempelajari fungsi gerbang XOR dan XNOR untuk pemeriksaan bit.

- Merakit sebuah rangkaian digital dengan menggunakan gerbang logika kompleks (XOR)
