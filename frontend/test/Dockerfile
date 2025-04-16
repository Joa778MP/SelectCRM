# Imagen base con Apache + PHP 7.4
FROM php:7.4-apache

# Instala extensiones necesarias para EspoCRM
RUN docker-php-ext-install mysqli pdo pdo_mysql

# Habilita mod_rewrite para URLs amigables
RUN a2enmod rewrite

# Copia todo el contenido del proyecto al servidor web
COPY . /var/www/html/

# Asigna permisos correctos
RUN chown -R www-data:www-data /var/www/html/ \
    && chmod -R 755 /var/www/html/

# Expone el puerto 80
EXPOSE 80
