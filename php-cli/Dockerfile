FROM php:7.1.9

# for xdebug by CLI with PhpStorm
ENV PHP_IDE_CONFIG "serverName=Docker"

ADD php.ini /usr/local/etc/php/conf.d/php.ini

RUN echo "deb http://deb.debian.org/debian jessie main" > /etc/apt/sources.list &&\
    echo "deb http://security.debian.org jessie/updates main" >> /etc/apt/sources.list &&\
    apt-get update && apt-get install -y \
    libmcrypt-dev \
    mysql-client \
    zip \
    unzip \
    git \
    libzip-dev \
    vim \
    libfreetype6-dev \
    libjpeg62-turbo-dev \
    libpng12-dev

RUN git clone https://github.com/phpredis/phpredis.git /usr/src/php/ext/redis

RUN docker-php-ext-install zip bcmath pdo_mysql mysqli mbstring redis gd

RUN pecl install xdebug \ docker-php-ext-enable xdebug
