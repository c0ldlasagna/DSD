---
title: Case Study - 8 (Latch & Flip-Flop)

---

# Case Study - 8 (Latch & Flip-Flop)

```
Nama        : Elias Rechoum
NPM         : 2406354045
Kelompok    : A13
Rekan Kerja : Altaf Farzana (2406355754)
```

## Rangkaian (40 Poin)

Dalam sebuah sistem otomatisasi rumah futuristic, terdapat smart door dengan electronic lock. Sistem ini dirancang untuk dikendalikan menggunakan switch dan sensor proximity. Keypad memungkinkan penghuni menekan switch yang telah ditentukan untuk membuka pintu, sedangkan sensor proximity secara otomatis membuka pintu saat mendeteksi pengguna yang di-authorize berada dalam jarak dekat. Electronic lock memiliki dua status: terkunci dan terbuka. Ketika sistem berada dalam status terkunci, pintu tetap tertutup . Sebaliknya, dalam status terbuka, pintu dapat dibuka. 

Latch dan flip-flop memainkan peran penting dalam sistem ini:


### Komponen Sistem
1. **Latch untuk Keypad**:
    - Digunakan untuk mengaktifkan sistem berdasarkan input dari switch.
    - **Password** diimplementasikan dengan SR latch.
    - Input S dan R dihubungkan ke dua switch.
    - Ketika switch **Set** ditekan, latch diaktifkan untuk mengubah status, menandakan ada yang ingin masuk.
    - Jika switch **Set** diturunkan, maka pintu tetap terbuka, namun switch **Reset** harus ditekan untuk mengubah status kembali.
    - Output latch terhubung ke **electronic lock** untuk mempengaruhi statusnya.

2. **Flip-Flop untuk Sensor Proximity**:
    - Digunakan untuk melacak status dari sensor proximity.
    - **Sensor proximity** disimulasikan dengan sebuah button (Di sini gunakan saja switch) .
    - Flip-flop digunakan untuk **men-toggle** status sensor proximity.
    - Ketika sensor proximity mendeteksi pengguna yang di-authorize, flip-flop mengubah statusnya.
    - Output flip-flop terhubung ke **electronic lock** untuk mempengaruhi statusnya.

## Ketentuan
- **Latch**: Dibuat dengan gerbang logika **NAND** atau **NOR**.
- **Flip-Flop**: Dapat menggunakan IC flip-flop yang sesuai.

***Buatlah rangkaian asli dari instruksi yang diberikan dan Sertakan foto sekaligus beberapa contoh kondisi input dan output rangkaian! (Minimal 2)***

![alt text](<https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%208/WhatsApp Image 2025-04-23 at 11.38.11_c5c4252b.jpg>)

![alt text](<https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%208/WhatsApp Image 2025-04-23 at 11.38.14_0453ae20.jpg>)



## Analisis dan Kesimpulan (60 Poin)

### 1. Jelaskan dan buatlah analisis pada rangkaian yang anda telah buat, khususnya pada implementasi latch dan flip flop! (20 Poin)

Rangkaian ini dibuat dari dua bagian utama: SR Latch (menggunakan gerbang NOR) dan D Flip-Flop (menggunakan IC 7474).

### Analisis:

#### SR Latch:

U1 dan U2 adalah gerbang NOR yang dikonfigurasi sebagai SR latch. Input SET dan RESET digunakan untuk mengendalikan keadaan output dari latch.

Jika SET = 1 dan RESET = 0, maka output latch akan menjadi HIGH (1).

Jika SET = 0 dan RESET = 1, maka output latch akan menjadi LOW (0).

Jika keduanya SET = 0 dan RESET = 0, maka latch akan menahan keadaan sebelumnya.

Keadaan SET = 1 dan RESET = 1 adalah kondisi tidak valid dan dapat menyebabkan output tidak terdefinisi (race condition).

#### D Flip-Flop:

IC 7474 berfungsi sebagai D Flip-Flop tipe edge-triggered (berpindah hanya pada perubahan tepi clock).

Input D berasal dari input manual, sedangkan CLK diberikan oleh sumber clock eksternal.

Ketika terdapat rising edge (tepi naik) pada clock, maka nilai pada input D akan disalin ke output Q.

#### Gerbang AND:

Gerbang AND digunakan untuk menghasilkan output akhir dari rangkaian, dengan menggabungkan output dari latch dan flip-flop.

Output hanya akan 1 jika kedua input ke U4 adalah 1, yaitu jika output latch dan flip-flop HIGH.

### 2. Sertakan truth / excitation table rangkaian Anda dari masing - masing komponen sampai output logic probe! (10 Poin)

#### Truth Table SR Latch

|SET | RESET | Q (Latch Output)|
|:---|:---:|---:|
|0 | 0 | Q(t-1) (Hold)|
|0 | 1 | 0|
|1 | 0 | 1|
|1 | 1 | Tidak valid|

#### Excitation Table D Flip-Flop

|CLK (↑) | D | Q (Flip-Flop Output)|
|:---|:---:|---:|
|0 → 1 | 0 | 0|
|0 → 1 | 1 | 1|
|Steady | x | Q(t-1)|

#### Truth Table AND

|Q (Latch) | Q (Flip-Flop) | Output AND|
|:---|:---:|---:|
|0 | 0 | 0|
|0 | 1 | 0|
|1 | 0 | 0|
|1 | 1 | 1|


### 3. Jelaskan secara rinci jumlah dan jenis masing-masing IC yang dibutuhkan (5 Poin).

| Jenis IC / Komponen | Jumlah | Keterangan|
|:---|:---:|---:|
| NOR (7402) | 1 | Mengandung 4 NOR, digunakan 2|
| AND (7408) | 1 | Mengandung 4 AND, digunakan 1|
| D Flip-Flop (7474) | 1 | Mengandung 2 D Flip-Flop, digunakan 1|

### 4. Menurut anda, selain contoh yang sudah diberikan di Soal, apa contoh kegunaan Flip-Flop/Latch atau Rangkaian Sekuensial di kehidupan sehari-hari? (10 Poin)

1. Jam Digital / Stopwatch

    Flip-flop digunakan untuk menyimpan dan menghitung waktu berdasarkan pulsa clock.

2. Memori Sementara dalam Mikroprosesor

    Latch digunakan untuk menyimpan bit sementara saat operasi pembacaan dan penulisan data.

3. Sistem Pengunci Otomatis (Misal: Pintu Otomatis)

    Menggunakan flip-flop untuk menyimpan status terkunci atau terbuka berdasarkan sensor.

### 5. Berikanlah kesimpulan terhadap seluruh rangkaian praktikum modul 8 ini (15 poin)

Pada praktikum modul hari ini, kita buat sebuah rangkaian dengan menggunakan latch dan flip flop untuk mensimulasi sebuah lock yang buka dengan keypad dan proximity sensor. Latch dibuat dari 2 gerbang NOR, dan mensimulasikan keypad. Flip flop disambung ke sebuah switch dan clock signal dan mensimulasikan proximity sensor. Output dari kedua rangkaian itu disabmung ke AND, dan lock hanya buka jika kedua kondisi terpenuhi.
