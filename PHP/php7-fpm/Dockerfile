FROM php:7.0-fpm-alpine
RUN apk add --no-cache \
        freetype-dev libpng-dev libjpeg-turbo-dev libmcrypt-dev \
        freetype libpng libjpeg-turbo libmcrypt libxml2-dev && \
    docker-php-ext-configure gd \
        --with-freetype-dir=/usr/include/ \
        --with-png-dir=/usr/include/ \
        --with-jpeg-dir=/usr/include/ && \
    docker-php-ext-install gd mcrypt mysqli pdo_mysql zip soap && \
    apk del --no-cache \
        freetype-dev libpng-dev libjpeg-turbo-dev libmcrypt-dev
