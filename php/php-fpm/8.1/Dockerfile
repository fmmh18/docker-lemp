FROM phpdockerio/php:8.1-fpm
WORKDIR "/var/www"

RUN apt-get update \
    && apt-get -y --no-install-recommends install \
    php-pear \
    php8.1-dev \
    wget  \
    make \
    curl \
    nano \
    php8.1-bz2 \ 
    php8.1-gd \ 
    php8.1-imagick \ 
    php8.1-imap \ 
    php8.1-ldap \ 
    php8.1-mysql \  
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

