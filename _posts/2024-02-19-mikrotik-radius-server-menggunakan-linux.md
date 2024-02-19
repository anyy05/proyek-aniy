---
---
### Berikut adalah langkah-langkah umum untuk mengonfigurasi MikroTik dengan Radius Server menggunakan Linux:

## 1. Installasi dan Konfigurasi Radius Server di Linux:
Ubuntu/Debian
### 1. Install FreeRADIUS dengan perintah:

bash
Copy code
sudo apt-get update
sudo apt-get install freeradius
### 2. Konfigurasi FreeRADIUS:

File konfigurasi utama ada di /etc/freeradius/3.0/radiusd.conf.
Konfigurasi klien (MikroTik) dapat ditambahkan di /etc/freeradius/3.0/clients.conf.
### 3. Konfigurasi pengguna (user) di /etc/freeradius/3.0/users atau menggunakan modul seperti MySQL atau LDAP untuk menyimpan informasi pengguna.

### 4. Mulai dan aktifkan FreeRADIUS:

bash
Copy code
sudo systemctl start freeradius
sudo systemctl enable freeradius

## 2. Konfigurasi MikroTik:
### 1. Masuk ke MikroTik melalui Winbox atau terminal SSH.

### 2. Tambahkan konfigurasi Radius Server:

bash
Copy code
/radius add address=IP_Radius secret=shared_secret service=login,hotspot
IP_Radius: Alamat IP dari server Radius.
shared_secret: Kata sandi yang sama dengan yang dikonfigurasi di server Radius.

### 3. Atur MikroTik untuk menggunakan Radius sebagai metode otentikasi:

bash
Copy code
/ip hotspot profile set [find default=yes] use-radius=yes

### 4. Konfigurasi interface yang akan digunakan untuk Hotspot:

bash
Copy code
/ip hotspot set [find] interface=nama_interface

## 3. Uji Koneksi dan Otorisasi:
### 1. Uji koneksi ke server Radius dari MikroTik:

bash
Copy code
/tool user-manager user add username=test password=test customer=admin

### 2. Periksa log pada server Radius untuk memastikan tidak ada kesalahan:

bash
Copy code
sudo tail -f /var/log/freeradius/radius.log

### 3. Coba koneksikan perangkat ke Hotspot dan pastikan bahwa otentikasi dan otorisasi berfungsi dengan benar.
