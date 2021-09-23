# Jarkom-Modul-1-D04-2021

### Soal no 11
Untuk memfilter agar wireshark hanya mengambil paket yang berasal dari port 80 maka pada capture filter diberikan filter: 
```
src port 80
```
![alt text](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/11.png?raw=true)

### Soal no 12
Untuk memfilter agar wireshark hanya mengambil paket yang mengandung port 21 maka pada capture filter diberikan filter: 
```
port 21
```
![alt text](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/12.png?raw=true)

### Soal no 13
Untuk memfilter agar wireshark hanya menampilkan paket yang menuju port 443 maka pada display filter diberikan filter: 
```
tcp.dstport == 443
```
![alt text](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/13.png?raw=true)

### Soal no 14
Untuk memfilter agar wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id maka pada capture filter diberikan filter: 
```
dst host kemenag.go.id
```
![alt text](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/14.png?raw=true)

### Soal no 15
Untuk memfilter agar wireshark hanya mengambil paket yang berasal dari ip kalian maka pada capture filter diberikan filter src host <ip masing masing> atau sebagai contoh: 
```
src host 192.168.0.108
```
![alt text](https://github.com/EEB12/Jarkom-Modul-1-D04-2021/blob/main/images/15.png?raw=true)

## Kendala
1. Tidak teliti membaca soal
