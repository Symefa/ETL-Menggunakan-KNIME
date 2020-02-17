# ETL Menggunakan KNIME

Oleh : Alifa Izzan

## Daftar Isi
1. KNIME dan ETL
   1. [Tentang KNIME](#tentang-knime)
   2. [Penjelasan ETL](#penjelasan-ETL)
   3. [Pemasangan KNIME](#pemasangan-knime)
      1. [Unduh KNIME](#unduh-knime)
      2. [Jalankan Installer](#jalankan-installer)
      3. [Menggunakan KNIME](#menggunakan-knime)
2. ETL dengan KNIME
   1. [Persiapan](#persiapan)
   2. [Unduh Datasaet](#unduh-dataset)
   3. [Deskripsi Dataset](#deskripsi-dataset)
   4. [Pemasangan Dataset](#pemasangan-dataset)
   5. [Menentukan Tujuan Proses ETL](#menentukan-tujuan-proses-etl)
   6. [Proses ETL dengan KNIME](#proses-etl-dengan-knime)
   7. [Hasil dan Kesimpulan](#hasil-dan-kesimpulan)
3. [Refrensi](#refrensi)
4. [Lisensi](#lisensi)

## Tentang KNIME
![knime](assets/knime.png "Logo KNIME")

KNIME merupakan perangkat lunak gratis dan terbuka yang digunakan untuk menganalisa, membuat laporan, dan mengintegrasikan data. KNIME merupakan kependekan dari, *the Konstanz Information Miner*. Perangkat lunak ini cukup mudah digunakan karena tidak perlu belajar bahasa pemrograman khusus. Berikut tampilan antar muka KNIME.

![antar muka](assets/knime-1.jpg "Antar muka KNIME")

## Penjelasan ETL

![ETL](assets/ETL.jpg)

ETL merupakan kependekan dari *Extract-Transform-Load*, proses ini merupakan proses yang dimulai dari mengambil data dari berbagai sumber lalu data tersebut diolah sedemikian rupa sesuai kebutuhan bisnis. Data yang telah diolah tersebut lalu disimpan pada tempat penyimpanan basis data.

## Pemasangan KNIME

### Unduh KNIME

untuk mengunduh perangkat lunak KNIME anda dapat memilih sesuai sistem operasi yang anda gunakan

| Sistem Operasi | Arsitektur |
| :------------: | :---: |
| Windows        | [64-bit](https://www.knime.com/download-installer/2/64bit) |
|                | [32-bit](https://www.knime.com/download-installer/2/32bit) |
| Linux          | [64-bit](https://www.knime.com/download-installer/6/64bit) |
| MacOS          | [64-bit](https://www.knime.com/download-installer/8/64bit) |

> Jika tautan diatas tidak bisa diakses buka tautan ini: [Unduh Knime](https://www.knime.com/downloads/download-knime)

### Jalankan Installer
> Petunjuk ini menggunakan sistem operasi *Windows 10 build 1909 64-bit*, beberapa material petunjuk mungkin berbeda untuk versi dan/atau jenis sistem operasi yang berbeda.

![Install](assets/install.jpg "Jalankan Installer")

Klik 2 kali berkas *installasi* yang telah diunduh melalui tautan sebelumnya. Setelah anda klik maka akan muncul pemberitahuan UAC(User Account Control). Klik *yes* untuk memulai pemasangan.

![Accept](assets/install-2.png)

Pilih *I accept the agreement* lalu tekan tombol *Next*.

![Folder](assets/install-3.png)

Anda dapat memilih map pemasangan perangkat lunak KNIME. Setelah anda memilih map pemasangan perangkat lunak KNIME, klik *Next* untuk melanjutkan pemasangan.

![Shortcut](assets/install-4.png)

Selanjutnya anda dapat memilih tautan cepat yang dipasang pada menu mulai. Setelah selesai memilih maka klik *Next* untuk melanjutkan pemasangan.

![Opsional](assets/install-5.png)

Setelah itu anda dapat memilih opsi tambahan pengaturan perangkat lunak KNIME. Setelah selesai memilih opsi tambahan maka klik *Next* untuk melanjutkan pemasangan.

![RAM](assets/install-6.png)

Selanjutnya anda akan diminta untuk mengisi opsi maksimum RAM (Random Access Memory) yang dapat digunakan oleh perangkat lunak KNIME, opsi ini akan otomatis terisi dan menyesuaikan dengan kapasitas RAM perangkat keras anda. Klik *Next* untuk melanjutkan pemasangan.

![Review](assets/install-7.png)

Setelah selesai memilih opsi pada antar muka sebelumnya anda dapat melihat kembali apakah opsi yang anda pilih sudah sesuai pada jendela ini. Setelah selesai maka tekan *Install* untuk memulai pemasangan.

![Mulai](assets/install-8.png)

Tunggu hingga pemasangan selesai, jangan mematikan paksa perangkat lunak anda selama proses berlangsung. jika sudah selesai anda akan menemui jendela ini.

![Finish](assets/install-9.png)

Tekan *Finish* untuk keluar dari jendela dan menjalankan perangkat lunak KNIME.

### Menggunakan KNIME

Anda dapat menggunakan KNIME melalui tautan cepat pada menu mulai.

![First](assets/first-launch.jpg)

Saat pertama kali menjalankan perangkat lunak KNIME anda akan diminta untuk mengisi map tempat kerja. Agar tidak muncul jendela tempat kerja lagi maka centang opsi "Use this as default and do not ask again". setelah selesai klik tombol *Launch*.

![data collection](assets/launch-1.jpg)

Jendela persetujuan pembagian data akan muncul anda dapat memilih opsi pembagian data penggunaan perangkat lunak dengan KNIME untuk meningkatkan kualitas perangkat lunak KNIME.

![antar muka](assets/launch-2.jpg)

anda telah selesai menggunakan KNIME.

## ETL dengan KNIME
___
### Persiapan

Sebelum melakukan proses ETL beberapa bagian yang perlu disiapkan adalah:

1. Sistem Basis Data (MySQL, PostgreSQL, dan lain-lain)
2. Perangkat Lunak Pemrosesan Basis Data (PHPMyAdmin, PHPPgAdmin, Navicat, Workbench, dan lain-lain) 
3. Perangkat Lunak Pemrosesan Text (VScode, Notepad++, Notepad, dan lain-lain)
4. KNIME
5. Dataset 
   
Untuk panduan ETL dengan KNIME ini penulis menggunakan :
1. KNIME 4.1.1
2. MySQL 80
3. PostgreSQL 12
4. VScode 1.42.1
5. Windows 10 build 1909 64-bit

Dataset yang penulis gunakan didapatkan melalui [kaggle](https://kaggle.com)
   
> Perbedaan versi dan/atau jenis perangkat lunak yang digunakan mungkin memiliki perbedaan langkah dalam panduan ini

### Unduh Dataset

![unduhdt](assets/unduh.jpg "Tampilan halaman pengunduhan")

Anda dapat mengunduh dataset yang saya gunakan melalui tautan berikut: [goodbooks-10k](https://www.kaggle.com/zygmunt/goodbooks-10k)

### Deskripsi Dataset

Dataset goodbooks-10k ini terdiri dari beberapa berkas dengan format csv.

![dataset](assets/dataset.jpg "goodbooks-10k")

| Berkas | Deskripsi | Kolom | Jumlah Kolom |
| :----- | :-------- | :--- | :---: |
| books_tags.csv | berkas ini berisi hubungan beserta kekuatannya antara penanda dan buku | goodreads_book_id, tag_id, count | 3 |
| books.csv | berkas ini berisi deskripsi dari buku | id, book_id, best_book_id, work_id, books_count, isbn, isbn13, authors, original_publication_year, original_title, title, language_code, average_rating, ratings_count, work_ratings_count, work_text_reviews_count, ratings_1, ratings_2, ratings_3, ratings_4, ratings_5, image_url, small_image_url | 23 |
| ratings.csv | berkas ini berisi penilaian yang diberikan oleh pengguna layanan | book_id, user_id, rating | 3 |
| sample_book.xml | berkas ini merupakan contoh data yang diperoleh dari layanan |  |  |
| tags.csv | berkas ini berisikan penanda dari buku | tag_id, tag_name | 2 |
| to_read.csv | berkasa ini berisikan buku yang akan dibaca oleh pengguna layanan | user_id, book_id | 2 |

### Pemasangan Dataset

![dataset1](assets/dataset1.jpg)

Pengaturan pemasangan dataset yang dipilih penulis adalah sebagai berikut:

| Berkas | Basis Data |
| :----- | :--------- |
| books_tags.csv | MySQL |
| books.csv | PostgreSQL |
| ratings.csv | MySQL |
| sample_book.xml | |
| tags.csv | File |
| to_read.csv | File |

### Menentukan Tujuan Proses ETL

Dari deskripsi dataset yang penulis temukan penulis memutuskan untuk menemukan penanda apa yang paling dinikmati oleh pengguna layanan berdasarkan:
* to_read
* ratings

> Metode aggregasi menggunakan penambahan agar prosesnya cepat. Hal ini dapat menyebabkan hasil rekomendasi kurang akurat. Anda dapat menggunakan metode lain yang lebih akurat.

### Proses ETL dengan KNIME

#### Persiapan

![](assets/etl-1.jpg)
Buat *workflow group* baru dengan cara klik kanan pada *Local Workspace*, lalu pilih *New Workflow Group*

![](assets/etl-2.jpg)
Setelah itu akan muncul jendela baru. disini anda dapat memasukkan nama *workflow group* yang anda inginkan. Klik *Finish* untuk menyelesaikan pembuatan *workflow group*.

![](assets/etl-3.jpg)
Selanjutnya klik kanan pada *workflow group* yang baru anda buat dan pilih *New KNIME Workflow*

![](assets/etl-4.jpg)
Sama seperti saat membuat *workflow group*, muncul jendela baru. Di sini anda dapat mengisikan nama *KNIME workflow*, jika sudah selesai maka klik *Finish*.

#### Proses Extract

![](assets/etl-5.jpg)
Klik dan tahan penghubung basis data dan/atau pembaca yang anda gunakan, lalu lepaskan di tengah perangkat lunak.

![](assets/etl-6.jpg)
Pada jendela perangkat lunak KNIME bagian tengah akan muncul gambar penghubung yang anda pilih. Klik kanan pada gambar tersebut lalu pilih *Configure*

![](assets/etl-7.jpg)
Setelah anda klik *Configure*, naka akan muncul jendela baru. isikan kredensial sistem basis data yang anda gunakan pada jendela ini. Lalu klik *Ok*.

Ulangi proses ini sesuai kebutuhan anda.

![](assets/etl-11.jpg)
Ulangi proses ini sesuai kebutuhan anda.

![](assets/etl-12.jpg)
Anda juga dapat merubah nama dari *Node* dengan cara Klik 2 kali pada nama *Node* yang ingin anda ubah.

![](assets/etl-15.jpg)
Jika menggunakan penghubung sistem basis data anda memerlukan pembaca *query DB*. Hubungkan pembaca dengan penghubung dengan meng-klik dan menahan gambar kotak merah kecil dan melepaskannya pada kotak merah kecil yang ingin dihubungkan.

![](assets/etl-16.jpg)
Selanjutnya buka konfigurasi pembaca *query DB* dan mengklik *Refresh*, klik 2 kali pada tabel yang ingin anda ambil lalu pada kotak paling kanan tambahkan

```
SELECT * FROM 
```

sebelum nama tabel dan skema yang ingin anda ambil. sehingga menjadi

```SQL
SELECT * FROM "goodbooks"."book_tags"
```
![](assets/etl-17.jpg)
tekan *evaluate* untuk memastikan sintaks anda sudah benar. Jika sudah benar, maka akan muncul seperti gambar diatas. selanjutnya tekan tombol *Ok*

![](assets/etl-18.jpg)
Ulangi proses ini sesuai kebutuhan anda.

#### Proses Transform

![](assets/etl-19.jpg)
Pada jendela kiri bawah anda dapat memilih manipulasi apa yang anda inginkan atau anda dapat menggunakan fitur pencarian pada paling kanan atas di jendela kiri bawah.

![](assets/etl-20.jpg)
Atur penyaring sesuai kebutuhan anda. fitur penyaringan digunakan untuk membersihkan data awal. Pemilik dataset telah memberi peringatan bahwa dataset goodbooks-10k memiliki book_id duplikat.

![](assets/etl-21.jpg)
Setelah dieksekusi anda dapat menampilkan hasil pengolahan melalui klik kanan pada *node* yang anda pilih lalu klik opsi pada paling bawah dialog yang muncul.

![](assets/etl-22.jpg)

![](assets/etl-25.jpg)
Untuk menyaring data duplikat dari tabel sekunder yang pada normalnya terdapat data duplikat penting, kita dapat menggunakan penyaring dengan refrensi. Fungsi dari penyaring tersebut memilih hanya data yang ter-refrensi pada tabel primer yang normalnya tidak memiliki data duplikat.

![](assets/etl-27.jpg)
untuk menyaring data yang tidak penting juga dapat menggunakan fitur penyaring baris dengan *RegEx*.

```RegEx
[a-z\-]+
```
![](assets/etl-28.jpg)
Tambahkan penyaring sesuai kebutuhan anda.

![](assets/etl-29.jpg)
Selanjutnya menggabungkan dua tabel data dengan menggunakan fitur penggabung.

![](assets/etl-31.jpg)
Atur penggabungan data sesuai dataset yang anda pilih.

![](assets/etl-30.jpg)
Jika terjadi *error* pada pembaca berkas matikan opsi *read row IDs*

![](assets/etl-join.jpg)
Atur penggabung tabel sesuai tabel yang ingin anda gabung

![](assets/groupby.jpg)
Tambahkan agregasi yang anda inginkan, fitur ini mengelompokkan baris dengan nilai yang sama.

![](assets/groupby-2.jpg)
Atur Agregasi sesuai kebutuhan anda. gunakan fitur penyaringan, penggabungan, dan aggregasi sesuai kebutuhan anda.

#### Proses Load
![](assets/etl-34.jpg)
Tambahkan penulis basis data dan atur sesuai skema basis data anda. pilih opsi *remove exiting table*

![](assets/etl-35.jpg)
Tambahkan penulis berkas. dan atur sesuai kebutuhan anda.

### Hasil dan Kesimpulan
![](goodread_structure.svg)
Skema final dari ETL menggunakan KNIME

![](assets/etl-33.jpg)
Hasil ETL dengan menggunakan KNIME

| Hasil | File |
| :---: | :---: |
|10_tags_most_rated|[Download](result/10_tags_most_rated.xlsx)|
|10_tags_to_read|[Download](result/10_tags_to_read.xlsx)|
| goodread.knar | [Download](goodread.knar) |

Kesimpulan yang penulis dapatkan bahwasanya KNIME merupakan perangkat lunak pengolahan ETL yang mudah digunakan karena tidak membutuhkan bahasa khusus. Dengan penggunaan KNIME penulis dapat mencapai tujuan ETL yang penulis inginkan. Desain antar muka yang cukup intuitif dan menarik mendukung pengalaman pengguna.

## Refrensi

1. KNIME AG, Zurich, Switzerland, [Download KNIME Analytics Platform](https://www.knime.com/next-steps "Download KNIME Analytics Platform"), *www.knime.com*, Diakses tanggal 17/2/2020
2. Zygmunt Zając, [goodbooks-10k](https://www.kaggle.com/zygmunt/goodbooks-10k), Diakses tanggal 17/2/2020
3. M. Bernard, Big Data: : using smart big data, analytics and metrics to make better decisions and improve performance, 1 penyunt., Chichester, West Sussex: John Wiley & Sons Ltd, 2015
4.  "[ETL-Extract-Load-Process](https://www.guru99.com/etl-extract-load-process.html)". *www.Guru99.com*, Diakses tanggal 17/2/2020

## Lisensi

Penulis : Alifa Izzan - izzan@poroskolektif.com

Lisensi : [![CC BY-SA](https://licensebuttons.net/l/by-sa/3.0/88x31.png)](https://creativecommons.org/licenses/by-sa/4.0/)