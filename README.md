# PHP CI Docker images

Docker images for PHP based on the [official PHP Alpine images](https://hub.docker.com/r/_/php/).

These images contain the basic requirements for use with continuous integration in most projects.

## Overview

Additional installations made to the base image:

* **git** (https://git-scm.com) 
    
    Version control system

* **composer** (https://getcomposer.org) 
    
    Dependency manager

* **phive** (https://phar.io) 
    
    Phar installation manager

* **mcrypt** (https://pecl.php.net/package/mcrypt) 
    
    Encryption library (legacy purposes only)

* **xdebug** (https://xdebug.org) 
    
    Debugger

* **prestissimo** (https://github.com/hirak/prestissimo) 
    
    Composer parallel install plugin

## Tags

Available tags:

* 7.0
* 7.3

## Usage

Images are available at https://hub.docker.com/r/adlacruzes/php-ci

Download image:

```
docker pull adlacruzes/php-ci:TAG
```

Run container:

```
docker run -it adlacruzes/php-ci:TAG sh
```
