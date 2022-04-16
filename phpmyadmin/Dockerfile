FROM php:8.0.3-fpm-buster

RUN apt-get update \
 && apt-get install -y --no-install-recommends \
  libzip-dev \
  unzip \
  git \
 # phpがmysqlに接続するのに必要なドライバ
 && docker-php-ext-install pdo_mysql        
# Composerのインストール   
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer