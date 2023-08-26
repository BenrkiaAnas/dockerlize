# docker/php/Dockerfile
FROM php:8.1-fpm

ADD www.conf /usr/local/etc/php-fpm.d/www.conf

RUN addgroup --system --gid 1000 laravel && adduser --system --ingroup laravel --shell /bin/sh --home /var/www/html --uid 1000 laravel


RUN mkdir -p /var/www/html
RUN mkdir -p /var/www/storage
RUN mkdir -p /var/www/storage/framework
RUN mkdir -p /var/www/storage/framework/sessions

RUN chown laravel:laravel /var/www/html

WORKDIR /var/www/html

RUN apt-get update
RUN apt-get install -y openssl zip unzip git curl
RUN apt-get install -y libzip-dev libonig-dev libicu-dev
RUN apt-get install -y autoconf pkg-config libssl-dev

RUN docker-php-ext-install bcmath mbstring intl opcache

RUN docker-php-ext-install pdo pdo_mysql mysqli

