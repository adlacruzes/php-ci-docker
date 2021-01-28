FROM php:7.1.33-alpine3.10

RUN apk --update add --no-cache --virtual .build-deps $PHPIZE_DEPS \
    && apk add --no-cache git openssh-client ncurses gnupg libmcrypt-dev libxml2-dev libzip-dev mysql-client mariadb-connector-c \
    && docker-php-ext-install zip bcmath mcrypt soap pdo_mysql \
    && pecl install xdebug-2.9.8 && docker-php-ext-enable xdebug \
    && php -r "readfile('http://getcomposer.org/installer');" | php -- --install-dir=/usr/bin/ --filename=composer --version=1.10.20 \
    && wget -q -O /usr/local/bin/phive https://github.com/phar-io/phive/releases/download/0.13.5/phive-0.13.5.phar && chmod +x /usr/local/bin/phive \
    && composer global require hirak/prestissimo \
    && apk del .build-deps \
    && cp "$PHP_INI_DIR/php.ini-development" "$PHP_INI_DIR/php.ini" \
    && echo "alias ll='ls -l'" >> "$HOME/.profile" \
    && echo "export PS1='🐳 \[\033[1;36m\]\h \[\033[1;34m\]\w\[\033[0;35m\] \[\033[1;36m\]# \[\033[0m\]'" >> "$HOME/.profile"
