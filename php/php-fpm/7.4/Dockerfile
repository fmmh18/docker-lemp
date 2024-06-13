FROM phpdockerio/php:7.4-fpm
WORKDIR "/var/www"

RUN apt-get update \
    && apt-get -y --no-install-recommends install \
    php-pear \
    php7.4-dev \
    unixodbc \
    unixodbc-dev \
    build-essential \
    wget  \
    make \
    curl \
    nano \
    php7.4-bz2 \ 
    php7.4-gd \ 
    php7.4-imagick \ 
    php7.4-imap \ 
    php7.4-ldap \ 
    php7.4-pgsql \
    php7.4-mysql 

RUN curl https://packages.microsoft.com/keys/microsoft.asc | apt-key add - \
    && curl https://packages.microsoft.com/config/ubuntu/18.04/prod.list > /etc/apt/sources.list.d/mssql-release.list
RUN apt-get update && ACCEPT_EULA=Y apt-get install -y \
    msodbcsql17 \
    unixodbc-dev \
    && rm -rf /var/lib/apt/lists/*
RUN pecl install sqlsrv-5.9.0 \
    && pecl install pdo_sqlsrv-5.9.0
RUN printf "; priority=20\nextension=sqlsrv.so\n" > /etc/php/7.4/mods-available/sqlsrv.ini \
    && printf "; priority=30\nextension=pdo_sqlsrv.so\n" > /etc/php/7.4/mods-available/pdo_sqlsrv.ini
RUN apt-get clean 
RUN phpenmod -v 7.4 sqlsrv pdo_sqlsrv
RUN rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

