Checklist Implementasi TUgas 7

Program Flutter baru dengan tema E-Commerce: Program ini diinisialisasi sebagai aplikasi Flutter yang bertema e-commerce sederhana dengan judul "Aura Artisan."

Tombol dengan Ikon dan Teks: Tiga tombol telah dibuat dalam bentuk ItemHomepage yang berisi ikon dan teks:

Lihat Daftar Produk
Tambah Produk
Logout

Warna Berbeda untuk Setiap Tombol: Setiap tombol memiliki warna yang berbeda. Ini diatur melalui atribut color pada setiap instance ItemHomepage, sehingga tombol "Lihat Produk" berwarna biru, "Tambah Produk" berwarna hijau, dan "Logout" berwarna merah.

Snackbar: Ketika tombol ditekan, sebuah Snackbar akan muncul dengan pesan yang sesuai:

Untuk tombol "Lihat Produk", pesan Kamu telah menekan tombol Lihat Daftar Produk.
Untuk tombol "Tambah Produk", pesan Kamu telah menekan tombol Tambah Produk.
Untuk tombol "Logout", pesan Kamu telah menekan tombol Logout.

Jawaban pada README.md: Beberapa pertanyaan dapat dijawab sebagai berikut:

Apa yang dimaksud dengan stateless widget dan stateful widget, dan perbedaannya?

Stateless widget adalah widget yang tidak dapat berubah setelah dibuat, cocok untuk UI yang statis. Stateful widget adalah widget yang memiliki status dan dapat diperbarui saat aplikasi berjalan.

Widget yang digunakan pada proyek ini dan fungsinya:

Scaffold: Struktur dasar halaman, berisi elemen utama seperti AppBar, Drawer, dan Body.
AppBar: Header aplikasi yang menampilkan judul.
GridView.count: Menampilkan tombol dalam tata letak grid.
Card: Menampilkan informasi NPM, Nama, dan Kelas.
Material, InkWell: Menambahkan efek interaktif pada tombol.
SnackBar: Menampilkan pesan notifikasi saat tombol ditekan.

Fungsi dari setState():

Menggunakan setState() memperbarui tampilan widget ketika variabel terkait berubah.

Perbedaan antara const dan final:

const: Menginisialisasi variabel sebagai konstanta yang tetap di compile-time.
final: Menginisialisasi variabel hanya sekali pada runtime, tetapi nilainya tidak bisa diubah.

Cara mengimplementasikan checklist di atas:

Menyusun program dalam widget yang terstruktur, menggunakan Scaffold untuk tampilan dasar, lalu menambahkan tombol dengan GridView yang dirancang dalam ItemCard. Warna dan fungsi tombol diatur di dalam class ItemHomepage yang dibuat untuk menyimpan informasi tombol.

Checklist Implementasi TUgas 8

Halaman Formulir Tambah Item Baru: Membuat halaman baru untuk menambah item baru dengan elemen input berikut:
Produk: Nama produk
Deskripsi: Deskripsi produk
Harga: Harga produk


Validasi Input Formulir:
Setiap input tidak boleh kosong.
Validasi tambahan pada Harga untuk memastikan nilainya angka dan lebih besar dari 0.


Navigasi ke Halaman Form Tambah Item Baru:
Tombol "Tambah Item" di halaman utama mengarahkan pengguna ke halaman formulir tambah item.


Menampilkan Data dalam Pop-up setelah Save:
Setelah pengguna menekan tombol "Save" pada halaman formulir, data yang diisi akan muncul dalam pop-up konfirmasi.


Drawer dengan Dua Opsi:
Drawer memiliki opsi untuk Halaman Utama dan Tambah Item.
Opsi "Halaman Utama" mengarahkan pengguna ke halaman utama.
Opsi "Tambah Item" mengarahkan pengguna ke halaman formulir tambah item baru.




Apa kegunaan const di Flutter? Jelaskan apa keuntungan ketika menggunakan const pada kode Flutter. Kapan sebaiknya kita menggunakan const, dan kapan sebaiknya tidak digunakan?

const di Flutter digunakan untuk mendefinisikan widget atau nilai yang tidak akan berubah selama runtime.
Keuntungan: Menggunakan const memungkinkan Flutter menghindari rendering ulang pada widget yang sama sehingga menghemat memori dan meningkatkan performa aplikasi.
Penggunaan: const sebaiknya digunakan saat nilai widget sudah diketahui saat compile-time dan tidak akan berubah. Tidak perlu menggunakan const untuk widget yang akan diperbarui atau yang memiliki dependensi pada variabel runtime.

Jelaskan dan bandingkan penggunaan Column dan Row pada Flutter. Berikan contoh implementasi dari masing-masing layout widget ini!

Column digunakan untuk menyusun widget secara vertikal, sedangkan Row untuk menyusun widget secara horizontal.
Contoh Implementasi:
Column - Cocok untuk form input yang membutuhkan tata letak vertikal:
dart
Column(
  children: [
    Text('Label 1'),
    TextField(),
    Text('Label 2'),
    TextField(),
  ],
);
Row - Cocok untuk menampilkan ikon dan teks di sebelahnya:
dart
Row(
  children: [
    Icon(Icons.home),
    Text("Home"),
  ],
);


Sebutkan apa saja elemen input yang kamu gunakan pada halaman form yang kamu buat pada tugas kali ini. Apakah terdapat elemen input Flutter lain yang tidak kamu gunakan pada tugas ini? Jelaskan!
Elemen input yang digunakan adalah TextFormField untuk input Produk, Deskripsi, dan Harga.

Bagaimana cara kamu mengatur tema (theme) dalam aplikasi Flutter agar aplikasi yang dibuat konsisten? Apakah kamu mengimplementasikan tema pada aplikasi yang kamu buat?
Tema diatur menggunakan ThemeData dalam widget MaterialApp untuk mengatur skema warna dan tampilan yang konsisten di seluruh aplikasi.
Implementasi: Menggunakan primarySwatch pada ThemeData untuk memastikan warna dasar aplikasi seragam, dengan skema warna yang mudah dikelola.
Bagaimana cara kamu menangani navigasi dalam aplikasi dengan banyak halaman pada Flutter?

Menggunakan Navigator.push untuk berpindah ke halaman baru dan Navigator.pop untuk kembali ke halaman sebelumnya.
Pada proyek ini, Navigator.push digunakan untuk membuka halaman formulir tambah item, dan drawer digunakan untuk navigasi cepat antara halaman utama dan halaman tambah item baru.
