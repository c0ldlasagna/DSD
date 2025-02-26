# Case Study - Karnaugh Map

``` txt
Nama        : Elias Rechoum
NPM         : 2406354045
Kelompok    : A13
Rekan Kerja : Altaf Farzana (2406355754)
```

## 1. Praktikum (70 poin)

Lanjutan dari TP kemarin adalah anda hanya perlu membuat versi fisiknya di praktikum ini :v

### Truth Table
|  A  |  B  |  C  |  D  | Output |
|:---:|:---:|:---:|:---:|:------:|
|  0  |  0  |  0  |  0  |   0    |
|  0  |  0  |  0  |  1  |   1    |
|  0  |  0  |  1  |  0  |   1    |
|  0  |  0  |  1  |  1  |   1    |
|  0  |  1  |  0  |  0  |   0    |
|  0  |  1  |  0  |  1  |   1    |
|  0  |  1  |  1  |  0  |   1    |
|  0  |  1  |  1  |  1  |   1    |
|  1  |  0  |  0  |  0  |   0    |
|  1  |  0  |  0  |  1  |   0    |
|  1  |  0  |  1  |  0  |   1    |
|  1  |  0  |  1  |  1  |   0    |
|  1  |  1  |  0  |  0  |   1    |
|  1  |  1  |  0  |  1  |   1    |
|  1  |  1  |  1  |  0  |   1    |
|  1  |  1  |  1  |  1  |   1    |


### Karnaugh Map 

| AB\CD | 00  | 01  | 11    | 10    |
|:-----:|:---:|:---:|:-----:|:-----:|
| **00**|  0  |  1  | 1     |  1   |
| **01**|  0  |  1  | 1     |  1   |
| **11**|  1  |  1  | 1     |  1   |
| **10**|  0  |  0  | 0     |  1   |

### Persamaan Boolean
`F(A,B,C,D) = AB + A'D + CD'`


### Dengan rumus Boolean ini, buat rangkaian yang sesuai dan foto seluruh kombinasi input yang menyebabkan lampu LED untuk menyala!


|  A  |  B  |  C  |  D  | Output | Foto Rangkaian |
|:---:|:---:|:---:|:---:|:------:|:--------------:|
|  0  |  0  |  0  |  0  |   0    |![WhatsApp Image 2025-02-26 at 11 14 11_5af07704](https://github.com/user-attachments/assets/423f9cc5-2bfc-4864-ab3e-c0ce0c00f830)|
|  0  |  0  |  0  |  1  |   1    |![WhatsApp Image 2025-02-26 at 11 14 47_d91bc784](https://github.com/user-attachments/assets/3971ed2c-07c6-4678-948c-f01f809fa4c3) |
|  0  |  0  |  1  |  0  |   1    |![WhatsApp Image 2025-02-26 at 11 15 10_e0bdad81](https://github.com/user-attachments/assets/2ed6b762-8d73-4c3c-9768-d8e66625e17b) |
|  0  |  0  |  1  |  1  |   1    |![WhatsApp Image 2025-02-26 at 11 15 24_46f0779e](https://github.com/user-attachments/assets/a7faec82-8392-4706-aeb7-7ac28681c4ba)|
|  0  |  1  |  0  |  0  |   0    |    ![WhatsApp Image 2025-02-26 at 11 14 11_68730618](https://github.com/user-attachments/assets/b67a7f55-91ef-41e7-abdc-c6c873d8bb0b)|
|  0  |  1  |  0  |  1  |   1    |![WhatsApp Image 2025-02-26 at 11 15 51_d218c286](https://github.com/user-attachments/assets/133f2733-e83b-42da-9db5-d37f02a4d6e8)|
|  0  |  1  |  1  |  0  |   1    |![WhatsApp Image 2025-02-26 at 11 16 09_40c109eb](https://github.com/user-attachments/assets/48eb7be1-767a-4058-8646-fcecc3ccd0c3)|
|  0  |  1  |  1  |  1  |   1    |![WhatsApp Image 2025-02-26 at 11 17 08_307446c4](https://github.com/user-attachments/assets/d8e4d448-f24c-4b3d-95f7-0b150793dc60)|
|  1  |  0  |  0  |  0  |   0    |  ![WhatsApp Image 2025-02-26 at 11 17 40_f4f7ddab](https://github.com/user-attachments/assets/c9fd2793-281c-4be2-aa2f-ac49e5762e56)|
|  1  |  0  |  0  |  1  |   0    |    ![WhatsApp Image 2025-02-26 at 11 17 56_e719c77c](https://github.com/user-attachments/assets/6cdef71f-0d1e-48fc-8cbe-8648f1f505b5)|
|  1  |  0  |  1  |  0  |   1    |   ![WhatsApp Image 2025-02-26 at 11 18 09_1148865a](https://github.com/user-attachments/assets/0094f1ac-f86b-4e5f-a7cc-46d65122db0c)|
|  1  |  0  |  1  |  1  |   0    |        ![WhatsApp Image 2025-02-26 at 11 18 28_e67a747a](https://github.com/user-attachments/assets/0db68235-e044-4673-92ce-847bee1d73a3)|
|  1  |  1  |  0  |  0  |   1    |       ![WhatsApp Image 2025-02-26 at 11 18 47_0c390ceb](https://github.com/user-attachments/assets/c3010353-f81f-42a3-bed1-2a1c27b00b1e)|
|  1  |  1  |  0  |  1  |   1    |   ![WhatsApp Image 2025-02-26 at 11 19 00_f41a57a6](https://github.com/user-attachments/assets/266c7826-08a0-4fe9-846e-4a679cb4cd2f)|
|  1  |  1  |  1  |  0  |   1    |  ![WhatsApp Image 2025-02-26 at 11 19 15_04ffffdb](https://github.com/user-attachments/assets/8b9f5c52-0ce5-4061-a0b6-b633ed0500bc)|
|  1  |  1  |  1  |  1  |   1    |     ![WhatsApp Image 2025-02-26 at 11 19 29_87099e0d](https://github.com/user-attachments/assets/9c7a4a6d-9774-49c8-b4a9-b812a078772c)|

(Ganti dengan foto sirkuit Anda!)

## 2. Tuliskan SUM of Minterms dari Truth Table yang dibuat! Apakah Anda sanggup untuk menyederhanakan dari hasil tersebut tanpa KMAP? (10 poin)

Sum of Minterms dari Truth table adalah: 

```txt
∑(1,2,3,5,6,7,10,12,13,14,15)
```

Saya tidak sanggup menyederhanakan tanpa KMAP.

## 3. Dibanding metode aljabar boolean lainnya (seperti menyederhanakan maxterms dan minterms), metode mana yang menurut Anda lebih efisien? (10 poin)

Menurut saya, KMAP lebih efisien dari metode aljabar boolean lainnya.

## 4. Buatlah kesimpulan dari percobaan kali ini! (Buat dalam bentuk poin-poin!) (10 poin)
- Saya belajar cara menggunakan KMAP untuk menyederhanakan fungsi boolean.
- Saya belajar rakit rangkaian logik digital dari KMAP.
