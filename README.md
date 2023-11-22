**Nama    : Ammara Pranahiza Widaryati**
**NPM     : 2206083022**
**Kelas   : PBP B**

## TUGAS 7: ELEMEN DASAR FLUTTER

**1. Apa perbedaan utama antara stateless dan stateful widget dalam konteks pengembangan aplikasi Flutter?**
- Stateless Widget
Stateless Widget adalah widget yang tidak dapat berubah atau statis. Setelah widget ini dibuat dan dijalankan, konfigurasi yang dimuat dalam widget tersebut tidak akan berubah. Misalnya, jika ada widget yang menampilkan teks "Angka : 1", maka isi dari widget tersebut tidak akan berubah dari awal widget tersebut dimuat hingga aplikasi berjalan. Stateless Widget cocok digunakan ketika Anda hanya perlu menampilkan data yang statis atau tidak perlu adanya perubahan nilai.

- Stateful Widget adalah widget yang dapat berubah atau dinamis. Widget ini dapat melacak perubahan data dan merender ulang layout sesuai dengan perubahan data tersebut. Contoh dari pengaplikasiannya adalah ketika ingin menampilkan list nama dan warna yang berubah setiap kali tombol refresh diklik.

Maka, dapat disimpulkan perbedaan utamanya adalah Stateless Widget ketika ingin membuat widget atau komponen yang sederhana dan bersifat statis. Sedangkan, Stateful Widget ketika ingin membuat widget yang memiliki data atau komponen yang akan berubah-ubah

**2. Sebutkan seluruh widget yang kamu gunakan untuk menyelesaikan tugas ini dan jelaskan fungsinya masing-masing.**
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

**3. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial)**
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



## TUGAS 9: Integrasi Layanan Web Django dengan Aplikasi Flutter

**1. Apakah bisa kita melakukan pengambilan data JSON tanpa membuat model terlebih dahulu? Jika iya, apakah hal tersebut lebih baik daripada membuat model sebelum melakukan pengambilan data JSON?**
Ya, dapat dilakukan pengambilan data JSON tanpa membuat model terlebih dahulu. Ini bisa dilakukan dengan menggunakan fungsi json.decode() dari pustaka dart:convert. Namun, metode ini biasanya lebih baik digunakan untuk proyek kecil atau prototipe cepat. Untuk aplikasi dengan banyak model JSON dan kompleksitas yang lebih tinggi, metode ini bisa menjadi sulit dan memiliki risiko kesalahan yang tinggi. Model dapat membantu memvalidasi dan memahami struktur data.

**2. Jelaskan fungsi dari CookieRequest dan jelaskan mengapa instance CookieRequest perlu untuk dibagikan ke semua komponen di aplikasi Flutter.**
Dalam pengembangan aplikasi web dan mobile, cookieRequest adalah ide yang digunakan untuk mengirim atau menerima cookies melalui permintaan HTTP. Cookies biasanya digunakan untuk menyimpan informasi pengguna seperti preferensi atau status login. Instance CookieRequest harus dibagikan ke semua komponen dalam aplikasi Flutter untuk memastikan bahwa setiap permintaan HTTP yang dibuat oleh komponen tersebut menyertakan cookies yang sesuai, sehingga backend dapat mengidentifikasi pengguna yang membuat permintaan tersebut. Ini adalah cara yang dapat digunakan dalam Flutter untuk mempertahankan sesi pengguna saat berinteraksi dengan backend.

**3. Jelaskan mekanisme pengambilan data dari JSON hingga dapat ditampilkan pada Flutter.**
Untuk mendapatkan data dari JSON dan menampilkannya di Flutter, berikut langkah-langkah umumnya: 
- Buat permintaan HTTP ke endpoint yang akan mengembalikan data JSON menggunakan pustaka HTTP.

- Dapatkan respons dari permintaan dan ubahlah menjadi string.

- Untuk mengubah string JSON menjadi struktur data Dart, biasanya Map atau List, gunakan json.decode() atau web Quicktype.

- Gunakan informasi ini untuk memperbarui status aplikasi.

- Menggunakan widget yang sesuai, tampilkan informasi tersebut di UI Flutter.

**4. Jelaskan mekanisme autentikasi dari input data akun pada Flutter ke Django hingga selesainya proses autentikasi oleh Django dan tampilnya menu pada Flutter.**
- Pengguna dapat memasukkan informasi akun mereka, seperti nama pengguna dan kata sandi, ke dalam aplikasi Flutter.

- Melalui permintaan HTTP POST, aplikasi Flutter mengirimkan informasi akun ke backend Django.

- Backend Django memverifikasi informasi akun dan menghasilkan token autentikasi, seperti token JWT atau token sesi, dan mengirimkannya kembali ke aplikasi Flutter jika informasi akun tersebut valid.

- Aplikasi Flutter menyimpan token autentikasi tersebut dan menggunakannya untuk setiap permintaan berikutnya ke backend Django. Hal ini memungkinkan backend Django untuk mengidentifikasi pengguna yang mengajukan permintaan.

