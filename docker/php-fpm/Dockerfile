FROM php:7.4-fpm

RUN apt-get update && apt-get install -y \
	libxml2-dev \
	git \
	zip \
	unzip \
	libpq-dev \ 
    && apt-get clean -y \
    && docker-php-ext-install soap pdo_pgsql

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
