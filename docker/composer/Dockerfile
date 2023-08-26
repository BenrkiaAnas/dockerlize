FROM composer:latest

RUN addgroup --system --gid 1000 laravel && adduser --system --ingroup laravel --shell /bin/sh --home /var/www/html --uid 1000 laravel

WORKDIR /var/www/html