FROM php:8.3-apache
RUN apt-get update && apt-get install -y \
    libjpeg62-turbo-dev \
    libpng-dev \
    libfreetype6-dev \
    libzip-dev \
    libicu-dev \
    libxml2-dev \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install \
        mysqli \
        pdo_mysql \
        gd \
        intl \
        zip \
        exif \
        bcmath \
        opcache \
    && docker-php-ext-enable mysqli pdo_mysql exif opcache
