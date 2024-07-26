FROM php:8.1-apache

# Install dependencies
RUN apt-get update && apt-get install -y \
  git \
  curl \
  zip \
  unzip

# Enable Apache mod_rewrite
RUN a2enmod rewrite

# Install Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Set the document root
WORKDIR /var/www/html
