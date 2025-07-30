# 🚀 Deploy Mikhmon lanjut 

Panduan lengkap untuk membuat lagi 

---

## 📦 1. buat folder baru

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
docker run -d --name royhan -p 1002:80 -v /var/www/html/royhan:/var/www/html php:7.4-apache
```

---

## ⬇️ 4. izin kan fille mikhmon
```bash
chown -R www-data:www-data /var/www/html/royhan
chmod -R 755 /var/www/html/royhan
chmod -R 777 /var/www/html/royhan
```

---
mikhmon baru sudah jalan dengan port 1002 sesuaikan dengan selera



