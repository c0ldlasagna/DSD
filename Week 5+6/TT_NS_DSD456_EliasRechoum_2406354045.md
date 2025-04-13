# Tugas Tambahan - 4 5 6

```
Nama : Elias Rechoum
NPM  : 2406354045
```

Dalam tiga modul terakhir, Anda telah mempelajari penggunaan gerbang logika kompleks serta perancangan dan penerapan encoder, decoder, multiplexer, dan demultiplexer.

Saat mengimplementasikan modul-modul tersebut, penting untuk diketahui bahwa terdapat berbagai IC yang sudah dirancang khusus untuk menjalankan fungsi multiplexer, demultiplexer, encoder, dan decoder. Penggunaan IC ini dapat menyederhanakan desain dan meningkatkan efisiensi sistem.

Tugas Anda hari ini adalah memanfaatkan IC-IC tersebut untuk menyelesaikan sebuah masalah sederhana.

### Problem
Anda adalah seorang teknisi di TwinTower Campus, yang memiliki 8 lantai dan 4 buat lift. Demi keberlangsungan acara mendatang, anda diminta untuk mendesain sistem kontrol lift secara manual dengan ketentuan sebagai berikut:

- Terdapat input X Y untuk menentukan lift yang dipilih (1 - 4)
- Terdapat 8 buah input button (1-8) yang dapat untuk menentukan lantai tujuan.
- Terdapat 2 buah 7 segment display. Untuk menampilkan lift yang digunakan (1-4) serta menampilkan lantai tujuan
- Karena TwinTower bersifat superstitious, mereka tidak ingin menampilkan angka 4 pada lift. Oleh sebab itu tampilan lantai dari lift adalah (1 2 3 3A 5 6 7 8).
- Untuk menampilkan huruf A, anda dapat menggunakan 7 segment baru dengan tampilan berikut:
![image](https://hackmd.io/_uploads/SJpxb7ajJl.png)

### Aturan Pengerjaan
- Rangkaian dibuat di Proteus, Dalam pembuatan rangkaian ini, anda diminta untuk menggunakan minimal 1 (boleh lebih) IC komponen Encoder / Decoder / MUX / DEMUX.
- Setelahnya, dokumentasikan komponen serta fungsionalitas yang anda gunakan pada tabel komponen. Bila bagian rangkaian tersebut dibuat tanpa IC komponen Encoder / Decoder / MUX / DEMUX, isi dengan CUSTOM dan cukup isi kolom nama pada tabel.
- Pada bagian akhir dari Tutam, terdapat panduan penggunaan komponen pada Proteus yang dapat dijadikan referensi bila menemukan error.
- Jangan lupa mengerjakan bagian tabel komponen dan refleksi. Good luck!


### Tabel Komponen (20 poin)


| Kode IC | Nama Komponen                         | Kegunaan Dalam Rangkaian                           |
| ------- | ---------------------------------- | ----------------------------------------------------- |
| 7448    | BCD - 7 Seg Decoder (Common Anode) | Untuk menampilkan lantai yangg dipilih pada 7 segment |
| 7482    | 2 Bit Adder                        | Untuk menambah 2 Bit untuk tampilan lift (1,2,3,4)    |
| 4532    | 8 Bit Priority Encoder             | Untuk konversi input dari tombol lantai ke binary     |
| 7483    | 4 Bit Adder                        | Untuk menambah 1 ke input tombol lantai supaya 0 dari 4532 jadi 1, 1 menjadi 2, dsb.|
| 74157   | Quad 2:1 Multiplexer               | Untuk memilih output antara A atau 1-8. Jika tombol 4 dipilih, output akan menampilkan A|
| CUSTOM  | - | Menggunakan NOT dan AND untuk menampilkan A jika lantai 4 dipilih|
 
### Refleksi (10 poin)
Berdasarkan Tutam ini, dalam situasi apa IC komersial, seperti IC multiplexer, demultiplexer, encoder, atau decoder yang sudah jadi, dapat ditemukan atau digunakan?

Melalui tugas tambahan ini, saya belajar bahwa penggunaan IC komersial seperti multiplexer, demultiplexer, encoder, dan decoder sangat membantu dalam menyederhanakan desain rangkaian logika yang kompleks. IC-IC tersebut dirancang secara efisien untuk menghemat waktu saat merancang dan menyusun sistem digital.

IC komersial sangat berguna terutama saat kita membutuhkan konversi data dalam jumlah besar atau dengan kecepatan tinggi, misalnya pada sistem kontrol seperti lift, remote control, komunikasi data, ataupun sistem kendali otomatis lainnya. Dalam kasus tugas ini, encoder digunakan untuk mengubah input dari tombol lantai menjadi format biner, decoder untuk mengendalikan 7 segment, dan multiplexer untuk memilih tampilan tertentu—semuanya menunjukkan bagaimana IC tersebut bisa membuat sistem menjadi lebih modular dan mudah dikembangkan.

Secara umum, IC seperti ini sangat cocok digunakan ketika:

- Desain logika terlalu rumit jika menggunakan gerbang logika dasar saja

- Dibutuhkan efisiensi waktu dalam proses perancangan

- Sistem membutuhkan akurasi dan kecepatan pemrosesan sinyal digital

- Ingin mempermudah debugging dan perawatan karena rangkaian menjadi lebih terstruktur

Pengalaman dari tugas ini menunjukkan bahwa memahami cara kerja IC-IC tersebut dan kapan menggunakannya adalah hal penting dalam dunia teknik elektro dan sistem digital.