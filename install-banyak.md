# 🚀 Deploy Mikhmon lanjut 

Panduan lengkap untuk membuat lagi 

---

## 📦 1. buat folder baru

```bash
mkdir -p /var/www/html/paijo
```

---

## ⬇️ 2. Clone fille dari root
```bash
cp -r /root/mikppp/* /var/www/html/paijo/
```

---

## ⬇️ 3. buat nama container,port baru
```bash
docker run -d --name paijo -p 1002:80 -v /var/www/html/paijo:/var/www/html php:7.4-apache
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


© 2025 vnetmedia88



