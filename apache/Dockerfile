FROM php:apache

RUN docker-php-ext-install \
    pdo_mysql \
    && a2enmod \
    rewrite

RUN sed -ri -e 's!/var/www/html!/var/www/html/public!g' /etc/apache2/sites-available/*.conf
RUN sed -ri -e 's!/var/www/html!/var/www/html/public!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf

#RUN chgrp -R www-data storage bootstrap/cache && chmod -R ug+rwx storage bootstrap/cache && chown -R www-data:www-data storage/logs

RUN apt update
RUN apt install mc -y
