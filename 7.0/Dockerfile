FROM php:7.0.33-alpine3.7

RUN apk --update add --no-cache --virtual .build-deps $PHPIZE_DEPS \
    && apk add --no-cache git openssh-client ncurses gnupg libmcrypt-dev libxml2-dev libzip-dev mysql-client vim p7zip \
    && docker-php-ext-install zip bcmath mcrypt soap pdo_mysql \
    && pecl install xdebug-2.7.2 && docker-php-ext-enable xdebug \
    && php -r "readfile('https://getcomposer.org/installer');" | php -- --install-dir=/usr/bin/ --filename=composer --version=2.2.14 \
    && wget -q -O /usr/local/bin/phive https://github.com/phar-io/phive/releases/download/0.12.1/phive-0.12.1.phar && chmod +x /usr/local/bin/phive \
    && apk del .build-deps \
    && cp "$PHP_INI_DIR/php.ini-development" "$PHP_INI_DIR/php.ini" \
    && echo "alias ll='ls -l'" >> "$HOME/.profile" \
    && echo "export PS1='🐳 \[\033[1;36m\]\h \[\033[1;34m\]\w\[\033[0;35m\] \[\033[1;36m\]# \[\033[0m\]'" >> "$HOME/.profile"
