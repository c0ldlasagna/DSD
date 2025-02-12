# Case Study Modul 1 : Pengenalan Dasar Rangkaian Digital

Nama : Kafu [Ganti dengan nama lengkap anda]
NPM    : 2401234567 [Ganti dengan NPM anda]

Pada tugas pendahuluan, anda telah membuat rangkaian sederhana untuk menyalakan LED. Pada Case Study, LED akan dinyalakan menggunakan IC 7408 berdasarkan datasheet. Untuk itu, ikuti lah langkah-langkah dibawah ini.

### Praktik

1. Buatlah rangkaian baru pada Tinkercad, tambahkan breadboard, baterai 9V, LED, dan IC 7408 pada breadboard. Tidak perlu dihubungkan terlebih dahulu.
2. Bukalah datasheet dari IC 7408. Anda dapat menggunakan datasheet pada link berikut : https://www.farnell.com/datasheets/59359.pdf
3. Dari bagian General Description, sebutkan apa kegunaan dari IC 7408! (5 poin)
   Jawaban singkat: _________________________
4. Hubungkan baterai 9v pada bagian power strip dari breadboard.
5. Dari bagian Connection Diagram, jelaskan lokasi pin VCC dan GND, apa yang seharusnya dihubungkan pada VCC dan GND? (5 poin)

   Jawaban singkat: _________________________
6. Hubungkan VCC dan GND dari power strip breadboard sesuai dengan jawaban anda sebelumnya.
7. Letakkan IC pada bagian tengah breadboard.

   ![1739074112870](https://raw.githubusercontent.com/lebit-L1X/FileDigilab/refs/heads/main/Screenshot%202025-02-09%20110717.png)
8. Letakkan LED pada breadboard, dan hubungkan Cathode dari LED dengan resistor menuju ground seperti yang telah dikerjakan pada Tugas Pendahuluan.
9. Dari bagian connection diagram, gunakan AND gate pertama (A1, B1, dan Y1) pada Tinkercad.
10. Hubungkan VCC dari dua buah port (lubang) power strip breadboard menuju pin A1 dan B1 pada IC 7408 (1A dan 1B pada Tinkercad)
11. Hubungkan output dari AND gate yaitu pin Y1 (Output 1 pada Tinkercad) pada bagian Anode dari LED.
12. Pada datasheet, perhatikan bagian function table, dalam hal ini H berarti High Logic Level (dihubungkan dengan VCC) dan L berarti Low Logic Level (Dihubungkan dengan GND), berdasarkan tabel tersebut, apa output seharusnya jika pada input IC dihubungkan High dengan High? (5 poin)

    Jawaban singkat:__________________________
13. Run Simulation Tinkercad dan perhatikan LED, bila LED menyala maka ia dalam kondisi High, sedangkan bila ia padam, maka ia dalam kondisi Low. Pastikan output sudah sesuai dengan function table sebelum lanjut ke nomor selanjutnya.
14. Namun, perhatikan bahwa IC akan meledak atau terbakar ketika simulasi dijalankan. Buka halaman kedua dari datasheet anda, lalu perhatikan tabel **Recommended Operating Conditions**. Berdasarkan tabel tersebut, berapakah tegangan operasional yang disarankan untuk VCC? (5 poin)

    Jawaban singkat:___________________________
15. Dapat diamati bahwa baterai yang memiliki tegangan sebesar 9V tidak sesuai untuk IC yang digunakan, maka ubahlah baterai tersebut dengan Power Supply yang digunakan pada Tugas Pendahuluan.
16. Setelah melakukan perubahan, kembali Run Simulation. Pastikan bahwa kondisi LED dan IC sudah sesuai dan tidak meledak.
17. Selanjutnya, anda akan melakukan pengujian truth table (function table) IC 7408 berdasarkan datasheet. Untuk memudahkan prosesnya, anda akan menggunakan Dip Switch.
18. Dip switch bertindak sebagai saklar yang dapat dengan mudah mengubah nilai High atau Low dari input tanpa harus mengganti hubungan kabel. Contoh penggunaannya dapat dilihat digambar berikut.
    ![1739074488469](https://raw.githubusercontent.com/lebit-L1X/FileDigilab/refs/heads/main/Screenshot%202025-02-09%20111443.png)
19. Hubungkan dipswitch pada rangkaian anda, coba melakukan Run Simulation lalu nyalakan pin 1 dan 2 pada dip switch, pastikan bahwa output sesuai dengan rangkaian pada nomor 16.
20. Jika sudah sesuai, Lengkapilah tabel berikut ini. Apakah hasil akhir rangkaian anda sesuai dengan function table pada datasheet? (10 poin)


    | Inputs  | Output Datasheet | Output Sebenarnya | Screenshot Output |
    | ------- | ---------------- | ----------------- | ----------------- |
    | LL (00) | L                | ___               |                   |
    | LH (01) | L                | ___               |                   |
    | HL (10) | L                | ___               |                   |
    | HH (11) | H                | ___               |                   |

### Analisis

1. Berikan analisis berupa paragraf yang menjelaskan kegiatan dan aplikasi teori dan modul anda pada Case Study ini, sertakan screenshot dan link rangkaian Tinkercad anda (30 poin).

   Jawaban:
   Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
2. Perhatikan penggunaan LED pada rangkaian anda, jelaskan apa yang terjadi ketika posisi Anode dan Katode dari LED di balikkan! (dapat anda demonstrasikan dengan mencantumkan SS rangkaian) (10 poin)
   Jawaban:
   Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
3. Pada LED fisik di dunia nyata, bagiamana anda membedakan posisi dari Anode dan Katode LED? (10 poin)
   Jawaban:
   Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
4. Perhatikan posisi Pin IC pada rangkaian anda, apakah dampak jika posisi pin tertukar pada IC dan bagaimana anda membedakan posisi dari pin IC pada IC fisik? Anda dapat menggunakan gambar berikut sebagai referensi (20 poin)
   ![](https://raw.githubusercontent.com/lebit-L1X/FileDigilab/refs/heads/main/Screenshot%202025-02-09%20114500.png)

   Jawaban:
   Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages.
5. Berikan kesimpulan praktikum modul ini dalam bentuk poin-poin, untuk jawaban yang maksimal, jelaskan kembali apa saja informasi yang dapat anda peroleh dari datasheet, serta jelaskan hal baru yang anda pelajari dari praktikum hari ini! (10 poin)

   - Kesimpulan 1
   - Kesimpulan 2
   - Kesimpulan 3 ... Dst
