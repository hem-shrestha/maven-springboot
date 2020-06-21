FROM 01shreeram/nginx:phpcomposer
ENV DEBIAN_FRONTEND=noninteractive
WORKDIR /var/www/html
COPY --chown=www-data:www-data . .
RUN if test -f 'composer.json'; then  composer install; fi
CMD [\"/bin/bash\", \"-c\", \"php-fpm7.2 -D && nginx -g 'daemon off;'\"]
