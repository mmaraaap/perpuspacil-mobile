**Nama    : Ammara Pranahiza Widaryati**
**NPM     : 2206083022**
**Kelas   : PBP B**

## TUGAS 7: ELEMEN DASAR FLUTTER

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


## TUGAS 8: Flutter Navigation, Layouts, Forms, and Input Elements

**1. Jelaskan perbedaan antara Navigator.push() dan Navigator.pushReplacement(), disertai dengan contoh mengenai penggunaan kedua metode tersebut yang tepat!**
- Navigator.push() digunakan untuk memasukkan halaman baru ke atas stack navigasi. Halaman yang dipanggil menggunakan Navigator.push() akan menjadi halaman teratas dalam stack navigasi. Ketika kembali dari halaman tersebut, maka akan kembali ke halaman sebelumnya dalam stack

- Navigator.pushReplacement() digunakan untuk memasukkan halaman baru ke atas stack navigasi dan menghapus halaman sebelumnya dari stack. Halaman yang dipanggil menggunakan Navigator.pushReplacement() akan menjadi halaman teratas dalam stack navigasi dan halaman sebelumnya akan dihapus dari stack. Oleh karena itu, tidak ada cara kembali ke halaman sebelumnya dari halaman yang dipanggil menggunakan Navigator.pushReplacement()

- Contoh Penggunaan:
**Menggunakan Navigator.push()**
   Navigator.push(
     context,
     MaterialPageRoute(builder: (context) => SecondRoute()),
   );

**Menggunakan Navigator.pushReplacement()**
   Navigator.pushReplacement(
     context,
     MaterialPageRoute(builder: (context) => HomeRoute()),
   );

**2. Jelaskan masing-masing layout widget pada Flutter dan konteks penggunaannya masing-masing!**
- Container:  
Container adalah widget serbaguna yang dapat digunakan untuk mengubah properti seperti padding, margin, ukuran, dan warna latar. Ini memungkinkan membungkus dan mengatur tata letak widget lainnya. Container ideal untuk mengatur properti dasar dan menata widget lain dengan properti yang sudah ditentukan.

- Kolom dan Row:
Row dan Column membantu mengorganisir tata letak dalam satu arah dengan menyusun widget secara horizontal (Row) atau vertikal (Column). Membantu menyusun widget seperti tombol, teks, atau gambar dalam satu baris atau kolom untuk membuat tata letak linear.

- ListView:
ListView adalah widget yang digunakan untuk membuat daftar scrollable (bergulir) dari widget. Ini sangat berguna ketika memiliki daftar item yang mungkin lebih panjang dari layar perangkat. Cocok untuk menampilkan daftar item dalam aplikasi, seperti daftar pesan, kontak, atau berita.

- Stack:
Stack memungkinkan penumpukan widget di atas satu sama lain, memungkinkan tata letak yang lebih kompleks dan layering. Berguna ketika perlu menempatkan widget di atas widget lainnya, seperti dalam pembuatan overlay atau desain yang lebih kompleks.

- Expanded dan Flexible:
Expanded dan Flexible digunakan dalam Row atau Column untuk memberikan ukuran dinamis kepada widget. Ini membantu mendistribusikan ruang yang tersedia sesuai dengan proporsi tertentu. Berguna untuk membuat widget berukuran dinamis, terutama ketika ingin memberikan ruang lebih banyak kepada satu widget dibandingkan yang lain.

- SizedBox:
SizedBox digunakan untuk menentukan ukuran tepat untuk suatu widget atau memberikan ruang putih di antara widget. Berguna ketika perlu menentukan dimensi tepat dari suatu widget atau memberikan spasi di antara widget.

**3. Sebutkan apa saja elemen input pada form yang kamu pakai pada tugas kali ini dan jelaskan mengapa kamu menggunakan elemen input tersebut!**
- TextFormField: Digunakan untuk memasukkan teks seperti nama produk, harga, dan deskripsi. Dapat digunakan untuk validasi dan mendapatkan nilai dari pengguna.
- ElevatedButton: Digunakan sebagai tombol untuk mengirimkan atau menyimpan formulir.
- AlertDialog: Menampilkan dialog dengan informasi produk setelah formulir disimpan.

