FROM php:7.2-fpm-alpine
RUN apk add --no-cache \
        freetype-dev libpng-dev libjpeg-turbo-dev libmcrypt-dev \
        freetype libpng libjpeg-turbo libmcrypt && \
    docker-php-ext-configure gd \
        --with-freetype-dir=/usr/include/ \
        --with-png-dir=/usr/include/ \
        --with-jpeg-dir=/usr/include/ && \
    docker-php-ext-install gd mysqli pdo_mysql zip && \
    apk del --no-cache \
        freetype-dev libpng-dev libjpeg-turbo-dev libmcrypt-dev
