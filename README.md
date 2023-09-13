# docker_laravel

```
git init
git remote add origin git@github.com:ishipilov/docker_laravel.git
git pull
git checkout main
git pull
```
```
mkdir app && cd app
git init
git remote add origin git@github.com:ishipilov/laravel8.40
git pull
git checkout main
git pull
```
```
docker exec -it laravel840-apache-1 bash
chgrp -R www-data storage bootstrap/cache && chmod -R ug+rwx storage bootstrap/cache && chown -R www-data:www-data storage/logs
php artisan key:generate
php artisan migrate --seed
```
