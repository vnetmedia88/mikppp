# 🚀 Deploy Mikhmon v3 via Docker

Panduan lengkap untuk menginstall dan menjalankan Mikhmon v3 menggunakan Docker. Cocok untuk pemula dan praktis untuk VPS / STB UBUNTU/ CASA OS!

---

## 📦 1. Install Git & Docker

```bash
apt update && apt install -y git docker.io
```

---

## ⬇️ 2. Clone Repo Mikhmon

```bash
git clone https://github.com/vnetmedia88/mikppp.git
cd mikppp
```

---

## 🛠️ 3. Buat Dockerfile

```bash
nano Dockerfile
```

Isi file `Dockerfile` dengan:

```Dockerfile
FROM php:7.4-apache
RUN a2enmod rewrite
COPY . /var/www/html/
EXPOSE 80
CMD ["apache2-foreground"]
```

Simpan: tekan `CTRL+O`, ENTER, lalu `CTRL+X`.

---

## 🧱 4. Build Docker Image

```bash
docker build -t mikppp .
```

---

## 🚀 5. Jalankan Container

```bash
docker run -d -p 1001:80 \
  -v $(pwd):/var/www/html \
  --name mikppp-container \
  mikppp
```

---

## 🔐 6. Atur Izin Akses Folder

```bash
sudo chown -R www-data:www-data $(pwd)
sudo chmod -R 755 $(pwd)
```

---

## ✅ 7. Cek Container

```bash
docker ps
```

---

## 🌐 8. Akses Mikhmon via Browser

Buka browser dan akses:

```
http://<IP-VPS>:1001
```

Ganti `<IP-VPS>` dengan alamat IP publik VPS kamu.

---

Mikhmon siap digunakan dari container Docker.  
Untuk login default, username: `admin`, password: `admin`.

---


## 🎉 kalau mau buat lg 
cp -r mikppp paijo

cd /root/paijo

docker build -t paijo .

docker run -d --name paijo-container -p 1002:80 -v $(pwd):/var/www/html paijo


© 2025 vnetmedia88
