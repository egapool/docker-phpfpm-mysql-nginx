FROM php:7.1-fpm

ADD php.ini /usr/local/etc/php/conf.d/php.ini

RUN apt-get update \
  && docker-php-ext-install pdo_mysql mysqli mbstring
