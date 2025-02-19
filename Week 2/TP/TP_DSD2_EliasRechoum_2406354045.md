# Tugas Pendahuluan - Boolean Algebra And Basic Logic Gates

```txt
Nama    : Elias Rechoum
NPM     : 2406354045
```

## 1. Bagaimana cara menghubungkan input `1` atau `0` ke IC pada breadboard? dan berikan salah satu cara untuk menunjukkan outputnya! (Contohkan pada 1 IC) (10 poin)

Untuk menghubungkan input `0` atau `1` ke IC pada breadboard, kita bisa menggunakan kabel jumper dan switch untuk mengganti input dari `1` ke `0`. Jika switch terbuka (OFF), inputnya 0, dan jika switch tertutup (ON), inputnya `1`.

Untuk menunjukkan output, kita dapat menggunakan LED. Jika LED menyala, output LED adalah `1`. Jika LED mati, output LED adalah `0`.

### Contoh pada IC 7408 (Quad AND):

1. Pada contoh pertama, switch 1 and 2 di posisi **OFF**, yaitu input `0`. Karena kedua input `0` ke sebuah AND gate, LED tidak nyala, yaitu output `0`.
![alt text](https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%202/740800.png)

2. Pada contoh kedua, switch 1 and 2 di posisi **ON**, yaitu input `1`. Karena kedua input `1` ke sebuah AND gate, LED menyala, yaitu output `1`.
![alt text](https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%202/740811.png)

### Referensi: 

- “COS 116 The Computational Universe Laboratory 6: Digital Logic I.” Accessed: Feb. 15, 2025. [Online]. Available: <https://www.cs.princeton.edu/courses/archive/spr06/cos116/COS_116_Lab_6.pdf>
‌

## 2. Teori - Selain `0` dan `1`, terdapat satu lagi state yang penting dikenali, yaitu `Floating`. Apa yang dimaksud dan apa bedanya dengan state `0` ? (10 poin)

Sebuah output dinyatakan `Floating` jika tidak terhubung ke level voltage yang ditentukan, misalnya, tidak terhubung ke ground, dan dapat menyebabkan perilaku yang tidak terekspektasi.

### Referensi: 

- “Floating | Analog Devices,” Analog.com Accessed: Feb. 15, 2025. [Online]. Available:  <https://www.analog.com/en/resources/glossary/floating.html>
‌


## 3. PreCS - (80 poin)

Mr. Kim adalah seorang mantan mahasiswa teknik yang berpindah ke jurusan lain karena desakan lingkungan. Dia selalu dihormati oleh kawan-kawan seangkatannya, baik masa di teknik maupun di luar. Akan tetapi, ia punya satu masalah.
Selama bertahun-tahun perjalanannya, ia belum menemukan seorang `Soulmate` sekalipun, dan ia termasuk orang yang "banyak maunya". Kriteria untuk `Soulmate` yang diinginkan Mr. Kim adalah sebagai berikut : 
 
 - ```(Cantik dan Agamis) atau (Berbudi dan Tidak Dungu)```

Mr. Kim meminta Anda untuk membuatkannya sebuah `rangkaian digital` yang mampu mengecek kualitas calon-calon pasangannya!

### Fungsi Boolean

`F(A,B,C,D)= (A∧C)∨(B∧D)`


### Truth Table 

*(Masing-masing `A`, `B`, `C`, `D` berkorespondensi ke **Agamis**, **Berbudi**, **Cantik**, dan **Dungu**)*

*(Di rangkaian, switch `1`,`2`,`3` dan `4` berkorespondensi ke `A`,`B`,`C`, dan `D`)*


|  A (`1`)  |  B (`2`)  |  C (`3`) |  D (`4`) | Output | Screenshot Rangkaian|
|:---------:|:---------:|:--------:|:--------:|:------:|:-------------------:|
|  0  |  0  |  0  |  0  |   `0`    |![0000](https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%202/0000.png)|
|  0  |  0  |  0  |  1  |   `0`    |![0001](https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%202/0001.png)|
|  0  |  0  |  1  |  0  |   `0`    |![0010](https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%202/0010.png)|
|  0  |  0  |  1  |  1  |   `0`    |![0011](https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%202/0011.png)|
|  0  |  1  |  0  |  0  |   `0`    |![0100](https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%202/0100.png)|
|  0  |  1  |  0  |  1  |   `1`    |![0101](https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%202/0101.png)|
|  0  |  1  |  1  |  0  |   `0`    |![0110](https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%202/0110.png)|
|  0  |  1  |  1  |  1  |   `1`    |![0111](https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%202/0111.png)|
|  1  |  0  |  0  |  0  |   `0`    |![1000](https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%202/1000.png)|
|  1  |  0  |  0  |  1  |   `0`    |![1001](https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%202/1001.png)|
|  1  |  0  |  1  |  0  |   `1`    |![1010](https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%202/1010.png)|
|  1  |  0  |  1  |  1  |   `1`    |![1011](https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%202/1011.png)|
|  1  |  1  |  0  |  0  |   `0`    |![1100](https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%202/1100.png)|
|  1  |  1  |  0  |  1  |   `1`    |![1101](https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%202/1101.png)|
|  1  |  1  |  1  |  0  |   `1`    |![1110](https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%202/1110.png)|
|  1  |  1  |  1  |  1  |   `1`    |![1111](https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%202/1111.png)|




### Link Tinkercad (Jangan lupa dibuat public): 
[Link Rangkaian Tinkercad](https://www.tinkercad.com/things/butiIM3D79s-tp2-dsd-elias-2406354045)


