FROM php:7.4.9-fpm
COPY ./phpredis-3.1.3.tar.gz  /tmp/redis.tar.gz
COPY ./swoole-src-master.tar.gz  /tmp/swoole-src-master.tar.gz
RUN apt-get update && apt-get -y install libzip-dev libpng-dev libjpeg-dev  libfreetype6-dev libmcrypt-dev && \
    docker-php-ext-configure gd &&  \
    tar xfz /tmp/redis.tar.gz  &&  \
    rm -r /tmp/redis.tar.gz  &&  \
    mkdir -p /usr/src/php/ext  &&  \
    mv phpredis-3.1.3 /usr/src/php/ext/redis  && \
    tar xfz /tmp/swoole-src-master.tar.gz && \
    rm -r /tmp/swoole-src-master.tar.gz && \
    mv swoole-src-master /usr/src/php/ext/swoole && \

RUN apt install libonig-dev  && \
    docker-php-ext-install pdo_mysql mysqli redis  gd  mbstring zip  
WORKDIR /usr/share/nginx/html

