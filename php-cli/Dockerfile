FROM php:7.1.9

# for xdebug by CLI with PhpStorm
ENV PHP_IDE_CONFIG "serverName=Docker"


ADD php.ini /usr/local/etc/php/conf.d/php.ini

RUN apt-get update \
    && apt-get install -y libmcrypt-dev mysql-client \
    && apt-get install -y zip unzip git libzip-dev \
    && apt-get install -y vim

RUN git clone https://github.com/phpredis/phpredis.git /usr/src/php/ext/redis

RUN docker-php-ext-install zip bcmath pdo_mysql mysqli mbstring redis

RUN pecl install xdebug \ docker-php-ext-enable xdebug
