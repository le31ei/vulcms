FROM php:5.6-apache

MAINTAINER le31ei

RUN apt-get update && apt-get install -y \
    libfreetype6-dev \
    libjpeg62-turbo-dev \
    libpng-dev \
    libzip-dev \
    zip \
    && rm -rf /var/lib/apt/lists/*

RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install -j$(nproc) gd \
    && docker-php-ext-install pdo_mysql mysqli \
    && docker-php-ext-install zip

# 设置工作目录
WORKDIR /var/www/html

# 暴露 80 端口
EXPOSE 80
