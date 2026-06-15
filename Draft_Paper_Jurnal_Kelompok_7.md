Sistem Pendukung Keputusan Penentuan Menu Harian Program Makan Bergizi Gratis Menggunakan Metode Simple Additive Weighting

**Dermawan Syahputra Gulo<sup>1*</sup>, Muhammad Harlan Harahap<sup>2</sup>, Rakha Radityatama<sup>3</sup>**
<sup>1,2,3</sup>Program Studi Sistem Informasi, Universitas (Isi Nama Universitas Anda), Indonesia
*Corresponding author: (Isi Email Anda)

**Abstrak** — Makanan bergizi memainkan peran krusial dalam masa pertumbuhan anak-anak, terutama dalam mendukung kesehatan fisik dan kecerdasan kognitif. Kebijakan Program Makan Bergizi Gratis (MBG) yang dicanangkan oleh pemerintah bertujuan untuk memberikan asupan gizi yang optimal kepada peserta didik. Namun, dalam pelaksanaannya, proses penentuan menu harian yang sehat dan variatif seringkali menjadi tantangan tersendiri bagi pihak penyedia makanan karena banyaknya kombinasi menu dan kebutuhan nilai gizi (kalori, protein, lemak, karbohidrat, dan serat) yang harus dipenuhi secara seimbang. Penelitian ini bertujuan untuk membangun sebuah Sistem Pendukung Keputusan (SPK) yang mampu merekomendasikan menu harian secara otomatis dan tepat sasaran dengan menggunakan metode *Simple Additive Weighting* (SAW). Metode ini dipilih karena kemampuannya dalam melakukan penilaian secara presisi berdasarkan nilai bobot dari masing-masing kriteria gizi. Sistem ini dirancang menggunakan bahasa pemrograman VB .NET Framework 4 dan *database* MySQL dengan menerapkan mekanisme *Create, Read, Update, Delete* (CRUD) untuk manajemen data kriteria dan data menu yang bersumber dari SPPG Kabupaten Deli Serdang, Sumatera Utara. Hasil dari penelitian ini adalah sebuah sistem informasi interaktif yang menghasilkan rekomendasi 5 menu terbaik yang secara otomatis dijadwalkan untuk hari Senin hingga Jumat. Penerapan metode SAW terbukti efektif dalam memberikan perankingan menu makanan sehat secara objektif, sehingga dapat mendukung kesuksesan implementasi Program Makan Bergizi Gratis di sekolah-sekolah.

**Kata kunci**— Makan Bergizi Gratis; MySQL; SAW; Sistem Pendukung Keputusan; VB .NET.

***Title in English: Decision Support System for Determining the Daily Menu of the Free Nutritious Meal Program Using the Simple Additive Weighting Method***

***Abstract*** — *Nutritious food plays a crucial role in the growth period of children, especially in supporting physical health and cognitive intelligence. The Free Nutritious Meal (MBG) Program policy launched by the government aims to provide optimal nutritional intake to students. However, in its implementation, the process of determining a healthy and varied daily menu is often a challenge for food providers due to the many menu combinations and nutritional value needs (calories, protein, fat, carbohydrates, and fiber) that must be met in a balanced manner. This study aims to build a Decision Support System (DSS) capable of automatically and accurately recommending daily menus using the Simple Additive Weighting (SAW) method. This method was chosen because of its ability to make precise assessments based on the weight value of each nutritional criterion. The system is designed using the VB .NET Framework 4 programming language and MySQL database by applying Create, Read, Update, Delete (CRUD) mechanisms for criteria and menu data management sourced from SPPG Deli Serdang Regency, North Sumatra. The result of this research is an interactive information system that produces recommendations for the 5 best menus which are automatically scheduled for Monday to Friday. The application of the SAW method has proven effective in providing objective rankings of healthy food menus, thereby supporting the successful implementation of the Free Nutritious Meal Program in schools.*

***Keywords***— *Decision Support System; Free Nutritious Meals; MySQL; SAW; VB .NET.*

I. PENDAHULUAN

