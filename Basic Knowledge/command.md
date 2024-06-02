
# Command Line
Command-line adalah antarmuka pengguna yang memungkinkan pengguna untuk berinteraksi dengan sistem operasi melalui baris perintah. Berikut adalah beberapa perintah command-line yang sering digunakan:

---
### sudo (Superuser Do)
>Perintah `sudo` digunakan agar bisa menjalankan perintah dengan hak akses superuser/root. 

Contoh:
```shell
sudo apt-get update
sudo apt-get upgrade
```
---

### apt-get (APT Package Manager)
>Perintah `apt-get` digunakan untuk mengelola paket perangkat lunak menggunakan APT (Advanced Package Tool). 

Contoh
```shell
sudo apt-get install git
```
---

### ufw (Uncomplicated Firewall):
>Perintah `ufw` digunakan untuk mengelola firewall atau port pada sistem Ubuntu.

Contoh
```shell
sudo ufw enable
sudo ufw allow 22
sudo ufw reload
sudo ufw status
```
---

### screen:
>Perintah `screen` digunakan untuk membuat sesi terminal baru atau mengelola sesi terminal yang ada. bisa juga disebut agar bisa menjalankan di latar belakang.

Contoh:

>Untuk membuat terminal atau latar belakang baru
```shell
screen -S mysession
```
>Untuk melanjutkan atau membuka sesi terminal yang ada:
```
screen -R mysession
```
>Untuk melihat daftar sesi terminal yang ada:
```
screen -ls
```
>Untuk keluar dari sesi terminal tanpa menghentikan proses yang berjalan di dalamnya:
tekan `Ctrl` + `a`, lalu tekan `d`

---

### cd (Change Directory):
>Perintah `cd` digunakan untuk berpindah dari satu direktori ke direktori lain di sistem file atau berfungsi untuk membuka folder.

Contoh 
```shell
cd /home/Documents
cd node
```
---

### ls (List):

> Perintah `ls` digunakan untuk menampilkan daftar file dan direktori dalam direktori saat ini.

Contoh
```shell
ls -l
```
---

### mkdir (Make Directory):

>Perintah `mkdir` digunakan untuk membuat direktori/folder baru di sistem file.

Contoh:
```shell
mkdir my_directory
```
---

### cp (Copy):
>Perintah `cp` digunakan untuk menyalin file atau direktori dari satu lokasi ke lokasi lain di sistem file.

Contoh:
```
cp file1.txt /path/to/destination
```
---

### rm -rf (Remove Recursive Force):
>Perintah `rm -rf` digunakan untuk menghapus file atau direktori secara rekursif dan paksa dari sistem file.

Contoh:
```
rm -rf my_directory
```
---

### mv (Move):
>Perintah `mv` digunakan untuk memindahkan file atau direktori dari satu lokasi ke lokasi lain di sistem file.

Contoh:
```
mv file1.txt /path/to/destination
```
---

### nano (Text Editor):
>Perintah `nano` digunakan untuk membuka dan mengedit file teks dari baris perintah.

Contoh:
>Membuka dan memgedit file
```shell
nano myfile.txt
```
>Setelah itu `CTRL + O + Enter` untuk menyimpan dan `CTRL + X + Y` untuk keluar
---

### wget (Web Get):
>Perintah `wget` digunakan untuk mengunduh file dari internet.

Contoh:
```shell
wget https://example.com/file.zip
```
---

### curl (Client URL):
>Perintah `curl` digunakan untuk mengunduh atau mengunggah data menggunakan protokol berbeda.

Contoh:
```shell
curl -O https://example.com/file.zip
```
---

### tar (Tape Archive):
>Perintah `tar` digunakan untuk mengarsipkan file atau direktori di sistem file.

Contoh:
```shell
tar -czvf archive.tar.gz my_directory
```
---

### chmod (Change Mode):
>Perintah `chmod` digunakan untuk mengubah izin file atau direktori.

Contoh:
```shell
chmod 755 myfile.txt
```
---

### htop (Interactive Process Viewer):
>Perintah `htop` digunakan untuk menampilkan informasi tentang penggunaan CPU dan memori serta proses yang sedang berjalan secara interaktif.

Contoh:
```shell
htop
```

### netstat (Network Statistics):
>Perintah `netstat` digunakan untuk menampilkan informasi tentang koneksi jaringan, routing, dan antarmuka jaringan.

Contoh:

```shell
netstat -an
```
---

### ps (Process Status):
>Perintah `ps` digunakan untuk menampilkan proses yang sedang berjalan.

Contoh:

```shell
docker ps -a
```
---

### df (Disk Free):
>Perintah `df` digunakan untuk menampilkan ruang disk yang tersedia dan digunakan.

Contoh:

```
df -h
```
---
