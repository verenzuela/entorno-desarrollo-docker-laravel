FROM php:7.2.22-fpm-stretch

RUN apt-get update && apt-get install -y \
    git \
    libmcrypt-dev \
    libfreetype6-dev \
    libjpeg62-turbo-dev \
    libpng-dev \
    mysql-client libmagickwand-dev --no-install-recommends \
    libzip-dev \
    && pecl install mcrypt-1.0.2 \
    && docker-php-ext-enable mcrypt \
    && pecl install imagick \
    && pecl install zip \
    && docker-php-ext-enable imagick \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install gd \
    && docker-php-ext-install pdo_mysql \
    && apt-get install -y zlib1g-dev libicu-dev g++ \
    && docker-php-ext-configure intl \
    && docker-php-ext-install intl

    ENV TZ=America/Los_Angeles
    RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

ADD php/uploads.ini /usr/local/etc/php/conf.d/uploads.ini

RUN echo "extension=zip.so" >> /usr/local/etc/php/conf.d/docker-php-ext-zip.ini