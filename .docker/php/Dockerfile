FROM php:fpm-alpine3.18

RUN apk update && apk upgrade

RUN apk add bash

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer --version=2.7.2

RUN docker-php-ext-install pdo_mysql

ENV USERNAME=lfcf

RUN adduser -D lfcf && addgroup lfcf www-data

EXPOSE 9000

WORKDIR /var/www

ENTRYPOINT ["php-fpm"]