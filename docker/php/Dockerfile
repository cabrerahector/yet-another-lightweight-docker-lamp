ARG PHP_VERSION

FROM php:${PHP_VERSION}-fpm-alpine

# Install extensions
RUN docker-php-ext-install mysqli \
    && docker-php-ext-install pdo \
    && docker-php-ext-install pdo_mysql \
    && docker-php-ext-install opcache
