**Nama    : Ammara Pranahiza Widaryati**
**NPM     : 2206083022**
**Kelas   : PBP B**

TUGAS 7: ELEMEN DASAR FLUTTER

1. Apa perbedaan utama antara stateless dan stateful widget dalam konteks pengembangan aplikasi Flutter?
- Stateless Widget
Stateless Widget adalah widget yang tidak dapat berubah atau statis. Setelah widget ini dibuat dan dijalankan, konfigurasi yang dimuat dalam widget tersebut tidak akan berubah. Misalnya, jika ada widget yang menampilkan teks "Angka : 1", maka isi dari widget tersebut tidak akan berubah dari awal widget tersebut dimuat hingga aplikasi berjalan. Stateless Widget cocok digunakan ketika Anda hanya perlu menampilkan data yang statis atau tidak perlu adanya perubahan nilai.

- Stateful Widget adalah widget yang dapat berubah atau dinamis. Widget ini dapat melacak perubahan data dan merender ulang layout sesuai dengan perubahan data tersebut. Contoh dari pengaplikasiannya adalah ketika ingin menampilkan list nama dan warna yang berubah setiap kali tombol refresh diklik.

Maka, dapat disimpulkan perbedaan utamanya adalah Stateless Widget ketika ingin membuat widget atau komponen yang sederhana dan bersifat statis. Sedangkan, Stateful Widget ketika ingin membuat widget yang memiliki data atau komponen yang akan berubah-ubah

2. Sebutkan seluruh widget yang kamu gunakan untuk menyelesaikan tugas ini dan jelaskan fungsinya masing-masing.
- MaterialApp: Widget ini adalah widget root yang memberikan banyak fitur yang umum digunakan seperti navigasi, tema, dan localisasi bahasa.
- Scaffold: Widget ini menyediakan struktur dasar untuk halaman aplikasi Anda, seperti AppBar, BottomNavigationBar, FloatingActionButton, dan Drawer.
- AppBar: Widget ini biasanya digunakan untuk menampilkan judul aplikasi dan opsi navigasi.
- Text: Widget ini digunakan untuk menampilkan teks di aplikasi Anda.
- GridView: Widget ini digunakan untuk menampilkan daftar item dalam bentuk grid.
- SingleChildScrollView: Widget ini digunakan untuk memberikan scrolling pada widget tunggal.
- Padding: Widget ini digunakan untuk memberikan padding pada widget anaknya.
- Column: Widget ini digunakan untuk menampilkan widget anaknya secara vertikal.
- SnackBar: Widget ini digunakan untuk menampilkan pesan singkat yang muncul di bagian bawah layar.
- InkWell: Widget ini digunakan untuk memberikan responsivitas terhadap sentuhan pengguna.
- Container: Widget ini digunakan untuk memberikan padding, margin, dan decoration pada widget anaknya.
- Icon: Widget ini digunakan untuk menampilkan ikon.
- ShopCard: Widget khusus yang Anda buat untuk menampilkan informasi tentang item yang dijual.

3. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial)
Berikut adalah ringkasan dari tutorial yang Anda berikan:

- Memulai dengan Flutter
1. Buka Terminal atau Command Prompt dan masuk ke direktori tempat ingin menyimpan proyek Flutter.
2. Generate proyek Flutter baru sesuai nama proyek, kemudian masuk ke dalam direktori proyek tersebut menggunakan perintah `flutter create <APP_NAME>` dan `cd <APP_NAME>`.
3. Jalankan proyek melalui Terminal atau Command Prompt menggunakan perintah `flutter run`.

- Merapikan Struktur Proyek
1. Buat file baru bernama `menu.dart` pada direktori `nama-proyek/lib`.
2. Pindahkan kode dari class `MyHomePage` dan `_MyHomePageState` dari file `main.dart` ke file `menu.dart` yang baru saja dibuat.
3. Tambahkan kode `import 'package:shopping_list/menu.dart';` pada awal file `main.dart` untuk memperbaiki error yang terjadi karena pemindahan class `MyHomePage`.
4. Jalankan proyek melalui Terminal atau Command Prompt untuk memastikan bahwa aplikasi tetap dapat berjalan dengan baik.

- Membuat Widget Sederhana pada Flutter
1. Ubah tema warna aplikasi menjadi indigo dengan mengubah kode pada `main.dart` dibagian tema aplikasi.
2. Ubah sifat widget halaman menu menjadi stateless. Hapus `MyHomePage(title: 'Flutter Demo Home Page')` dan ubah `MyHomePage({Key? key}) : super(key: key);` menjadi `MyHomePage({Key? key}) : super(key: key);`.
3. Tambahkan teks dan card untuk memperlihatkan barang yang dijual. Definisikan tipe pada list dan tambahkan barang-barang yang dijual.
4. Tambahkan kode untuk menampilkan teks dan card di dalam Widget build.
5. Buat widget stateless baru untuk menampilkan card.

Dalam tutorial ini, menjelaskan tentang cara menggunakan Flutter dalam merapikan struktur proyek, dan membuat widget sederhana di Flutter.Selain itu, juga belajar cara mengubah tema warna aplikasi dan mengubah sifat widget menjadi stateless.