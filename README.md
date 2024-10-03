* Nama : M. Rafif Farihan
* Nim : 09011282328042
* Kelas : SK3C
* Tugas 7 Praktikum sistem operasi
  
# Cara Menginstal dan Mengonfigurasi OpenSSH di Ubuntu

## Langkah 1: Memperbarui Paket
Hal pertama yang perlu dilakukan sebelum mulai menginstal SSH di Ubuntu adalah memperbarui semua paket apt ke versi terbaru. Untuk melakukannya, gunakan perintah berikut:
```bash
sudo apt update && sudo apt upgrade
```
![Memperbarui Paket](https://github.com/Rafiffarihan13/M.-Rafif-Farihan_09011282328042_SK3C_tugas-7-praktikum-sistem-operasi/blob/main/gambar/1.png)

## Langkah 2: Menginstal OpenSSH
OpenSSH belum terinstal di sistem, sehingga perlu diinstal secara manual. Untuk melakukannya, ketik perintah berikut di terminal:
```bash
sudo apt install openssh-server
```
Instalasi semua komponen yang diperlukan akan dimulai. Jawablah "Ya" untuk semua permintaan yang muncul di sistem.
![Menginstal OpenSSH](https://github.com/Rafiffarihan13/M.-Rafif-Farihan_09011282328042_SK3C_tugas-7-praktikum-sistem-operasi/blob/main/gambar/2.png)

## Langkah 3: Mengaktifkan Layanan SSH
Setelah instalasi selesai, layanan yang baru saja diinstal perlu diaktifkan dengan menggunakan perintah berikut:
```bash
sudo systemctl enable --now ssh
```
![Mengaktifkan Layanan SSH](https://github.com/Rafiffarihan13/M.-Rafif-Farihan_09011282328042_SK3C_tugas-7-praktikum-sistem-operasi/blob/main/gambar/3.png)

## Langkah 4: Memverifikasi Status Layanan
Untuk memastikan bahwa layanan telah diaktifkan dan berjalan dengan sukses, ketikkan perintah berikut:
```bash
sudo systemctl status ssh
```
Output yang dihasilkan seharusnya menunjukkan `Active: active (running)`, yang menandakan bahwa layanan berhasil dijalankan.
![Status Layanan SSH](https://github.com/Rafiffarihan13/M.-Rafif-Farihan_09011282328042_SK3C_tugas-7-praktikum-sistem-operasi/blob/main/gambar/4.png)

## Langkah 5: Memeriksa Firewall
Sebelum menghubungkan ke server melalui SSH, penting untuk memeriksa firewall agar dikonfigurasi dengan benar. Dalam kasus ini, jika sudah menginstal UFW, gunakan perintah berikut:
```bash
sudo ufw status
```
Pada output, akan terlihat apakah lalu lintas SSH diizinkan. Jika tidak tercantum, perlu mengizinkan koneksi SSH yang masuk. Perintah berikut akan membantu:
```bash
sudo ufw allow ssh
```
![Memeriksa Firewall](https://github.com/Rafiffarihan13/M.-Rafif-Farihan_09011282328042_SK3C_tugas-7-praktikum-sistem-operasi/blob/main/gambar/5.png)

## Langkah 6: Menghubungkan ke Server
Setelah menyelesaikan semua langkah sebelumnya, dapat masuk ke server menggunakan protokol SSH. Untuk melakukan ini, perlu memiliki alamat IP atau nama domain server serta nama pengguna yang telah dibuat di server. Pada baris terminal, masukkan perintah berikut:
```bash
ssh username@IP_address
```
![Menghubungkan ke Server](https://github.com/Rafiffarihan13/M.-Rafif-Farihan_09011282328042_SK3C_tugas-7-praktikum-sistem-operasi/blob/main/gambar/6.png)

--- 

