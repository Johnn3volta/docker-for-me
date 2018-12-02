FROM php:7.1-apache

RUN apt-get update && apt-get install -y \
    libmagickwand-dev --no-install-recommends \
    && pecl install imagick \
	&& docker-php-ext-enable imagick \
    && docker-php-ext-install pdo_mysql \
    && a2enmod rewrite \
    && usermod -u 1000 www-data \
    && rm -rf /var/lib/apt/lists/*
