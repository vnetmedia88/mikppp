buat mikhmon
mkdir -p /var/www/html/royhan
cp -r /root/mikppp/* /var/www/html/royhan/
docker run -d --name royhan -p 1001:80 -v /var/www/html/royhan:/var/www/html php:7.4-apache
chown -R www-data:www-data /var/www/html/royhan
chmod -R 755 /var/www/html/royhan
chmod -R 777 /var/www/html/royhan

