FROM phpdockerio/php:7.2-fpm
WORKDIR "/var/www"

RUN apt-get update \
    && apt-get -y --no-install-recommends install \
    php7.2-bz2 \ 
    php7.2-gd \ 
    php7.2-imagick \ 
    php7.2-imap \ 
    php7.2-ldap \ 
    php7.2-mysql \ 
    php7.2-pgsql \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

