# Jarkom-Modul-1-D04-2021
1. Daffa Muhamad Azhar [05111940000037]
2. Taqarra Rayhan I [05111940000121]
3. Iwan Dwi Prakoso [05111940000229]

### Soal no 1 Sebutkan webserver yang digunakan pada "ichimarumaru.tech"!
Untuk mencari tahu web server yang digunakan. Dapat menggunakan display filter 
```http.host == ichimarumaru.tech```
![nomer 1](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/1a.PNG?raw=true)
lalu **CTRL + ALT + SHIFT + T** (klik kanan ==> follow ==> TCP Stream)
```tcp.stream eq 12```

### Soal no 2 Temukan paket dari **web-web** yang menggunakan **basic authentication** method!

### Soal no 3 Ikuti perintah di basic.ichimarumaru.tech! Username dan password bisa didapatkan dari file .pcapng!

### Soal no 4 Temukan paket mysql yang mengandung perintah query select!

### Soal no 5 Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file .pcap!

### Soal no 6 Cari username dan password ketika melakukan login ke FTP Server!

### Soal no 7 Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya "Real.pdf")

### Soal no 8 Cari paket yang menunjukan pengambilan file dari FTP tersebut!

### Soal no 9 Dari paket-paket yang menuju FTP terdapat inidkasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama "secret.zip". Simpan dan buka file tersebut!

### Soal no 10 Selain itu terdapat "history.txt" yang kemungkinan berisi history bash server tersebut! Gunakan isi dari "history.txt" untuk menemukan password untuk membuka file rahasia yang ada di "secret.zip"!

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
