
# Apps Tools
Untuk membangun dan menjalankan node validator, Anda memerlukan beberapa alat dasar seperti Rust, Git, Docker, dan alat lainnya tergantung pada kebutuhan spesifik proyek Anda. Berikut adalah langkah-langkah untuk menginstal beberapa alat dasar yang umum digunakan:

## **1. Rust**
Rust adalah bahasa pemrograman yang digunakan untuk membangun aplikasi blockchain. Rust adalah bahasa pemrograman sistem yang dirancang untuk kinerja tinggi dan keamanan memori. Rust memastikan bahwa program yang ditulis bebas dari kesalahan memori seperti dereferensi pointer null atau kondisi balapan (race conditions). Anda dapat menginstal Rust menggunakan rustup, manajer versi Rust. Buka terminal dan jalankan perintah berikut:

```shell
# Download and install
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs/ | sh

# Activate rust
source $HOME/.cargo/env
```

Ikuti instruksi pada layar untuk menyelesaikan instalasi. Setelah instalasi selesai, pastikan Rust sudah terpasang dengan menjalankan perintah:

```shell
rustc --version
```
---

## **2. Git**
Git digunakan untuk mengelola kode sumber. Untuk menginstal Git, jalankan perintah berikut di terminal:

```shell
# Download and install
sudo apt update & sudo apt upgrade -y
sudo apt install git
```

Setelah instalasi selesai, Anda dapat memeriksa versi Git dengan perintah:

```
git --version
```
---

## **3. Clang**
Clang adalah kompiler yang merupakan bagian dari proyek LLVM. Clang digunakan untuk mengkompilasi bahasa pemrograman C, C++, dan Objective-C. Clang dirancang untuk memberikan kesalahan dan peringatan yang jelas dan mudah dimengerti, menjadikannya pilihan populer di kalangan pengembang perangkat lunak. Untuk menginstal Git, jalankan perintah berikut di terminal:

```shell
# Download and install
sudo apt update & sudo apt upgrade -y
sudo apt install clang
```

Setelah instalasi selesai, Anda dapat memeriksa versi Git dengan perintah:
```
clang --version
```
---

## **4. Node.js**
Node.js adalah lingkungan runtime yang memungkinkan Anda menjalankan JavaScript di server, di luar browser. Ini dibangun di atas mesin JavaScript V8 milik Google Chrome. Node.js sangat efisien dan ringan karena menggunakan model I/O non-blocking dan event-driven, yang membuatnya sangat cocok untuk aplikasi real-time yang intensif data dan berjalan di perangkat yang terdistribusi.

Untuk menginstal Node.js di VPS yang menjalankan Ubuntu, ikuti langkah-langkah berikut:

```shell
# Download and install
sudo apt update & sudo apt upgrade -y
sudo apt install nodejs npm
```

Verifikasi instalasi dengan memeriksa versi Node.js dan npm:

```shell
node -v
npm -v
```
---

## **5. Docker dan Docker Compose**
#### Pengertian/Penjabaran Docker:
Docker adalah platform yang memungkinkan Anda untuk mengotomatisasi penyebaran aplikasi sebagai kontainer portabel, mandiri, dan ringan yang dapat berjalan secara konsisten di berbagai lingkungan. Docker memisahkan aplikasi dari infrastruktur, sehingga Anda dapat mengirimkan perangkat lunak dengan cepat.

### Pengertian/Penjabaran Docker Compose:
Docker Compose adalah alat untuk mendefinisikan dan menjalankan aplikasi Docker multi-kontainer. Dengan menggunakan file YAML, Anda dapat menentukan layanan, jaringan, dan volume yang diperlukan untuk aplikasi Anda. Docker Compose kemudian dapat digunakan untuk membuat dan mengelola seluruh aplikasi dengan satu perintah.

Untuk menginstal Docker dan Docker Compose di VPS yang menjalankan Ubuntu, ikuti langkah-langkah berikut:

```shell
# Add Docker's official GPG key:
sudo apt-get update && sudo apt-get upgrade -y
sudo apt-get install ca-certificates curl 
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources: 
echo \
"deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
$(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```

Once the Docker repository is added successfully, let’s install Docker and necessary components by using the below command:

```shell
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
Setelah instalasi selesai, Anda dapat memeriksa versi Docker dan Docker Compse dengan perintah:
```bash
docker --version
docker compose version
```
---