- Menu Flutter akan ditampilkan berdasarkan hak akses pengguna yang telah diverifikasi setelah proses autentikasi selesai.

**5. Sebutkan seluruh widget yang kamu pakai pada tugas ini dan jelaskan fungsinya masing-masing.**
- MaterialApp: Fungsi utama widget ini adalah untuk menyediakan konfigurasi dasar seperti judul aplikasi, tema, dan routing ke halaman utama, yang digunakan sebagai widget utama dalam aplikasi Flutter.

- Provider: widget yang memungkinkan pengelolaan state dan penyediaan objek ke seluruh bagian aplikasi. Dalam tugas ini, instance CookieRequest diberikan ke semua child widgets melalui Provider.

- Scaffold: Widget ini menawarkan komponen seperti appBar, body, dan drawer untuk memberikan struktur dasar halaman. Biasanya digunakan sebagai kerangka halaman utama atau halaman terpisah dalam aplikasi.

- AppBar: bagian yang menampilkan bar navigasi di bagian atas halaman, biasanya berisi judul halaman, tombol kembali, dan aksi-aksi lainnya.

- Drawer: Widget ini memiliki panel navigasi yang dapat ditarik dari sisi layar. Ini dapat menampilkan menu atau navigasi lainnya dalam aplikasi.

- TextField: widget input teks yang memungkinkan pengguna memasukkan teks. Dalam contoh ini, digunakan untuk menerima kata sandi dan kata sandi untuk halaman login.

- ElevatedButton: Ketika ditekan, tombol yang ditingkatkan dapat memulai tindakan seperti melakukan proses login atau tindakan lainnya.

- FutureBuilder: widget yang membuat penanganan data masa depan lebih mudah. Digunakan untuk menampilkan data yang akan diperoleh di masa mendatang dari pengumpulan data ke server atau sumber lainnya.

- ListView.builder: widget yang dapat digunakan untuk menampilkan daftar data dalam bentuk daftar yang dapat digulir. Ini dapat digunakan untuk menampilkan daftar produk atau informasi dalam bentuk dinamis.

- SnackBar: fitur yang menampilkan pesan singkat kepada pengguna. Ini biasanya digunakan untuk memberikan umpan balik setelah tindakan tertentu, seperti login berhasil/gagal atau penambahan produk berhasil/gagal.

- AlertDialog: Widget yang dapat menampilkan dialog dan memberi pengguna opsi seperti konfirmasi atau pesan peringatan.

- Text: Widget teks yang dapat menampilkan informasi seperti nama produk, harga, deskripsi, dan pesan aplikasi.

- Column: Widget yang memungkinkan penyusunan anak widget dalam satu kolom; ini bermanfaat untuk menata tampilan secara vertikal.

- MaterialPageRoute: Digunakan untuk menghubungkan aplikasi antara halaman.

**6. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step! (bukan hanya sekadar mengikuti tutorial).**
**Pada Django:**
1. Buat django-app ‘authentication’.
2. Tambahkan ‘authentication’ ke INSTALLED_APPS di settings.py.
3. Install library ‘django-cors-headers’.
4. Tambahkan ‘corsheaders’ ke INSTALLED_APPS dan ‘corsheaders.middleware.CorsMiddleware’ ke middleware di settings.py.
5. Atur variabel CORS dan CSRF di settings.py.
6. Buat metode view untuk login di authentication/views.py.
7. Tambahkan URL routing untuk fungsi login di urls.py.

**Pada Flutter:**
1. Install package ‘provider’ dan ‘pbp_django_auth’.
2. Modifikasi root widget untuk menyediakan CookieRequest library ke semua child widgets menggunakan Provider.
3. Buat halaman login.dart yang memungkinkan pengguna untuk login melalui Flutter.

**Pembuatan Model Kustom**
1. Manfaatkan situs web Quicktype untuk membuat model Dart yang sesuai dengan data JSON yang ada.
2. Buat file model baru dalam proyek Flutter dan tempelkan kode model yang dihasilkan dari Quicktype.

**Penerapan Fetch Data dari Django ke Flutter**
1. Tambahkan dependensi package http untuk melakukan HTTP request.
2. Buat halaman baru untuk menampilkan produk dengan menggunakan FutureBuilder dan fetch data dari Django.

**Integrasi Form Flutter Dengan Layanan Django**
1. Tambahkan fungsi view baru di views.py Django untuk menerima data dari Flutter.
2. Hubungkan halaman form di Flutter dengan Django untuk menambahkan produk baru.

**Implementasi Fitur Logout**
1. Tambahkan metode view untuk logout pada views.py Django.
2. Implementasikan fungsi logout pada aplikasi Flutter dengan menggunakan request ke endpoint logout yang telah dibuat pada Django.

Pastikan untuk menyesuaikan URL, pengaturan, dan kode sesuai dengan proyek masing-masing.