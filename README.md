![image](https://github.com/user-attachments/assets/3f99ecc1-a4be-497b-8078-c0368b2ca4c2)
[Sekilas Tentang](#sekilas-tentang) | [Instalasi](#instalasi) | [Konfigurasi](#konfigurasi) | [Otomatisasi](#otomatisasi) | [Cara Pemakaian](#cara-pemakaian) | [Pembahasan](#pembahasan) | [Referensi](#referensi)
:---:|:---:|:---:|:---:|:---:|:---:|:---:

# Anggota kelompok 3 P1 Project KDJK
| Nama | NIM |
| -----| ----|
| Jesika Oktaviani | G6401221038|
| Sindi Aprilianti | G6401221037|
| Ammar Radhi Aziz Chan | 
| Muhammad Shidqi Abhinaya | 
| Chairul Rifky Tirtacahyadi | 
| Schin Nasarani Pangaribuan | X1004241070|

# Sekilas Tentang
LimeSurvey adalah platform survei online yang sederhana dan efisien, memungkinkan pengguna untuk membuat dan mengelola survei secara anonim. Platform ini dirancang untuk memudahkan berbagai kalangan, seperti mahasiswa, profesional, maupun perusahaan, dalam mendapatkan data yang relevan melalui survei yang dirancang secara cepat dan mudah. LimeSurvey juga tersedia secara gratis, dengan fitur-fitur yang memungkinkan pengguna merancang survei dengan antarmuka yang intuitif, serta memperoleh wawasan yang berguna untuk berbagai keperluan analisis data.
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
Setelah melakukan proses instalasi, extract file zip yang telah diinstall ke dalam folder baru, sebelum itu buatlah folder baru bernama limesurvey.
![image](https://github.com/user-attachments/assets/e2c3c968-e3eb-4380-bf61-9f8b74f1efd3)
![image](https://github.com/user-attachments/assets/4ba19a70-fa86-423d-8aa6-c88de575394d)
## Buat database untuk limesurvey
- Buka command line masuk ke MariaDB/MySQL
![image](https://github.com/user-attachments/assets/32eec320-87ed-43ba-a9ad-388e3b56f572)
- Buat database bernama limesurvey, tampilkan seluruh database untuk memastikan database limesurvey sudah dibuat
![image](https://github.com/user-attachments/assets/edd359c0-854c-424a-b748-aa3ec3445a67)
- Setelah itu, buat pengguna baru bernama lime_user yang dapat mengakses database dari localhost (komputer yang sama dengan server MariaDB). Buat juga identifikasi pengguna, kata sandi untuk pengguna ini adalah 12345.
![image](https://github.com/user-attachments/assets/d37c9ea1-0980-46c6-bdf7-2851d8b29300)
- Berikan semua privilege kepada pengguna lime_user untuk database limesurvey, memungkinkan operasi seperti SELECT, INSERT, UPDATE, dan DELETE.
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

- Setelah itu, klik next hingga limesurvey terinstall dengan sempurna
![Screenshot 2024-10-08 165009](https://github.com/user-attachments/assets/aee0a402-af68-455a-a3b6-b8cb1371c6ca)

- Klik tombol administration agar diarahkan ke halaman login admin
![image](https://github.com/user-attachments/assets/778eda77-2343-4a7f-9695-35e48f2725df)

- Setelah itu kita dapat membuat survey, lalu survey siap disebarkan!
![image](https://github.com/user-attachments/assets/a4f85d97-ccca-4ae7-8779-dfeb8851b888)



# Konfigurasi
- Untuk menentukan konfigurasi umum, kita dapat mengakses menu configuration.
![image](https://github.com/user-attachments/assets/43dd6514-aca8-4edf-9dbb-f764a2138366)

- Contohnya kita dapat memilih tema survey kita.
![image](https://github.com/user-attachments/assets/e03445cd-3617-46da-9e65-12f5d54e63e1)


# Maintenance
Ketika kita ingin melakukan pemeliharaan atau modifikasi pada aplikasi LimeSurvey yang sudah terinstal, kita mungkin tidak ingin responden atau pengguna lain mengakses survei atau fitur lain selama proses ini. Dalam situasi seperti itu, kita dapat mengatur aplikasi ke dalam maintenance mode.
Berikut adalah langkah-langkah yang perlu dilakukan:
- Login ke Admin Panel
  Akses admin panel LimeSurvey dengan menggunakan kredensial Anda.
- Navigasi ke Pengaturan Umum
  Setelah masuk, klik pada menu Pengaturan di sidebar, lalu di dalam menu pengaturan, cari dan pilih tab Maintenance.
- Aktifkan Maintenance Mode
  Klik tombol untuk mengaktifkan atau menonaktifkan maintenance mode sesuai kebutuhan. Pilih "On" untuk mengaktifkan 
  mode pemeliharaan.
  ![image](https://github.com/user-attachments/assets/2c3e07a6-bc11-4f0a-82ae-3639530fa540)
- Izinkan Akses untuk IP Tertentu
  Jika kita ingin mengizinkan teman untuk mengakses aplikasi selama mode pemeliharaan, masukkan alamat IP mereka pada kolom Maintenance IP. Hal ini memungkinkan mereka untuk mengakses aplikasi meskipun dalam mode pemeliharaan.
   ![Screenshot 2024-10-08 225132](https://github.com/user-attachments/assets/7c360551-2f74-42aa-9edb-904159f2a06a)

- Setelah mengisi alamat IP, jangan lupa untuk mengklik tombol Save untuk menyimpan perubahan
 ![Screenshot 2024-10-08 224855](https://github.com/user-attachments/assets/4584542c-d64e-49b3-bfd8-bd7229e93bea)


# Otomatisasi
Untuk mempermudah instalasi, kita dapat menggunakan dua cara, yaitu:
## Cara pertama
- Menginstall aplikasi Limesurvey pada pengedia layanan hosting seperti softaculos. Kita dapat mengunjungi situs softaculos.com lalu mencari aplikasi limesurvey pada searchbar atau pada kategori polls & analytics.
![image](https://github.com/user-attachments/assets/ac91369b-b01f-4503-b86c-13cd52356fbd)
Di sini kita dapat memilih untuk menginstallnya ke cloud softaculos atau menginstall dan mengembangkannya di lokal.
![image](https://github.com/user-attachments/assets/15df75de-11ed-4290-b018-6ecad87bc850)

## Cara kedua
- Kita tidak perlu menginstall aplikasi limesurvey melalui command line, kita hanya perlu mengakses website resmi instalasi versi terbaru dari limesurvey.
- Install packages dan file zip limesurvey pada link https://community.limesurvey.org/downloads/
 ![image](https://github.com/user-attachments/assets/e8ea99c7-0f5b-4bc2-923c-0ad6129001e2)



# Cara Pemakaian
Setelah instalasi, pengguna dapat mengakses LimeSurvey melalui browser dengan mengunjungi alamat server yang sesuai. Antarmuka aplikasi akan menampilkan berbagai fungsi utama, termasuk:
## Membuat survei baru.
Berikut merupakan tahapannya:
- Masukkan judul survey, setting bahasa serta kebutuhan lain yang diperlukan, kemudian klik "create survey"
![image](https://github.com/user-attachments/assets/fdd6c681-f54c-4976-b361-bed2e625a544)
- Isi Kategori Survey, Lalu tambahkan beberapa pertanyaan
![image](https://github.com/user-attachments/assets/62369d4f-1879-4ff5-a835-81bde2bae4b4)
- Kita dapat membuat, lalu mengedit pertanyaan pada survey
![image](https://github.com/user-attachments/assets/bdc23177-38fb-4307-9404-654870e25610)
- Kita dapat melihat preview survey yang kita buat, namun karena survey belum kita aktifkan, maka data dari pengguna tidak akan masuk ke database kita.
![image](https://github.com/user-attachments/assets/904bf7b5-db4a-4664-ac1d-7bb5699f34a4)

## Mengelola survei yang sudah ada
Limesurvey memungkinkan kita untuk mengelola survey yang telah kita buat termasuk untuk mengedit, serta mengaktifkan survey yang sudah kita buat.
Untuk mengaktivasi, dapat dilakukan di menu aktivasi berikut. 
![image](https://github.com/user-attachments/assets/d54e8868-6a84-43fb-840a-4a67fb1741d2)

- Setelah kita mengaktivasi survey yang kita buat, kita akan mencoba untuk mengirim beberapa jawaban
![image](https://github.com/user-attachments/assets/a8ef3808-636e-4f47-8305-bb6905c6297b)
- Akan muncul notifikasi
![image](https://github.com/user-attachments/assets/45b21161-602c-434a-a8ad-1d0d4d6f66f5)
- Setelah itu kita dapat melihat jawaban yang kita kirimkan di menu survey responses
  Dari jawaban para responden, kita dapat menganalisa data-data yang telah terkumpul
![image](https://github.com/user-attachments/assets/e0d4ee62-e6b1-4e87-a87c-03c5396a5722)



# Pembahasan
LimeSurvey memiliki kelebihan seperti antarmuka yang user-friendly dan fitur yang kaya. Namun, mungkin terdapat kekurangan dalam hal kustomisasi dan dukungan teknis. Dibandingkan dengan aplikasi survei lain, LimeSurvey menawarkan fitur yang kompetitif dengan kemampuan untuk mengelola survei secara efisien.
<details> 
  <summary> Kekurangan LimeSurvey</summary>
  LimeSurvey memiliki antarmuka yang kurang user-friendly dan terkesan monoton.
</details>
<details>
  <summary> Perbandingan dengan platform sejenis</summary>
  Dibandingkan dengan platform survei lain, misalnya Google Form, aplikasi LimeSurvey memiliki keunggulan dalam mengelola survey dengan efisien. Selain itu, LimeSurvey juga memberi kontrol penuh atas data yang ada, karena aplikasi ini dapat di install di server lokal. Sedangkan Google Forms mengedepankan survey yang sifatnya sederhana dan juga cepat. Tidak begitu cocok untuk survey yang kompleks, karena fiturnya masih terbatas.
</details>

# Referensi
- https://github.com/LimeSurvey/LimeSurvey/tree/master
- https://www.limesurvey.org/
- https://manual.limesurvey.org/Installation_using_a_command_line_interface_(CLI)
- https://manual.limesurvey.org/Installation_-_LimeSurvey_CE





