FROM php:7.4.0alpha2-alpine

RUN apk --update add --no-cache --virtual .build-deps $PHPIZE_DEPS \
    && apk add --no-cache git openssh-client ncurses gnupg libmcrypt-dev libxml2-dev mysql-client \
    && docker-php-ext-install bcmath soap pdo_mysql \
    && apk add --no-cache --virtual .build-deps-xdebug autoconf gcc libc-dev make \
    && git clone https://github.com/xdebug/xdebug.git && cd /xdebug && sh rebuild.sh && cd / && rm -rf /xdebug \
    && git clone https://github.com/php/pecl-encryption-mcrypt.git mcrypt && cd /mcrypt && phpize && ./configure && make && make install && cd / && rm -rf /mcrypt \
    && php -r "readfile('http://getcomposer.org/installer');" | php -- --install-dir=/usr/bin/ --filename=composer \
    && wget -q -O /usr/local/bin/phive https://phar.io/releases/phive.phar && chmod +x /usr/local/bin/phive \
    && composer global require hirak/prestissimo \
    && apk del .build-deps .build-deps-xdebug \
    && echo 'zend_extension="xdebug.so"' >> /usr/local/etc/php/conf.d/xdebug.ini \
    && echo 'extension="mcrypt.so"' > /usr/local/etc/php/conf.d/mcrypt.ini