Makanan merupakan salah satu unsur krusial yang secara langsung memengaruhi taraf kesehatan dan kelangsungan hidup manusia, terutama pada masa kanak-kanak. Mengonsumsi makanan dengan gizi seimbang memberikan dampak positif bagi perkembangan fisik, mencegah stunting, dan mendukung kemampuan kognitif anak selama proses pendidikan [1]. Menyadari pentingnya hal ini, pemerintah menginisiasi Program Makan Bergizi Gratis (MBG) sebagai bentuk intervensi pendidikan dan kesehatan yang ditujukan bagi peserta didik. Program MBG diyakini memiliki dampak jangka panjang yang signifikan, baik dari segi peningkatan keberlanjutan pendidikan anak maupun pemberdayaan ekonomi lokal karena pelibatan para penyedia pasokan makanan di daerah [2], [3], [4].
Meskipun program ini memiliki visi yang sangat baik, efektivitas dan tantangan di lapangan kerap bermunculan, salah satunya adalah dalam hal penentuan menu makanan harian [5]. Pemilihan menu makanan tidak bisa dilakukan secara sembarangan, melainkan harus memenuhi standar nutrisi yang cukup seperti takaran kalori, protein, lemak, karbohidrat, dan serat. Kompleksitas dalam memastikan bahwa menu harian tidak hanya sehat tetapi juga bervariasi selama satu minggu penuh (Senin hingga Jumat) seringkali membingungkan pihak Satuan Pelayanan Pemberian Gizi (SPPG). Kesalahan dalam penentuan menu dapat berimbas pada tidak tercapainya target pemenuhan gizi harian anak. Ketidakpahaman serta keterbatasan waktu dalam menganalisis setiap takaran gizi dari berbagai alternatif menu menyebabkan pengambilan keputusan pemilihan menu makanan sehat jarang dilakukan secara sistematis dan optimal [1]. 
Untuk memecahkan masalah tersebut, dibutuhkan sebuah Sistem Pendukung Keputusan (SPK) yang dapat membantu memberikan rekomendasi menu harian terbaik secara komputasional. Sistem Pendukung Keputusan merupakan sistem informasi interaktif yang menyediakan pemodelan dan manipulasi data untuk membantu proses pengambilan keputusan pada situasi yang semiterstruktur [1], [6]. Dalam penelitian ini, proses pengolahan data pemilihan menu menggunakan metode *Simple Additive Weighting* (SAW). Metode SAW dikenal luas dengan istilah metode penjumlahan terbobot yang berfungsi menyeleksi alternatif terbaik (menu makanan) dari sejumlah kriteria gizi yang telah ditetapkan [1], [7], [8]. Metode ini memiliki keunggulan dalam memberikan penilaian secara objektif, sistematis, dan tepat sasaran karena dilandasi oleh normalisasi matriks dan preferensi bobot kriteria [9], [10]. Penelitian sebelumnya telah membuktikan bahwa metode SAW sangat efektif saat diaplikasikan pada kasus penentuan menu makanan sehat, penentuan status gizi, hingga pemilihan pemasok bahan makanan [1], [11], [12].
Sistem rekomendasi penentuan menu MBG ini dirancang berbasis aplikasi *desktop* menggunakan bahasa pemrograman *Visual Basic* .NET (VB .NET) Framework 4 dan basis data relasional MySQL. Penerapan sistem *Create, Read, Update, Delete* (CRUD) pada aplikasi memungkinkan pihak pengguna (administrator) untuk mengelola data alternatif menu dan kriteria gizi secara dinamis. Tujuan akhir dari penelitian ini adalah menyajikan suatu SPK terkomputerisasi yang sanggup mengotomatisasi seleksi 5 menu makanan paling bergizi, lalu menjadwalkannya untuk didistribusikan setiap hari mulai dari Senin sampai Jumat secara efektif di SPPG Kabupaten Deli Serdang, Sumatera Utara.

II. METODE PENELITIAN

*A. Objek dan Data Penelitian*

Penelitian ini menggunakan sampel data 15 menu makanan yang dikumpulkan dari standar pemenuhan gizi Satuan Pelayanan Pemberian Gizi (SPPG) wilayah Kabupaten Deli Serdang, Provinsi Sumatera Utara. Terdapat 5 kriteria utama (*C*) yang menjadi tolak ukur dalam menentukan kelayakan sebuah menu makanan bergizi gratis, yaitu:
1. Kalori (C1) - *Benefit*
2. Protein (C2) - *Benefit*
3. Lemak (C3) - *Cost* (Diasumsikan perlunya pembatasan lemak berlebih)
4. Karbohidrat (C4) - *Benefit*
5. Serat (C5) - *Benefit*

