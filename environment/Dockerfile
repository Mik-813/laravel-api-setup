FROM richarvey/nginx-php-fpm:3.1.6

COPY ./nginx/default.conf /etc/nginx/sites-enabled/default.conf

CMD php-fpm & nginx -g 'daemon off;'