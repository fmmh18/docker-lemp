FROM phpdockerio/php7-fpm:latest
WORKDIR "/var/www"

RUN apt-get update \
    && apt-get -y --no-install-recommends install \
    php-pear \
    php7.0-dev \
    unixodbc \
    unixodbc-dev \
    build-essential \
    wget  \
    make \
    curl \
    nano \
    php7.0-bz2 \ 
    php7.0-gd \ 
    php7.0-imagick \ 
    php7.0-imap \ 
    php7.0-ldap \ 
    php7.0-mysql \ 
    php7.0-pgsql \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*


