FROM php:8.0-fpm

WORKDIR /var/www

# Install dependencies
RUN apt-get update && apt-get install -y libmcrypt-dev && docker-php-ext-install pdo pdo_mysql
RUN apt-get update && apt-get install -y \
    build-essential \
    libpng-dev \
    libjpeg62-turbo-dev \
    libfreetype6-dev \
    locales \
    zip \
    jpegoptim optipng pngquant gifsicle \
    vim \
    unzip \
    git \
    curl


# instala composer en el contenedor
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# da permisos para editar los archivos en esta ruta del container
ADD . /var/www
COPY --chown=www-data:www-data . /var/www