Setiap kriteria memiliki bobot tingkat kepentingan (*W*) yang ditentukan berdasarkan skala prioritas gizi anak. Total bobot dari keseluruhan kriteria akan bernilai sama dengan 1 (satu) atau 100%.

*B. Konsep Simple Additive Weighting (SAW)*

Metode *Simple Additive Weighting* (SAW) sering juga dikenal dengan istilah metode penjumlahan terbobot. Konsep dasar metode SAW adalah mencari penjumlahan terbobot dari rating kinerja pada setiap alternatif di semua atribut kriteria [1], [8]. SAW membutuhkan proses normalisasi matriks keputusan (*X*) ke suatu skala yang dapat diperbandingkan dengan semua *rating* alternatif yang ada. 

Menurut referensi utama [1], rumus untuk melakukan normalisasi dalam metode SAW adalah sebagai berikut:

*(Disini masukkan *Equation 1* / Rumus Normalisasi SAW dari Word)*
1. Jika *j* adalah atribut keuntungan (*benefit*):
   r<sub>ij</sub> = X<sub>ij</sub> / Max<sub>i</sub>(X<sub>ij</sub>)

2. Jika *j* adalah atribut biaya (*cost*):
   r<sub>ij</sub> = Min<sub>i</sub>(X<sub>ij</sub>) / X<sub>ij</sub>

Keterangan:
r<sub>ij</sub> = *Rating* kinerja ternormalisasi dari alternatif *A<sub>i</sub>* pada atribut *C<sub>j</sub>*.
Max<sub>i</sub>(X<sub>ij</sub>) = Nilai maksimum dari setiap kolom kriteria.
Min<sub>i</sub>(X<sub>ij</sub>) = Nilai minimum dari setiap kolom kriteria.
X<sub>ij</sub> = Nilai baris ke-*i* dan kolom ke-*j* pada matriks awal.

Setelah didapatkan matriks ternormalisasi (*R*), proses selanjutnya adalah tahap perangkingan atau penentuan nilai preferensi (*V<sub>i</sub>*) untuk setiap alternatif. Nilai *V<sub>i</sub>* dihitung menggunakan rumus:

*(Disini masukkan *Equation 2* / Rumus Preferensi Vi dari Word)*
V<sub>i</sub> = Σ (W<sub>j</sub> × r<sub>ij</sub>)

Keterangan:
V<sub>i</sub> = Nilai preferensi akhir dari alternatif (menu makanan) ke-*i*.
W<sub>j</sub> = Bobot kriteria yang telah ditentukan pada atribut ke-*j*.
r<sub>ij</sub> = Matriks yang telah dinormalisasi.

*C. Perancangan Sistem dan Perangkat Lunak*

Sistem dibangun dengan menggunakan aplikasi *Microsoft Visual Studio* dengan basis bahasa VB .NET Framework 4. Untuk pengolahan dan penyimpanan data digunakan basis data *MySQL* melalui perantara *XAMPP/PHPMyAdmin*. Arsitektur sistem mendukung fungsionalitas CRUD secara penuh untuk tabel menu, tabel kriteria, dan tabel hasil penjadwalan.

III. HASIL DAN PEMBAHASAN

*A. Hasil Implementasi Sistem*

Aplikasi SPK Menu Makan Bergizi Gratis dirancang untuk memiliki antarmuka yang ramah pengguna (*user-friendly*). Saat sistem dijalankan, pengguna diharuskan masuk melalui Form Login untuk menjamin keamanan akses data. Setelah autentikasi berhasil, pengguna akan diarahkan ke *Form Menu Utama*.

*(Sisipkan Gambar 1 di sini)*
**Gambar 1. Tampilan Menu Utama Aplikasi SPK MBG**
*(Keterangan untuk penulis: Silakan paste screenshot FormMenuUtama Anda yang berwarna hijau tua di sini)*

Pada aplikasi ini, pengguna dapat mengelola data kriteria gizi beserta bobotnya pada *Form Kriteria*, serta mengelola daftar menu di *Form Menu*. Modul perhitungan utama terdapat pada *Form Perhitungan SAW*, di mana seluruh algoritma SAW diimplementasikan untuk memberikan hasil rekomendasi secara sistematis.

*(Sisipkan Gambar 2 di sini)*
**Gambar 2. Tampilan Hasil Perhitungan SAW**
*(Keterangan untuk penulis: Silakan paste screenshot FormPerhitunganSAW saat tabel terisi angka di sini)*

