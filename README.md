# Jarkom-Modul-1-D04-2021
1. Daffa Muhamad Azhar [05111940000037]
2. Taqarra Rayhan I [05111940000121]
3. Iwan Dwi Prakoso [05111940000229]

### Soal no 1 Sebutkan webserver yang digunakan pada "ichimarumaru.tech"!
Untuk mencari tahu web server yang digunakan. Dapat menggunakan display filter 

```
http.host == ichimarumaru.tech
```

![nomer 1](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/1a.PNG?raw=true)

lalu **CTRL + ALT + SHIFT + T** (klik kanan ==> follow ==> TCP Stream)

```
tcp.stream eq 12
```

![nomer 1](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/1b.PNG?raw=true)

sehingga didapatkan web server dari web tersebut adalah
> nginx/1.18.0 (ubuntu)


### Soal no 2 Temukan paket dari **web-web** yang menggunakan **basic authentication** method!
Untuk menemukan paket tersebut dapat menggunakan display filter

```
http.authbasic
```

sehingga paket - paket yang didapatkan adalah sebagai berikut

![nomer 2](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/2.PNG?raw=true)


### Soal no 3 Ikuti perintah di basic.ichimarumaru.tech! Username dan password bisa didapatkan dari file .pcapng!
Untuk mendapatkan username dan password dari web tersebut, dapat menggukana filter 

```
http.host == basic.ichimarumaru.tech
```

lalu pilih paket no 2066

kemudian lihat paket detail (Authorization ==> Credentials) maka didapatkan username:password

> kuncimenujulautan:tQKEJFbgNGC1NCZlWAOjhyCOm6o3xEbPkJhTciZN

![nomer 3](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/3a.PNG?raw=true)

Kemudian diminta untuk menyebutkan konfigurasi pengkabelan T568A

![nomer 3](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/3b.PNG?raw=true)


### Soal no 4 Temukan paket mysql yang mengandung perintah query select!
untuk menemukan paket tersebut dapat menggunakan filter

```
mysql.query matches select
```

![nomer 4](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/4.PNG?raw=true)


### Soal no 5 Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file .pcap!
Untuk mendapatkan username dan passwordnya dapat menggunakan filter

```
mysql.query matches insert
```

dapat dilihat pada detail paket tertera username dan juga passwordnya

> Username : akakanomi
>
> Password : pemisah4lautan

![nomer 5](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/5a.PNG?raw=true)

setelah berhasil login, kita diminta untuk menyebutkan urutan konfigurasi pengkabelan T568B

![nomer 5](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/5b.PNG?raw=true)


### Soal no 6 Cari username dan password ketika melakukan login ke FTP Server!
untuk mendapatkan username dan password dapat menggunakan display filter 

```
ftp.request.command == PASS || ftp.request.command == USER
```

dan kita akan mendapatkan username dan juga passwordnya

> USER secretuser
>
> PASS aku.pengen.pw.aja

![nomer 6](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/6.PNG?raw=true)


### Soal no 7 Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya "Real.pdf")
untuk mengetahui file yang benar dapat menggunakan display filter 

```
ftp-data contains Real.pdf
```

![nomer 7](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/7a.PNG?raw=true)

setelah mendapatkan paketnya, lalu **CTRL + ALT + SHIFT + T** (klik kanan ==> follow ==> TCP Stream) 

```
tcp.stream eq 128
```

![nomer 7](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/7b.PNG?raw=true)

kemudian ubah `show data as` menjadi RAW ==> save as zip file

![nomer 7](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/7c.PNG?raw=true)

setelah dibuka isinya adalah sebagai berikut

![nomer 7](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/7d.PNG?raw=true)


### Soal no 8 Cari paket yang menunjukan pengambilan file dari FTP tersebut!
untuk mencari paket yang menunjukan pengambilan file dari ftp tersebut dapat menggunakan display filter 
```
ftp.request.command == RETRR
```
setelah dijalankan  display filter maka akan muncul seperti dibawah ini

![nomer 8](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/8.PNG?raw=true)

tidak ada yang muncul pada wireshark setelah dijalankan display filter tersebut

### Soal no 9 Dari paket-paket yang menuju FTP terdapat inidkasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama "secret.zip". Simpan dan buka file tersebut!
pertama untuk mencari file rahasia yang bernama "secret.zip" dapat menggunakan display filter
```
ftp-data.command contains "secret.zip"
```
![nomer 9](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/9a.PNG?raw=true)
lalu setelah dijalankan display filter klik kanan dan follow tcp stream maka akan muncul seperti berikut
![nomer 9](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/9b.PNG?raw=true)

kemudian ubah data menjadi raw dan simpan menjadi file .zip
![nomer 9](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/9d.PNG?raw=true)

### Soal no 10 Selain itu terdapat "history.txt" yang kemungkinan berisi history bash server tersebut! Gunakan isi dari "history.txt" untuk menemukan password untuk membuka file rahasia yang ada di "secret.zip"!

untuk mendapatkan password dari file yang telah kita download dari nomor 9, kita diperintahkan untuk menggunakan isi dari "history.txt". Sama seperti sebelumnya kita menggunakan display filter berikut

```
ftp-data.command contains "history.txt"
```
![nomer 10](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/10a.PNG?raw=true)

setelah itu kita follow tcp stream dan muncul seperti berikut

![nomer 10](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/10b.PNG?raw=true)

kita akan melihat file bernama "bukanapaapa.txt" maka kita mencari file tersebut dengan display filter yang pernah kita gunakan sebelumnya.
```
ftp-data.command contains "bukanapaapa.txt"
```
![nomer 10](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/10c.PNG?raw=true)

lalu kita follow tcp stream
![nomer 10](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/10d.PNG?raw=true)
kita akan menemukan password dari isi file .zip sebelumnya dan dapat kita masukkan ke .zip 
![nomer 10](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/10e.PNG?raw=true)

dan akan muncul gambar wanted luffy
![nomer 10](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/10f.PNG?raw=true)

### Soal no 11 Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!
Untuk memfilter agar wireshark hanya mengambil paket yang berasal dari port 80 maka pada capture filter diberikan filter: 
```
src port 80
```
![alt text](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/11.png?raw=true)

### Soal no 12 Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
Untuk memfilter agar wireshark hanya mengambil paket yang mengandung port 21 maka pada capture filter diberikan filter: 
```
port 21
```
![alt text](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/12.png?raw=true)

### Soal no 13 Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
Untuk memfilter agar wireshark hanya menampilkan paket yang menuju port 443 maka pada display filter diberikan filter: 
```
tcp.dstport == 443
```
![alt text](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/13.png?raw=true)

### Soal no 14 Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id!
Untuk memfilter agar wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id maka pada capture filter diberikan filter: 
```
dst host kemenag.go.id
```
![alt text](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/14.png?raw=true)

### Soal no 15 Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
Untuk memfilter agar wireshark hanya mengambil paket yang berasal dari ip kalian maka pada capture filter diberikan filter src host <ip masing masing> atau sebagai contoh: 
```
src host 192.168.0.108
```
![alt text](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/15.png?raw=true)

## Kendala
1. Tidak teliti membaca soal
