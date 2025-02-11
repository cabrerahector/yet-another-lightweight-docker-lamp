ARG PHP_VERSION=8.1

FROM php:${PHP_VERSION}-fpm-alpine

# Install dependencies
RUN apk add --no-cache --update \
    freetype-dev \
    libjpeg-turbo-dev \
    libwebp-dev \
    libpng-dev

# Install extensions
RUN docker-php-ext-install mysqli \
    && docker-php-ext-install pdo \
    && docker-php-ext-install pdo_mysql \
    && docker-php-ext-install opcache \
    && docker-php-ext-configure gd --with-freetype --with-webp --with-jpeg \
    && docker-php-ext-install gd
