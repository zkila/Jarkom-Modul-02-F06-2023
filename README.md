# Jarkom-Modul-2-F06-2023

Kelompok F06:
- Arkana Bilal Imani / 5025211034
- Azhar Abiyu Rasendriya H. / 5025211177

## Daftar Isi

- [Official Report](#laporan-resmi)
  - [Daftar Isi](#daftar-isi)
  - [Topologi](#topologi)
  - [Konfig Node](#konfig)
  - [Prasyarat](#prerequisite)
- [No.1 - DNS](#Soal-1)
  - [Skrip](#skrip)
  - [Hasil Tes](#hasil)
- [No. 2 - DNS](#Soal-2)
  - [Skrip](#skrip-1)
  - [Hasil Tes](#hasil-1)
- [No. 3 - DNS](#Soal-3)
  - [Skrip](#skrip-2)
  - [Hasil Tes](#hasil-2)
- [No. 4 - DNS](#Soal-4)
  - [Skrip](#skrip-3)
  - [Hasil Tes](#hasil-3)
- [No. 5 - DNS](#Soal-5)
  - [Skrip](#skrip-4)
  - [Hasil Tes](#hasil-4)
- [No. 6 - DNS](#Soal-6)
  - [Skrip](#skrip-5)
  - [Hasil Tes](#hasil-5)
- [No. 7 - DNS](#Soal-7)
  - [Skrip](#skrip-6)
  - [Hasil Tes](#hasil-6)
- [No. 8 - DNS](#Soal-8)
  - [Skrip](#skrip-7)
  - [Hasil Tes](#hasil-7)
- [No. 9 - Webserver](#Soal-9)
  - [Skrip](#skrip-8)
  - [Hasil Tes](#hasil-8)
- [No. 10 - Webserver](#Soal-10)
  - [Skrip](#skrip-9)
  - [Hasil Tes](#hasil-9)
- [No. 11 - Webserver](#Soal-11)
  - [Skrip](#skrip-10)
  - [Hasil Tes](#hasil-10)
- [No. 12 - Webserver](#Soal-12)
  - [Skrip](#skrip-11)
  - [Hasil Tes](#hasil-11)
- [No. 13 - Webserver](#Soal-13)
  - [Skrip](#skrip-12)
  - [Hasil Tes](#hasil-12)
- [No. 14 - Webserver](#Soal-14)
  - [Skrip](#skrip-13)
  - [Hasil Tes](#hasil-13)
- [No. 15 - Webserver](#Soal-15)
  - [Skrip](#skrip-14)
  - [Hasil Tes](#hasil-14)
- [No. 16 - Webserver](#Soal-16)
  - [Skrip](#skrip-15)
  - [Hasil Tes](#hasil-15)
- [No. 17 - Webserver](#Soal-17)
  - [Skrip](#skrip-16)
  - [Hasil Tes](#hasil-16)
- [No. 18 - Webserver](#Soal-18)
  - [Skrip](#skrip-17)
  - [Hasil Tes](#hasil-17)
- [No. 19 - Webserver](#Soal-19)
  - [Skrip](#skrip-18)
  - [Hasil Tes](#hasil-18)
- [No. 20 - Webserver](#Soal-20)
  - [Skrip](#skrip-19)
  - [Hasil Tes](#hasil-19)
 
### Topologi

![Alt text](img/topolog.png)

### Konfig

- Router
```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
	address 192.224.1.1
	netmask 255.255.255.0

auto eth2
iface eth2 inet static
	address 192.224.2.1
	netmask 255.255.255.0

auto eth3
iface eth3 inet static
	address 192.224.3.1
	netmask 255.255.255.0
```
- Switch 1
  - Nakula
    ```
    auto eth0
      iface eth0 inet static
	    address 192.224.1.2
	    netmask 255.255.255.0
	    gateway 192.224.1.1
    ```
  - Sadewa
    ```
    auto eth0
    iface eth0 inet static
	    address 192.224.1.3
    	netmask 255.255.255.0
    	gateway 192.224.1.1
    ```
  - Arjuna
    ```
    auto eth0
    iface eth0 inet static
	    address 192.224.1.4
	    netmask 255.255.255.0
	    gateway 192.224.1.1
    ```
- Switch 2
  - Yudhistira
    ```
    auto eth0
    iface eth0 inet static
    	address 192.224.2.2
    	netmask 255.255.255.0
    	gateway 192.224.2.1
    ```
  - Werkudara
    ```
    auto eth0
    iface eth0 inet static
    	address 192.224.2.3
    	netmask 255.255.255.0
    	gateway 192.224.2.1
    ```
- Switch 3
  - Prabukusuma
    ```
    auto eth0
    iface eth0 inet static
    	address 192.224.3.2
    	netmask 255.255.255.0
    	gateway 192.224.3.1
    ```
  - Abimanyu
    ```
    auto eth0
    iface eth0 inet static
    	address 192.224.3.3
    	netmask 255.255.255.0
    	gateway 192.224.3.1
    ```
  - Wisanggeni
    ```
    auto eth0
    iface eth0 inet static
    	address 192.224.3.4
    	netmask 255.255.255.0
    	gateway 192.224.3.1
    ```
