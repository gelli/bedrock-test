FROM php:8.1-fpm-alpine3.16

RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli

# Copy the php config file
COPY ./docker/php/php-fpm.conf /usr/local/etc/php-fpm.d/www.conf

VOLUME ["/app"]