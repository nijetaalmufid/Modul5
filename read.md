1. Pengertian Bootstrap

Bootstrap adalah framework front-end open source yang berisi kumpulan CSS, JavaScript, dan komponen siap pakai untuk membangun tampilan website yang responsif. Bootstrap awalnya dikembangkan oleh tim Twitter, lalu dirilis sebagai proyek terbuka.

Kegunaannya:

Mempercepat pengembangan, karena komponen seperti navbar, card, tombol, form, dan modal sudah tersedia dan tinggal dipakai lewat class.
Tampilan responsif, karena Bootstrap menerapkan pendekatan mobile-first sehingga halaman otomatis menyesuaikan ukuran layar.
Tampilan konsisten di berbagai browser dan perangkat.
Mengurangi penulisan CSS manual, karena pengaturan warna, jarak, ukuran, dan tata letak cukup memakai class utilitas.

2. Cara Memasang Bootstrap
CDN (Content Delivery Network). Menambahkan tag <link> untuk CSS dan <script> untuk JS langsung dari server CDN. Cara ini paling praktis dan tidak perlu mengunduh file.
Mengunduh file compiled (lokal). Mengunduh file CSS dan JS Bootstrap dari situs resminya, menyimpannya di folder project, lalu menautkannya dengan <link> dan <script>. Cara ini tetap bisa dipakai tanpa internet.
Package manager. Memasang lewat npm, yarn, atau pnpm, misalnya npm install bootstrap@5.3.8. Cocok untuk project berbasis build tool atau framework modern.
Mengompilasi dari source Sass. Memakai file Sass sumber Bootstrap agar variabel, warna, dan tema bisa dikustomisasi sebelum dikompilasi menjadi CSS.
Package manager lain seperti Composer (PHP) atau NuGet (.NET), sesuai bahasa dan platform project.

3. Grid dan Breakpoint

Class grid. Bootstrap memakai sistem grid 12 kolom dengan struktur bertingkat:

container atau container-fluid sebagai pembungkus. container punya lebar maksimum tetap, sedangkan container-fluid selalu selebar layar.
row sebagai baris yang membungkus kolom.
col, col-6, col-md-4, dan sejenisnya sebagai kolom. Angkanya menunjukkan berapa dari 12 kolom yang dipakai, sehingga jumlah dalam satu baris idealnya 12. Contoh: col-6 dan col-6 membagi layar menjadi dua bagian sama besar.
Breakpoint adalah batas lebar layar tempat tata letak berubah. Bootstrap menyediakan enam tingkat:

Breakpoint	        Awalan class	Lebar layar
Extra small         tanpa awalan	kurang dari 576px
Small	            sm	            ≥576px
Medium	            md	            ≥768px
Large	            lg	            ≥992px
Extra large	        xl	            ≥1200px
Extra extra large	xxl	            ≥1400px

4. Class Bootstrap (minimal lima)
Class	            Kegunaan
container	        Pembungkus konten yang lebarnya terpusat dan menyesuaikan breakpoint
btn btn-primary	    Membuat tombol dengan gaya dan warna biru (primary)
card	            Membuat kotak konten dengan bingkai, latar, dan padding rapi
navbar	            Membuat bilah navigasi di bagian atas halaman
form-control	    Memberi gaya pada input form agar seragam dan selebar wadahnya
text-center	        Menjadikan teks rata tengah
mb-3 / p-3	        Utilitas spacing: mb-3 margin bawah, p-3 padding di semua sisi
shadow	            Memberi bayangan pada elemen
d-flex	            Mengubah elemen menjadi flex container untuk mengatur tata letak
bg-success	        Memberi warna latar hijau

5. Gambar Responsif

Cara paling sederhana di Bootstrap adalah menambahkan class img-fluid pada tag gambar:

html
<img src="foto.jpg" class="img-fluid" alt="Deskripsi gambar">

Class ini menerapkan max-width: 100% dan height: auto. Artinya gambar tidak akan melebihi lebar wadahnya dan akan mengecil mengikuti ukuran layar, sementara proporsi tinggi dan lebarnya tetap terjaga.

Cara pendukung lainnya:

<picture> dan srcset untuk memuat file gambar berukuran berbeda sesuai lebar layar.
object-fit-cover (di Bootstrap 5.3) agar gambar mengisi area tanpa terdistorsi.
CSS manual dengan max-width: 100%; height: auto; pada gambar.