*B. Perhitungan Metode SAW*

Untuk memvalidasi kesesuaian logika program, dilakukan pengujian perhitungan manual terhadap beberapa sampel menu makanan dari *database*. Tabel 1 berikut menunjukkan contoh *rating* kecocokan (*Matriks X*) dari 5 alternatif menu (M1 sampai M5) terhadap 5 kriteria gizi (C1-C5).

**Tabel 1**
*CONTOH MATRIKS KEPUTUSAN AWAL (X)*
| Alternatif | C1 (Kalori) | C2 (Protein) | C3 (Lemak) | C4 (Karbo) | C5 (Serat) |
|------------|-------------|--------------|------------|------------|------------|
| M1 (Menu A)| 400         | 15           | 10         | 50         | 8          |
| M2 (Menu B)| 350         | 20           | 8          | 45         | 10         |
| M3 (Menu C)| 450         | 12           | 15         | 60         | 6          |
| M4 (Menu D)| 380         | 18           | 12         | 55         | 9          |
| M5 (Menu E)| 420         | 16           | 11         | 48         | 7          |

Setelah nilai *rating* terbentuk, tahap selanjutnya adalah membentuk matriks ternormalisasi (*R*) berdasarkan sifat atribut (*benefit* atau *cost*). Diasumsikan C1, C2, C4, dan C5 adalah *benefit* (dicari nilai maksimal), sedangkan C3 adalah *cost* (dicari nilai minimal). Sesuai dengan rumus normalisasi, hasil matriks ternormalisasi disajikan pada Tabel 2.

**Tabel 2**
*CONTOH MATRIKS TERNORMALISASI (R)*
| Alternatif | C1 | C2 | C3 | C4 | C5 |
|------------|----|----|----|----|----|
| M1 | 0.88 | 0.75 | 0.80 | 0.83 | 0.80 |
| M2 | 0.77 | 1.00 | 1.00 | 0.75 | 1.00 |
| M3 | 1.00 | 0.60 | 0.53 | 1.00 | 0.60 |
| M4 | 0.84 | 0.90 | 0.66 | 0.91 | 0.90 |
| M5 | 0.93 | 0.80 | 0.72 | 0.80 | 0.70 |

Tahapan akhir adalah mengalikan setiap sel matriks *R* dengan bobot kriteria *W* untuk mendapatkan nilai *V* (Perangkingan). Alternatif dengan nilai *V* tertinggi otomatis menjadi rekomendasi terbaik. 

*C. Hasil Penjadwalan Menu Mingguan*

Sistem memiliki fitur unggulan berupa penentuan jadwal menu untuk periode satu minggu pembelajaran (Senin hingga Jumat). Untuk menghindari repetisi menu, algoritma yang tertanam pada *Form Perhitungan SAW* menerapkan logika pengecualian (*exclusion*), di mana menu yang telah terpilih pada hari Senin tidak akan disertakan pada seleksi hari Selasa, dan seterusnya.

*(Sisipkan Gambar 3 di sini)*
**Gambar 3. Laporan Hasil Ranking dan Penjadwalan Harian**
*(Keterangan untuk penulis: Silakan paste screenshot FormHasilRanking di sini)*

Berdasarkan laporan hasil ranking yang diekspor dari aplikasi, didapatkan 5 menu teratas yang saling berbeda untuk dialokasikan pada setiap harinya. Keputusan ini mampu menyelesaikan dilema pihak SPPG dalam menyajikan makanan bergizi yang dinamis tanpa mengurangi pemenuhan batas kalori dan nutrisi esensial bagi anak.

IV. SIMPULAN

Berdasarkan hasil rancang bangun aplikasi dan analisis perhitungan terhadap metode *Simple Additive Weighting* (SAW), dapat disimpulkan beberapa hal sebagai berikut:
Pertama, implementasi metode SAW pada Sistem Pendukung Keputusan sukses membantu proses perankingan kelayakan menu harian Program Makan Bergizi Gratis (MBG) secara cepat dan akurat. Sistem dapat membedakan nilai gizi dengan tingkat kriteria yang kompleks menjadi matriks yang terkuantifikasi. 
Kedua, penerapan arsitektur pemrograman menggunakan VB .NET dan basis data MySQL terbukti stabil dalam menangani proses CRUD data referensi SPPG serta menampilkan laporan penjadwalan. Logika otomatisasi eksklusi pada pengalokasian menu berhasil menjamin variasi sajian makanan harian bagi siswa tanpa ada pengulangan menu pada hari yang berbeda dalam satu minggu. Keputusan sistem berbasis SAW ini diharapkan mampu memberikan dampak masif terhadap keberlanjutan program perbaikan gizi dan pendidikan di wilayah terkait.

