---
title: GUI Component - Progress Indicators (Loaders)
layout: post
---

## Definisi


Loader (pemuat) atau progress adalah component controll yang mengekspresikan waktu tunggu yang tidak ditentukan atau sejauh mana proses itu berjalan. 


## Penggunaan

Progress indikator menginformasikan pengguna mengenai status dari proses yang sedang berjalan. Seperti memuat suatu tampilan, melakukan submisi, ataupun mengenai download atau saving sesuatu.


Saat menampilkan gabungan dari banyak proses, progress juga dapat ditampilkan secara grup dimana progress yang ditampilkan di layar merupakan rata rata dari seluruh proses


## Anatomi

![](7.png)
 


Secara garis besar progress indicator terdiri dari dua elemen. yaitu :


### 1. Track

Track adalah tempat dimana indicator tersebut run. Track memiliki ukuran yang fix dan akan dilalui indikator


### 2. Indicator

Indikator akan menganimasikan proses berjalannya progress. Indikator akan running sepanjang track


## Behavior
 


Setiap jenis progress indicator memiliki behavior yang berbeda. Namun secara umunnya progress indikator, memiliki behavior running memenuhi suatu track (untuk definite) atau mengitari sesuatu. Progress indicator biasanya akan berada diatas suatu surface. 



## Types


Progress indicator dapat dibagi menjadi dua jenis berdasarkan bentuk.


### 1. Circular


Bentuk progress circular berbentuk dimana proses akan digambarkan dengan bentuk melingkar. Progress circular berbentuk lingkaran. Track akan berbentuk lingkaran dengan warna transparan / tipis, dengan indicator yang akan berputar mengisi track tersebut. Circular progress dibagi menjadi dua kembali yaitu, definite circular progress dan undefinit circular progress. 


Determinate Circular Progress digambarkan dengan indicator mengisi invisible track dengan pada circular track, dari 0 hingga 360 derajat

Indeterminate Circular Progress digambarkan dengan indikator yang membesar dan mengecil memutari track transparan.


2, Linear 


Linear progress digambarkan dengan indikator yang memenuhi track horizontal yang biasanya berada di sudut layar (biasanya diatas). Pada awalnya linear progress hanya dapat menggambarkan determinate operation dimana progress digambarkan berbentuk loading bar, dengan indikator memenuhi track berdasarkan progress yang telah berjalan. Namun semakin berkembangnya ux research, linear progress dapat menggambarkan proses indeterminate. Operasi indeterminate ditunjukan dengan garis indikator akan membesar dan mengecil sambil berjalan pada track hingga operasi tersebut berhasil di eksekusi.



## Placement


Penempatan dari progress indikator dapat ditentukan dari jangkauan dari proses tersebut.

1. JIka indikator berada di tengah layar mengartikan program melakukan loading.

![](/home/a/cj/IMK-master/14.png) 

2. JIka indikator berada di dalam kontainer, seperti pada card, mengartikan proses pada komponen tersebut

3. Indikator dapat diletakkan dalam expanding edge pada expanding items, agar user dapat mengetahui dimana konten tambahan saat konten ter ekspand
![](/home/a/cj/IMK-master/15.png)



## Spesifikasi


![](/home/a/cj/IMK-master/12.png)
Sebagai contoh pada material design milik android, progress indicator memiliki spesifikasi umum sebagai berikut.


1. Warna dari indikator adalah biru keunguan dengan hexcode #6200ef dengan warna indicator #6200ee99.
2. Ketebalan dari indicator atau track memiliki tebal 4 dps(device indepedent pixels)

## Keterangan tambahan

Di setiap environtment, device, aplikasi, hingga sistem operasi, terdapat bebarapa aturan dan tipe progress indicator yang bisa saja berbeda dibandingkan dengan kaidah design yang ada. 


## Implementasi pada Payfazz

PT PAYFAZZ Teknologi Nusantara atau PAYFAZZ merupakan platform layanan keuangan berbasis keagenan yang dapat membantu dan mempermudah transaksi serta pembayaran secara digital. Kehadiran kami bertujuan untuk membantu masyarakat Indonesia, khususnya bagi yang belum memiliki rekening bank (unbanked). Melalui layanan PAYFAZZ, semua pihak kini dapat melakukan transaksi keuangan dan pembayaran digital dengan mudah, cepat, nyaman, dimanapun, dan kapanpun hanya dalam satu genggaman.

Secara user interface dan user experience, payfazz terlihat nyaman digunakan walaupun terlihat simpel. Terdapat hal yang menarik dari progress indicator dari aplikasi PAYFAZZ ini. Progress indicator diaplikasi ini digambarkan dengan seolah olah apps melakukan loading terhadap card kosong, walaupun aplikasi ini tidak memuat card yang berukuran sama. Hal ini membuat user menjadi berpikir aplikasi akan sedang melakukan load.

Berikut adalah contoh implementasi dari progress bar di payfazz.


![](/home/a/cj/IMK-master/1.png) 
![](/home/a/cj/IMK-master/2.png) 

Implementasi ini memiliki banyak sisi baik ataupun sisi buruk. Sisi baiknya adalah tampilan dan prosesnya yang simple mengikuti dengan design utama dari PAYFAZZ. Pengguna pun merasa proses yang ditunggu benar benar akan load. Sisi buruknya adalah terdapat fake load, Dari aplikasi tersebut karena hasil load aplikasi tidak sesuai dengan indikator dan track yang ditampilkan.


## Backlink


https://www.payfazz.com/

 


## Referensi:


https://material.io/design/components/progress-indicators.html#linear-progress-indicators

https://google-developer-training.gitbooks.io/android-developer-fundamentals-course-practicals/content/en/Unit%202/52_p_material_design_cards_and_the_fab.html

https://www.hongkiat.com/blog/beautiful-progress-bars/

