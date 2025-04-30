# <span style="color:#FF5733; background-color:#FFFFCC; padding:5px; border-radius:10px;">🤖 Case Study - 9 (Register & Counter) 🤖</span>

<div style="background-color:#E6F7F; padding:15px; border-radius:10px; border:2px dashed #66CCFF;">
<p style="font-size:18px;">
Nama: <span style="color:#9966CC;">Elias Rechoum</span><br>
NPM: <span style="color:#9966CC;">2406354045</span><br>
Kelompok: <span style="color:#9966CC;">A13</span><br>
Rekan Kerja: <span style="color:#9966CC;">Altaf Farzana</span>
</p>
</div>

## <span style="color:#FF9933; background-color:#FFF0E6; padding:5px; border-radius:5px;">🔌 Rangkaian (50 Poin) 🔌</span>

<div style="background-color:#FFEECC; border-radius:px; border-left:5px solid #FFAA33;">
<p style="font-style:italic; color:#885500;">Selamat tinggal, kawan lama! 🪦👋😭😭😭😭😭😭😭😭😭😭😭😭😭😭😭😭😭😭😭😭😭😭😭😭😭😭😭😭</p>
</div>

![image](https://hackmd.io/_uploads/BkeQXPIzJe.png)

<div style="background-color:#; padding:15px; border-radius:10px;">
<p>Kamu telah berhasil menolong Mister Kim dalam menemukan pasangan sejatinya. Setelah lulus kuliah, kalian berpisah jalan dan menghidupi kehidupan masing-masing, dimana kamu melanjutkan karir di lapangan teknikal, sedangkan Mister Kim berpindah ke bidang ekonomi. Kini, mereka hidup dengan tenang dan bahagia, namun bantuanmu akan selalu diingat.</p>

<p>Selang beberapa dekade setelah kalian terakhir kali bertemu, kamu memanggil Mister Kim lagi. Telah tua, ia sadar bahwa <span style="color:red; font-weight:bold">waktunya sudah dekat</span>. Ternyata, tim medis menebak bahwa Mister Kim hanya memiliki hingga 7 bulan tersisa dan menderita penyakit kanker PR4K41PR06 stadium 69420, sebuah penyakit misterius yang baru muncul awal tahun 2025 ini 💀.</p>

<p>Sebagai permintaan terakhirnya, Mister Kim memintamu untuk membuat sebuah "kenang-kenangan" terakhir dalam bentuk sebuah counter. Ia memintamu untuk menggunakan <span style="color:blue; font-weight:bold">komponen-komponen sisa</span> yang kalian gunakan dahulu, yakni D Flip-Flop sederhana. Bisakah kamu memenuhi permintaan terakhir ini? 🥺</p>
</div>

### <span style="color:#6633CC; background-color:#F0E6FF; padding:5px; border-radius:5px;">⚙️ Komponen Sistem ⚙️</span>

<div style="background-color:#F; padding:15px; border-radius:10px; border:1px solid #CCCCFF;">
<ol>
<li style="margin-bottom:15px;">
  <span style="color:#3366FF; font-weight:bold; font-size:18px;">Counter</span>
  <ul style="list-style-type:none;">
    <li>🔸 Counter menggunakan D Flip-Flop</li>
    <li>🔸 Counter berukuran 3-bit, sehingga bisa menampilkan angka dari 7 hingga 0</li>
    <li>🔸 Counter bersifat <span style="color:#FF3366; font-style:italic;">asynchronous</span></li>
    <li>🔸 Jenis counter adalah <span style="color:#FF3366; font-weight:bold;">down counter</span></li>
    <li>🔸 Siklus counter adalah sebagai berikut: 7 → 6 → 5 → 4 → 3 → 2 → 1 → 0 → 7 → ... (Mengulang)</li>
  </ul>
</li>
<li>
  <span style="color:#3366FF; font-weight:bold; font-size:18px;">Output</span>
  <ul style="list-style-type:none;">
    <li>📊 Output direpresentasikan sebagai angka pada 7 segment</li>
    <li>📊 Ketiga LED pertama menggambarkan nilai dari tiap bit counter</li>
    <li>📊 Saat counter mencapai 0, sebuah LED tambahan akan menyala 💡</li>
  </ul>
</li>
</ol>
</div>

<div style="background-color:#FFCCC; padding:15px; border-radius:10px; margin-top:20px; text-align:center; font-weight:bold;">
⚠️ Buatlah rangkaian asli dari instruksi yang diberikan dan sertakan foto sekaligus beberapa contoh kondisi output rangkaian! (Minimal 2) ⚠️
</div>


![alt text](https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%209/image-5.png)
![alt text](https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%209/image-6.png)
![alt text](https://raw.githubusercontent.com/c0ldlasagna/DSD/refs/heads/master/Week%209/image-7.png)



## <span style="color:#009900; background-color:#E6FFE6; padding:5px; border-radius:5px;">🧠 Analisis dan Kesimpulan (50 Poin) 🧠</span>

<div style="background-color:#F0F8FF; padding:15px; border-radius:10px; margin-bottom:15px;">
<h3 style="color:#3366CC;">1. Jelaskan cara kalian mengimplementasikan counter kali ini (Secara praktis)! (15 poin) 🛠️</h3>
</div>

Rangkaian yang ditampilkan adalah implementasi dari sebuah counter 3-bit menggunakan rangkaian flip-flop JK (IC 74LS76) yang disusun secara berurutan. Tiga buah flip-flop digunakan untuk membentuk hitungan biner 3-bit (dari 000 sampai 111). Input J dan K diberikan logic high supaya output terus toggle. Clock diberikan pada flip-flop pertama (U1:A), dan output Q dari flip-flop pertama digunakan sebagai clock untuk flip-flop kedua (U1:B), dan begitu pula untuk flip-flop ketiga (U2:A). Dengan cara ini, flip-flop bekerja secara ripple (asynchronous). Ketiga output Q dari flip-flop ini disambungkan ke input decoder 7448 (U3), yang berfungsi untuk mengubah nilai biner dari counter menjadi tampilan desimal pada 7-segment display.

Selain itu, terdapat gerbang NOR 3-input (U4) yang digunakan untuk mendeteksi kondisi ketika semua output Q dari ketiga flip-flop berada dalam keadaan logika rendah (000). Dalam kondisi ini, output dari gerbang NOR akan menjadi logika tinggi, yang kemudian digunakan untuk menyalakan LED (D1). LED ini akan menyala hanya ketika counter menunjukkan angka 0.

<div style="background-color:#F0F8FF; padding:15px; border-radius:10px; margin-bottom:15px;">
<h3 style="color:#3366CC;">2. Sekarang, coba jelaskan cara asynchronous down counter bekerja agar bisa memiliki siklus mundur! Anda bisa menambahkan gambar wave diagram untuk memperjelas. (15 poin) 📉</h3>
</div>

Jawaban : Asynchronous down counter adalah counter yang menghitung mundur (misalnya dari 7 ke 0 dalam sistem 3-bit). Disebut asynchronous karena tidak semua flip-flop dikendalikan oleh clock yang sama — hanya flip-flop pertama yang menerima sinyal clock langsung, sementara flip-flop berikutnya dipicu oleh output dari flip-flop sebelumnya.

Untuk membuatnya menghitung mundur, perbedaan utamanya terletak pada bagaimana clock antar flip-flop dihubungkan. Pada counter up, biasanya output Q dari flip-flop digunakan untuk merepresentasi bit yang dihitung. Namun, pada counter down, yang digunakan adalah output Q̅. Ini karena ketika Q̅ berubah dari 1 ke 0, dan membuat counternya menurun.

Contohnya, misalnya kita mulai dari 111 (dalam 3-bit):

1. Flip-flop pertama (LSB) akan mendapatkan pulsa clock langsung dan akan mengubah status dari 1 ke 0.

2. Perubahan dari Q (dari 0 ke 1) kemudian memicu flip-flop kedua (bit tengah), dan proses ini berlanjut.

Siklus ini berlanjut sampai mencapai 000, dan kemudian kembali ke 111, membentuk siklus mundur.

Dengan mengatur J dan K dari setiap flip-flop ke logika tinggi (1), kita memastikan flip-flop bekerja dalam mode toggle, yaitu akan berganti keadaan setiap kali mendapat pulse clock.

<div style="background-color:#F0F8FF; padding:15px; border-radius:10px; margin-bottom:15px;">
<h3 style="color:#3366CC;">3. Jika kita ingin mengubah rangkaian down counter ini menjadi up counter, apa saja yang harus dimodifikasi? (10 poin) 📈</h3>
</div>

Jawaban : Untuk mengubah rangkaian asynchronous down counter menjadi up counter, hal utama yang perlu dimodifikasi adalah koneksi output pada masing-masing flip-flop. Dalam rangkaian down counter, output Q̅ dari flip-flop digunakan sebagai output.  Namun, untuk mengubahnya menjadi up counter, output untuk bit buat hitung harus diganti ke Q, supaya counter mulai pada state 000.

<div style="background-color:#F0F8FF; padding:15px; border-radius:10px; margin-bottom:15px;">
<h3 style="color:#3366CC;">4. Berikanlah kesimpulan terhadap seluruh rangkaian praktikum modul 9 ini (10 poin) 📝</h3>
</div>

- Praktikum ini berhasil menunjukkan cara kerja asynchronous counter dengan menggunakan JK flip-flop sebagai dasar rangkaian.

- Rangkaian dirancang sebagai down counter, yang menghitung mundur dari nilai biner tertinggi ke nol secara bertahap.

- Output dari counter ditampilkan menggunakan IC 7448 decoder yang terhubung ke seven-segment display, sehingga mempermudah pemantauan nilai biner secara visual.

- Sebuah gerbang NOR digunakan untuk mendeteksi kondisi tertentu, seperti 000, dan menyalakan LED sebagai indikator bahwa counter telah mencapai nilai akhir.

- Arah perhitungan ditentukan oleh bit output pada flip-flop:

  - Down counter menggunakan output Q̅ sebagai bit output.

  - Untuk mengubahnya menjadi up counter, cukup mengganti koneksi output ke Q.

- Semua flip-flop diatur agar input J dan K selalu HIGH (1), sehingga beroperasi dalam mode toggle.

- Praktikum ini memperkuat pemahaman tentang konsep dasar sistem counter, hubungan antar flip-flop, serta penerapan logika digital dalam rangkaian nyata.

- Secara keseluruhan, praktikum ini memberikan pengalaman langsung yang sangat bermanfaat dalam memahami teori dan implementasi rangkaian counter digital.

<div style="background-color:#FFE6FF; padding:15px; border-radius:10px; text-align:center; margin-top:30px; font-style:italic; color:#990099;">
<p style="font-size:18px;">-- Sampai berjumpa lagi nanti! 👋 --</p>
<p>
  <span style="font-size:24px;">
    🌟 - Aslab DSD 🌟
  </span>
</p>
</div>