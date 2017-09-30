FROM php:7.0-fpm-alpine

RUN apk add --no-cache less
RUN docker-php-ext-install mysqli pdo_mysql

WORKDIR /app

ENTRYPOINT ["php", "artisan"]
CMD ["--help"]