**4. Bagaimana penerapan clean architecture pada aplikasi Flutter?**
Clean Architecture adalah prinsip desain perangkat lunak yang menekankan pada pemisahan tanggung jawab antara komponen-komponen aplikasi. Dalam konteks aplikasi Flutter, Clean Architecture dapat diterapkan  dengan membuat aplikasi terdiri dari tiga layer: Presentation, Domain, dan Data.

- Layer Presentation adalah layer yang bertanggung jawab atas UI dan interaksi pengguna. Ini adalah layer di mana nanti akan menggunakan widget-widget Flutter seperti StatelessWidget dan StatefulWidget.

- Layer Domain adalah layer yang bertanggung jawab atas bisnis logic aplikasi. Ini adalah layer di mana nanti akan mendefinisikan entitas, use case, dan repository.

- Layer Data adalah layer yang bertanggung jawab atas komunikasi dengan sumber data eksternal seperti database atau API.

Dengan menerapkan Clean Architecture, akan  membuat aplikasi Flutter lebih mudah untuk dipahami, diuji, dan dikelola

**5. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step! (bukan hanya sekadar mengikuti tutorial)**

**Menambahkan Menu Drawer untuk Navigasi**
1. Membuat Berkas Baru:
    - Buat berkas left_drawer.dart di dalam direktori widgets.
    - Tambahkan widget Drawer dengan ListView di dalamnya.

2. Mengimpor Halaman:
    - Import halaman seperti MyHomePage dan ShopFormPage yang akan ditambahkan ke drawer.

3. Menambahkan Navigasi ke Drawer:
    - Tambahkan ListTile untuk setiap halaman yang ingin ditambahkan ke dalam routing drawer.
    - Gunakan Navigator.pushReplacement untuk mengarahkan ke halaman baru.

4. Menghias Drawer:
    - Tambahkan dekorasi dan teks pada bagian header drawer untuk memberikan tampilan yang menarik.
    - Sesuaikan desain dan tata letak sesuai dengan kebutuhan.

5. Mengintegrasikan Drawer ke Halaman:
    - Import drawer yang sudah dibuat ke halaman yang ingin ditambahkan drawer-nya.
    - Masukkan drawer sebagai nilai parameter drawer pada widget Scaffold.

**Menampilkan Data**
1. Membuat Berkas Form Baru:
    - Buat berkas shoplist_form.dart di dalam direktori lib.
    - Tambahkan widget Scaffold dengan AppBar dan drawer yang sudah dibuat sebelumnya.

2. Menambahkan Widget Form:
    - Gunakan widget Form sebagai wadah untuk bidang input.
    - Gunakan SingleChildScrollView untuk membuat form menjadi scrollable.

3. Mengimplementasikan Bidang Input:
    - Tambahkan TextFormField untuk setiap elemen input yang dibutuhkan.
    - Gunakan Padding dan Column untuk merapikan tata letak elemen input.
V
4. Validasi Input:
    - Gunakan atribut onChanged pada TextFormField untuk mendeteksi perubahan nilai.
    - Terapkan validasi dengan atribut validator untuk memastikan input sesuai kebutuhan.

5. Menampilkan Data pada AlertDialog:
    - Gunakan showDialog ketika formulir tervalidasi.
    - Tampilkan data yang dimasukkan oleh pengguna pada AlertDialog.
    - Reset formulir setelah data ditampilkan.

**Menambahkan Fitur Navigasi pada Tombol**
1. Navigasi dari Tombol pada ShopItem:
    - Dalam fungsi onTap pada widget ShopItem, gunakan Navigator.push untuk melakukan navigasi ke halaman yang sesuai.

**Refactoring File**
1. Membuat Berkas Baru untuk Widget:
    - Buat berkas shop_card.dart di dalam direktori widgets.
    - Pindahkan konten widget ShopItem dari menu.dart ke shop_card.dart.

2. Mengimpor File ke dalam Folder:
    - Buat folder baru screens di dalam direktori lib.
    - Pindahkan berkas menu.dart dan shoplist_form.dart ke dalam folder screens.

3. Memastikan Refactoring Dilakukan dengan IDE:
    - Pastikan proses pemindahan berkas dilakukan melalui IDE atau text editor dengan ekstensi Flutter