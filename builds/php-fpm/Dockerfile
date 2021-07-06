ARG version
FROM php:${version}-fpm-alpine

RUN \
  apk add --no-cache libjpeg-turbo libpng libzip &&\
  apk add --no-cache --virtual .build-deps libjpeg-turbo-dev libpng-dev libzip-dev &&\
  docker-php-ext-configure gd --with-jpeg=/usr &&\
  docker-php-ext-install gd mysqli opcache zip &&\
  apk del .build-deps

COPY php-fpm.conf /usr/local/etc/php-fpm.d/
COPY opcache.conf /usr/local/etc/php/
