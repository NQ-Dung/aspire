FROM php:8.0-apache

RUN apt update \
        && apt install -y \
            g++ \
            libicu-dev \
            libpq-dev \
            libzip-dev \
            zip \
            zlib1g-dev \
        && docker-php-ext-install \
            intl \
            opcache \
            mysqli \
            pdo_mysql \
            pdo \
            pdo_pgsql \
            pgsql

RUN a2enmod rewrite headers

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /var/www/aspire
