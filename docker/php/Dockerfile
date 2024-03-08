FROM php:8.3-fpm

# Laravel の依存関係をインストール
RUN apt-get update && apt-get install -y \
    libpng-dev \
    libjpeg-dev \
    libfreetype6-dev \
    zip \
    unzip

# Composer をインストール
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

# PHP の拡張機能をインストール
RUN docker-php-ext-install pdo pdo_mysql gd

WORKDIR /var/www/html
