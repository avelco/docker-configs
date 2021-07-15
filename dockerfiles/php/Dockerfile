FROM php:8.0-fpm

WORKDIR /var/www
# algunas configuraciones para que funcione el contenedor
RUN docker-php-ext-install pdo pdo_mysql
RUN apt-get update && apt-get install -y libmcrypt-dev && docker-php-ext-install pdo_mysql

# instala composer en el contenedor
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# da permisos para editar los archivos en esta ruta del container
ADD . /var/www
COPY --chown=www-data:www-data . /var/www