# asistencia-inei

git clone https://github.com/franklinvillegas/asistencia-inei.git


cd asistencia-inei

composer install

nano .env
--configure env variables

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=bd_asistencia-inei
DB_USERNAME=root
DB_PASSWORD=

php artisan migrate

php artisan key:generate
php artisan passport:keys
php artisan passport:client --personal
php artisan config:cache
chown -R www-data:www-data storage
chmod -R 775 storage
