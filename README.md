![image](https://github.com/user-attachments/assets/3f99ecc1-a4be-497b-8078-c0368b2ca4c2)
[Sekilas Tentang](#sekilas-tentang) | [Instalasi](#instalasi) | [Hosting](#hosting) | [Konfigurasi](#konfigurasi) | [Otomatisasi](#otomatisasi) | [Cara Pemakaian](#cara-pemakaian) | [Pembahasan](#pembahasan) | [Referensi](#referensi)
:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:

# Kelompok 3 P1 Project KDJK
| Nama | NIM |
| -----| ----|
| Jesika Oktaviani | G6401221038|
| Sindi Aprilianti | G6401221037|
| Ammar Radhi Aziz Chan | G6401221075
| Muhammad Shidqi Abhinaya | G6401221096 |
| Chairul Rifky Tirtacahyadi | G6401221067 |
| Schin Nasarani Pangaribuan | X1004241070 |

# Sekilas Tentang
LimeSurvey merupakan sebuah platform survei online yang bersifat sederhana dan efisien. Selain itu, aplikasi ini juga memungkinkan pengguna untuk dapat membuat dan mengelola survei secara anonim. Dirancang untuk memudahkan banyak kalangan, mulai dari mahasiswa, profesional,hingga perusahaan dalam mendapatkan data yang relevan melalui survei yang disusun secara cepat dan mudah. LimeSurvey tersedia secara gratis, dilengkapi dengan fitur-fitur yang memungkinkan pengguna untuk merancang survei dengan antarmuka yang intuitif, dan mendapatkan informasi yang dapat dimanfaatkan untuk berbagai keperluan, khususnya terkait analisis data.

# Instalasi
Sebelum menginstal LimeSurvey, pastikan bahwa sistem memenuhi prasyarat berikut:
- Apache >= 2.4 | nginx >= 1.1 | any other php-ready webserver
- php >= 7.2.5
  - with mbstring and pdo-database drivers
- mysql >= 5.5.9 | pgsql >= 9 | mariadb >= 5.5 | mssql >= 2005

## Memastikan sudah menginstall apache
  ![image](https://github.com/user-attachments/assets/4f336592-f9fc-48cf-aad5-c8d74a82aa60)

## Kita juga dapat memantau dan mengelola database menggunakan mysqlserver phpmyadmin
  ![image](https://github.com/user-attachments/assets/4cf21b2b-c0c5-4ac8-93c1-4cae8e961c64)

## Proses Instalasi:
- Buka command line (kelompok kami menggunakan command line pada windows)
- Masuk ke folder xampp>htdocs untuk menginstall file zip limesurvey yang versi paling baru.
![image](https://github.com/user-attachments/assets/9599b237-eefb-461e-b258-f751d90da72b)
Proses instalasi sedang berjalan
![image](https://github.com/user-attachments/assets/3ea2ea42-3271-43a1-9786-e966297ba515)
Buat folder baru bernama limesurvey, kemudian extract file zip yang telah terinstal ke folder tersebut.
![image](https://github.com/user-attachments/assets/e2c3c968-e3eb-4380-bf61-9f8b74f1efd3)
![image](https://github.com/user-attachments/assets/4ba19a70-fa86-423d-8aa6-c88de575394d)
## Buat database untuk limesurvey
- Buka command line dan masuk ke MariaDB/MySQL
![image](https://github.com/user-attachments/assets/32eec320-87ed-43ba-a9ad-388e3b56f572)
- Buat database bernama limesurvey, lalu tampilkan seluruh database untuk memastikan database limesurvey telah dibuat
![image](https://github.com/user-attachments/assets/edd359c0-854c-424a-b748-aa3ec3445a67)
- Setelah itu, buat pengguna baru bernama lime_user yang dapat mengakses database dari localhost, dari kkomputer yang sama dengan server MariaDB. Kemumdian buat juga identifikasi pengguna dan kata sandi untuk pengguna ini adalah 12345.
![image](https://github.com/user-attachments/assets/d37c9ea1-0980-46c6-bdf7-2851d8b29300)
- Berikan semua privileged kepada pengguna lime_user untuk operasi di database limesurvey, seperti SELECT, INSERT, UPDATE, dan DELETE.
![image](https://github.com/user-attachments/assets/e798b11b-d298-456d-be72-acfbb0205351)
- Segarkan hak akses agar perubahan segera berlaku.
![image](https://github.com/user-attachments/assets/8aa915cb-b82c-4ac9-b2be-ee70caf1eb3c)

## Kunjungi alamat IP web server kita untuk meneruskan instalasi.
- Pilih bahasa yang akan digunakan
![image](https://github.com/user-attachments/assets/bed007b4-5074-48b0-9119-43a8ff4c3fda)

- Setujui persyaratan yang berlaku
![image](https://github.com/user-attachments/assets/99d1c585-6548-4260-aaf1-357300ca4d3f)

- Cek semua minimum requiremets
![Screenshot 2024-10-08 164525](https://github.com/user-attachments/assets/366bc90a-f48c-4c04-9c37-7dae8425dcd0)
![Screenshot 2024-10-08 164534](https://github.com/user-attachments/assets/e06e6f10-df1b-4eea-a27a-d17df91f0e7e)
jika current tidak tercentang hijau, buka file php.ini di folder htdocs>php, lalu aktifkan ekstensi yang dibutuhkan dengan menghapus ";" pada bagian depannya.
![Screenshot 2024-10-08 164606](https://github.com/user-attachments/assets/51643ad9-2e68-4366-8937-eed0211b4276)

- Konfigurasi database
Cocokkan dengan data user serta database yang sudah kita buat tadi
![Screenshot 2024-10-08 164708](https://github.com/user-attachments/assets/6eab2dc1-2e50-4a60-8114-1767ebd26d9d)
![Screenshot 2024-10-08 164848](https://github.com/user-attachments/assets/0f81ccd8-6502-45c1-a6a4-a6ab812f9a55)

- Karena di sini kita memiliki role sebagai administrator, isi setting login name password, email dan sebagainya pada laman administrator setting.
![Screenshot 2024-10-08 164940](https://github.com/user-attachments/assets/0b14dd0e-7f2b-4ba9-be48-55f396908eca)
![Screenshot 2024-10-08 164950](https://github.com/user-attachments/assets/e9c7472d-6564-4997-bfcc-cf864c5a2d65)

- Setelah itu, klik next hingga limesurvey selesai terinstall.
![Screenshot 2024-10-08 165009](https://github.com/user-attachments/assets/aee0a402-af68-455a-a3b6-b8cb1371c6ca)

- Klik tombol administration agar diarahkan ke halaman login admin.
![image](https://github.com/user-attachments/assets/778eda77-2343-4a7f-9695-35e48f2725df)

- Setelah itu kita sudah dapat membuat survei dan laman survei siap disebar.
![image](https://github.com/user-attachments/assets/a4f85d97-ccca-4ae7-8779-dfeb8851b888)

# Hosting
## Menjalankan aplikasi web pada penyedia layanan hosting
Kelompok kami menggunakan jasa hosting dari rumahweb dengan rincian layanan hosting web selama satu bulan, limitasi ukuran file sebesar maksimal 1 GB, support aplikasi php, mysql dan sejenisnya. Kami juga mengunggah file aplikasi yang database dan administrasinya telah dikonfigurasi di localhost.
![image](https://github.com/user-attachments/assets/1cf08c58-ed97-4b95-929b-ea0b010fb25a)
Untuk tata caranya:
- Klik entry hosting lalu login ke Cpanel
  ![image](https://github.com/user-attachments/assets/644b4e82-2bb4-4380-be40-73edd5c6bd06)
- Lalu akan muncul tampilan seperti ini
  ![image](https://github.com/user-attachments/assets/3018a5e5-8672-4627-96c9-70fcd7e9c297)
- Setelah itu, klik mysql button untuk membuat database dan user baru.
  ![image](https://github.com/user-attachments/assets/fd5d832e-4bff-4862-897e-f35294965903)
- Database tersebut nantinya akan diisi dengan database localhost LimeSurvey yang telah diekspor. Ketika akan mengekspor, pastikan format filenya berupa .sql.
  ![image](https://github.com/user-attachments/assets/804e035b-07e1-449d-b36d-4cc1d707e464)
  ![image](https://github.com/user-attachments/assets/40b03d5b-87dc-4984-af7f-b21e666f1f62)
- Buka database yang telah dibuat di mysql melalui phpmyadmin, lalu klik database kdjk5557_limesurvey, lalu import database local.
  Tampilannya akan menjadi seperti berikut ini ketika import database telah berhasil.
  ![image](https://github.com/user-attachments/assets/e3beb238-1f96-4912-9dc9-316dae749989)
- Setelah database selesai diimport, buka cpanel dan masuk ke file manager. Berikutnya unggah file limesurvey ke folder bernama public_html dengan format zip untuk menghindari kelebihan ukuran file. Setelah file zipnya berhasil diunggah, ekstrak file tersebut di dalam folder public_html.
  ![image](https://github.com/user-attachments/assets/6e6c9605-cc13-49c8-9fae-00a8ef90302c)
- Atur konfigurasi database, host, dan user pada file cofig.php untuk menyesuaikan dengan database dan privileged user yang telah dibuat pada rumahweb.
![image](https://github.com/user-attachments/assets/3a57c4f8-d836-416b-b64f-c2c91f6ca55a)
  
- klik save changes
![image](https://github.com/user-attachments/assets/a8d5378e-0468-466f-8f63-95287b03cec8)

- Sekarang, aplikasi sudah dapat berjalan di link: https://kdjklimesurvey.my.id/limesurvey/
  - User publik akan dapat melihat berbagai survei yang tersedia
  ![image](https://github.com/user-attachments/assets/a9ea0cfc-1fa3-46bc-9d68-dd09c81f05c4)
  ![image](https://github.com/user-attachments/assets/c51d3d64-cb96-4d72-9a9a-01bc8174dd38)
  ![image](https://github.com/user-attachments/assets/f0023eb1-bbae-498e-9cb9-98c93856dd97)

- Kita dapat mengelola aplikasi sebagai admin pada web yang sudah dihosting, yang memiliki cara kerja persis sama dengan yang telah dijalankan di localhost.
  ![image](https://github.com/user-attachments/assets/37bda59f-0368-48a0-a191-e16c6129f097)



# Konfigurasi
- Menu configuration dapat digunakan untuk menentukan konfigurasi umum
![image](https://github.com/user-attachments/assets/43dd6514-aca8-4edf-9dbb-f764a2138366)

- Contohnya pengguna dapat memilih tema survei sesuai kebutuhan
![image](https://github.com/user-attachments/assets/e03445cd-3617-46da-9e65-12f5d54e63e1)


# Maintenance
Maintenance mode dapat digunakan ketika kita berencana melakukan modifikasi ataupun pemeliharaan pada aplikasi LimeSurvey yang sudah terinstal tapi tidak ingin pengguna atau responden mengakses fitur atau survei yang ada, cukup ikuti langkah-langkah berikut ini:  
- Login ke Admin Panel
  Akses admin panel LimeSurvey dengan menggunakan kredensial.
- Navigasi ke Pengaturan Umum
  Setelah masuk, klik menu pengaturan di sidebar, lalu cari tab Maintenance.
- Aktifkan Maintenance Mode
  Klik tombol untuk mengaktifkan atau menonaktifkan maintenance mode sesuai kebutuhan. Pilih "On" untuk mengaktifkan 
  mode pemeliharaan.
  ![image](https://github.com/user-attachments/assets/2c3e07a6-bc11-4f0a-82ae-3639530fa540)
- Izinkan Akses untuk IP Tertentu
  Jika kita ingin mengizinkan teman untuk mengakses aplikasi selama mode pemeliharaan, masukkan alamat IP mereka pada kolom Maintenance IP, yang memungkinkan mereka tetap dapat mengakses aplikasi meskipun sedang berada dalam mode pemeliharaan.
  ![Screenshot 2024-10-08 225132](https://github.com/user-attachments/assets/7c360551-2f74-42aa-9edb-904159f2a06a)

- Setelah mengisi alamat IP, jangan lupa untuk mengklik tombol Save untuk menyimpan perubahan
 ![Screenshot 2024-10-08 224855](https://github.com/user-attachments/assets/4584542c-d64e-49b3-bfd8-bd7229e93bea)


# Otomatisasi
Untuk mempermudah instalasi, kita dapat menggunakan dua cara, yaitu:
## Cara pertama
- Menginstall aplikasi Limesurvey pada pengedia layanan hosting seperti softaculos, dengan cara mengunjungi situs softaculos.com lalu mencari aplikasi limesurvey pada searchbar atau pada kategori polls & analytics.
![image](https://github.com/user-attachments/assets/ac91369b-b01f-4503-b86c-13cd52356fbd)
Di sini kita dapat memilih untuk menginstallnya ke cloud softaculos atau menginstall dan mengembangkannya di lokal.
![image](https://github.com/user-attachments/assets/15df75de-11ed-4290-b018-6ecad87bc850)

## Cara kedua
- Hanya perlu mengakses website resmi instalasi versi terbaru dari LimeSurvey tanpa perlu menginstal melalui command line.
- Install packages dan file zip limesurvey pada link https://community.limesurvey.org/downloads/
 ![image](https://github.com/user-attachments/assets/e8ea99c7-0f5b-4bc2-923c-0ad6129001e2)

# Cara Pemakaian
Setelah instalasi, pengguna dapat mengakses LimeSurvey melalui browser dengan mengunjungi alamat server yang sesuai, kemudian antarmuka aplikasi akan menampilkan berbagai fungsi utama, seperti:
## Membuat survei baru.
Berikut merupakan tahapannya:
- Masukkan judul survei, setting bahasa, dan kebutuhan lain yang diperlukan, kemudian klik "create survey"
![image](https://github.com/user-attachments/assets/fdd6c681-f54c-4976-b361-bed2e625a544)
- Isi Kategori Survei, lalu tambahkan beberapa pertanyaan
![image](https://github.com/user-attachments/assets/62369d4f-1879-4ff5-a835-81bde2bae4b4)
- Kita dapat membuat dan mengedit pertanyaan pada survei
![image](https://github.com/user-attachments/assets/bdc23177-38fb-4307-9404-654870e25610)
- Kita dapat melihat preview survei yang kita buat, namun karena survei belum kita aktifkan, maka data dari pengguna tidak akan masuk ke database kita.
![image](https://github.com/user-attachments/assets/904bf7b5-db4a-4664-ac1d-7bb5699f34a4)

## Mengelola survei yang sudah ada
LimeSurvey memungkinkan kita untuk dapat mengelola survei yang telah dibuat, seperti melakukan pengeditan dan mengaktifkan survei.
Jika ingin melakukan aktivasi, dapat masuk ke menu aktivasi berikut ini.
![image](https://github.com/user-attachments/assets/d54e8868-6a84-43fb-840a-4a67fb1741d2)

- Setelah dilakukan aktivasi survei, coba untuk mengirim beberapa jawaban
![image](https://github.com/user-attachments/assets/a8ef3808-636e-4f47-8305-bb6905c6297b)
- Jika terkirim, maka akan muncul notifikasi
![image](https://github.com/user-attachments/assets/45b21161-602c-434a-a8ad-1d0d4d6f66f5)
- Setelah itu kita dapat melihat jawaban yang kita kirimkan di menu survei responses
  Dari jawaban para responden, kita dapat menganalisa data-data yang telah terkumpul
![image](https://github.com/user-attachments/assets/e0d4ee62-e6b1-4e87-a87c-03c5396a5722)

- Statistik repons dari survei yang telah kita buat dapat dilihat di menu statistik. Selain itu, kita juga dapat menganalisis respon para responden tersebut melalui fitur visualisasi yang disediakan LimeSurvey.
![image](https://github.com/user-attachments/assets/f647fbc6-84d9-485a-bd47-cd5e550906cf)



# Pembahasan
LimeSurvey memiliki keunggulan ketika digunakan untuk survei kompleks dan berskala besar, dapat melihat statistik dan juga visualisasi dari para responden untuk memudahkan analisis data. Platform ini juga memberikan kontrol penuh atas data yang ada, karena di install di server lokal. Namun, LimeSurvey kekurangan dalam hal dukungan teknis, antarmuka yang kurang friendly dan terkesan monoton. <br>
  Dibandingkan dengan platform survei lain, misalnya Google Form, aplikasi LimeSurvey memiliki keunggulan dalam mengelola survei dengan efisien, karena dapat menampilkan statistik dan juga visualisasi dari jawaban para responden, sehingga memudahkan analisis data. Selain itu, LimeSurvey juga memberi kontrol penuh atas data yang ada karena dapat di instal di sever lokal. Aplikasi ini tepat digunakan bagi pengguna yang membutuhkan solusi survei yang fleksibel dan mendalam, terutama untuk proyek yang melibatkan survei kompleks berskala besar. Namun, LimeSurvey memiliki antarmuka yang kurang menarik dan dukungan teknis yang terbatas yang dapat menjadi hambatan bagi beberapa pengguna. Sedangkan Google Form mengedepankan survei yang sifatnya sederhana, mudah, dan cepat. Tidak cocok untuk survei yang kompleks karena fiturnya masih terbatas. Data pada Google Form ini disimpan di server Google.

# Referensi
- https://github.com/LimeSurvey/LimeSurvey/tree/master
- https://www.limesurvey.org/
- https://manual.limesurvey.org/Installation_using_a_command_line_interface_(CLI)
- https://manual.limesurvey.org/Installation_-_LimeSurvey_CE





