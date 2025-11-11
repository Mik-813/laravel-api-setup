FROM richarvey/nginx-php-fpm:3.1.6

COPY ./environment/nginx/default.conf /etc/nginx/sites-enabled/default.conf

COPY . /var/www/api

RUN chown -R www-data:www-data /var/www/api \
 && chmod -R 775 /var/www/api/storage

RUN COMPOSER_ALLOW_SUPERUSER=1 composer setup -d /var/www/api --no-interaction

CMD php-fpm & nginx -g 'daemon off;'