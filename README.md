## 1 Clone/Download Repository
```
git clone https://github.com/darshandomadiya/laravel_1.git
```

## 2 Run composer update
``` 
composer update 
```
## 3 Create Database
```
create database laravel1;
```
## 4 Run migration
```
php artisan migrate
```
## 5 Give Read/Write permission
```
sudo chmod 777 -R storage
sudo chmod 777 -R public/images/ (Create images directory if not created automatically)
```
## 6 Create Virtual Host
```
<VirtualHost *:80>
	DocumentRoot /var/www/html/laravel_1/public
	ServerName   local.laravel1.com
	<Directory "/var/www/html/laravel_1/public">
		AllowOverride All
		Options Indexes FollowSymLinks MultiViews
		Order allow,deny
	    allow from all
	</Directory>
	ErrorLog ${APACHE_LOG_DIR}/error.log
	CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```
## 7 Add entry into host file
```
127.0.0.1 local.laravelemp.com
```
## 8 Apache Restart
```
sudo service apache2 restart
```
## 9 open browser and hit local.laravel1.com
Enjoy!!