UCAPAN TERIMA KASIH

Penulis mengucapkan terima kasih yang sebesar-besarnya kepada dosen pengampu mata kuliah Pemrograman Visual yang telah memberikan bimbingan teknis selama proses pengembangan sistem. Kami juga menyampaikan apresiasi kepada pihak Satuan Pelayanan Pemberian Gizi (SPPG) Kabupaten Deli Serdang, Sumatera Utara, atas transparansi data standar nutrisi menu makanan yang dipergunakan sebagai basis pengujian dalam penelitian ini.

DAFTAR PUSTAKA

[1] S. Wulandari and S. W. Yudha, “Sistem Pendukung Keputusan Menentukan Menu Makanan Sehat Menggunakan Metode Simple Additive Weighting,” *Jurnal Nasional Teknologi Komputer (JNaSTek)*, vol. 1, no. 1, pp. 37–44, 2021.
[2] U. Agustini and S. Mulyani, “Efektivitas dan Tantangan Kebijakan Program Makan Bergizi Gratis sebagai Intervensi Pendidikan di Indonesia,” *Jurnal Kiprah Pendidikan*, vol. 4, no. 3, pp. 362–368, 2025.
[3] Y. S. Widyasari, A. Larasati, and Y. W. Alam, “Evaluasi Kebijakan Makan Bergizi Gratis di Sekolah Dasar: Implikasi terhadap Kesehatan Anak dan Pemberdayaan Ekonomi Lokal,” *Innovative: Journal of Social Science Research*, vol. 5, no. 4, pp. 1727–1736, 2025.
[4] M. Basit and H. Ramadani, “Analisis Implementasi Program Makan Bergizi Gratis terhadap Perkembangan Ekonomi,” *Journal of Education and Development Research (JOEDER)*, vol. 1, no. 2, pp. 49–54, 2025.
[5] R. Qomarrullah, S. Suratni, and M. Sawir, “Dampak Jangka Panjang Program Makan Bergizi Gratis terhadap Kesehatan dan Keberlanjutan Pendidikan,” *Indonesian Journal of Intellectual Publication*, vol. 5, no. 2, pp. 130–137, 2025.
[6] R. Setiawan and S. Hartati, “Analysis of Decision Support System in Determining the Nutritional Status of Toddlers Using Simple Additive Weighting,” *CommIT Journal*, vol. 14, no. 1, 2020.
[7] D. Y. Niska, “Sistem Pendukung Keputusan untuk Menentukan Menu Makanan Sehat dengan Metode Simple Additive Weighting,” *Jurnal Teknik dan Informatika*, vol. 5, no. 2, pp. 1–5, 2018.
[8] R. Putra, B. Prasetyo, and Haryanto, “Penerapan Metode Simple Additive Weighting pada Aplikasi Penentuan Pemasok Bahan Makanan dan Minuman,” *Jurnal Teknologi Informatika dan Komputer MH. Thamrin*, vol. 9, no. 1, 2023.
[9] L. Dwi Prasanti and D. Utomo, “Perancangan Sistem Pendukung Keputusan Rekomendasi Menu Makanan pada Penderita Diabetes Mellitus Menggunakan Metode Simple Additive Weighting,” *Jurnal Kecerdasan Buatan dan Teknologi Informasi (JKBTI)*, vol. 3, no. 1, pp. 11–16, 2024.
[10] A. Fadillah, S. Nugroho, and A. Wibowo, “Penerapan Algoritma Decision Making MCDM dan SAW Berbasis User-Personalize Profile dengan Fitur Food Preference,” *Jurnal Tekno Kompak*, 2024.
[11] J. R. Plaza, Haliq, and C. Irawan, “Sistem Pendukung Keputusan Balita Teridentifikasi Stunting Menggunakan Metode SAW,” *Jurnal Informatika*, vol. 22, no. 1, 2022.
[12] A. Nugroho and M. Kautsar, “Sistem Informasi dalam Penentuan Status Gizi Balita dengan Memanfaatkan Metode Simple Additive Weighting,” *JIKO (Jurnal Informatika dan Komputer)*, 2023.
