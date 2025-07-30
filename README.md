# 🚀 Deploy Mikhmon v3 via Docker

Panduan lengkap untuk menginstall dan menjalankan Mikhmon v3 menggunakan Docker. Cocok untuk pemula dan praktis untuk VPS / STB UBUNTU!

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

## 🛠️ 3. Buat folder docker manual di var/www/html/namafolder ( saya contoh pkai royhan)

```bash
mkdir -p /var/www/html/royhan
```

---

## ⬇️ 2. Clone fille dari root
```bash
cp -r /root/mikppp/* /var/www/html/royhan/
```

---

## ⬇️ 3. buat nama container,port baru
```bash
docker run -d --name royhan -p 1001:80 -v /var/www/html/royhan:/var/www/html php:7.4-apache
```

---

## 🔐 6. Atur Izin Akses Folder mikhmon

```bash
chown -R www-data:www-data /var/www/html/royhan
chmod -R 755 /var/www/html/royhan
chmod -R 777 /var/www/html/royhan
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
Untuk login default, username: `mikhmon`, password: `1234`.

---



© 2025 vnetmedia88



