FROM 01shreeram/nginx:laravel

ENV DEBIAN_FRONTEND=noninteractive

WORKDIR /var/www/html

COPY composer.json .

COPY --chown=www-data:www-data . .

RUN composer install

CMD [\"/bin/bash\", \"-c\", \"php-fpm7.2 -D && nginx -g 'daemon off;'\"]
