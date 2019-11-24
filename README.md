# PHP CI Docker images

[![Minimum PHP Version](https://img.shields.io/badge/php-%3E%3D%207.0-8892BF.svg?style=flat-square)](https://php.net/)
[![Build Status](https://travis-ci.org/adlacruzes/php-ci-docker.svg?branch=master)](https://travis-ci.org/adlacruzes/php-ci-docker)

Docker images for PHP based on the [official PHP Alpine images](https://hub.docker.com/r/_/php/).

These images contain the basic requirements for use with continuous integration in most projects.

## Images

|              | 7.0    | 7.1    | 7.2    | 7.3    | 7.4       |
| :---:        | :---:  | :---:  | :---:  | :---:  | :---:     |
| alpine       | 3.7.1  | 3.10.3 | 3.10.3 | 3.10.3 | 3.10.3    | 
| php          | 7.0.33 | 7.1.33 | 7.2.25 | 7.3.11 | 7.4.0RC6  |
| composer     | 1.9.1  | 1.9.1  | 1.9.1  | 1.9.1  | 1.9.1     |
| git          | 2.15.3 | 2.22.0 | 2.22.0 | 2.22.0 | 2.22.0    |
| phive        | 0.12.1 | 0.13.2 | 0.13.2 | 0.13.2 | 0.13.2    |
| xdebug       | 2.8.0  | 2.8.0  | 2.8.0  | 2.8.0  | 2.8.0     |

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

* **mysql-client** (https://mariadb.org based)
    
    CLI connection to mysql/mariadb

## Tags

Available tags:

* 7.0
* 7.1
* 7.2
* 7.3
* 7.4

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
