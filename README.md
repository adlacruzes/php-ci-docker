# PHP CI Docker images

[![Minimum PHP Version](https://img.shields.io/badge/php-%3E%3D%207.0-8892BF.svg?style=square)](https://php.net/)
[![Docker pulls](https://img.shields.io/docker/pulls/adlacruzes/php-ci?style=square)](https://hub.docker.com/r/adlacruzes/php-ci)
[![Docker build status](https://img.shields.io/docker/cloud/build/adlacruzes/php-ci?style=square)](https://hub.docker.com/r/adlacruzes/php-ci/builds)

Docker images for PHP based on the [official PHP Alpine images](https://hub.docker.com/r/_/php/).

These images contain the basic requirements for use with continuous integration in most projects.

## Images

|     | alpine | php    | composer | phive  | xdebug | size
| --- | :---:  | :---:  | :---:    | :---:  | :---:  | :---:
| 7.0 | 3.7    | 7.0.33 | 2.0.12 | 0.12.1 | 2.7.2  | ![](https://img.shields.io/docker/image-size/adlacruzes/php-ci/7.0?style=square)
| 7.1 | 3.10   | 7.1.33 | 2.0.12 | 0.13.5 | 2.9.8  | ![](https://img.shields.io/docker/image-size/adlacruzes/php-ci/7.1?style=square)
| 7.2 | 3.12   | 7.2.34 | 2.0.12 | 0.14.5 | 3.0.4  | ![](https://img.shields.io/docker/image-size/adlacruzes/php-ci/7.2?style=square)
| 7.3 | 3.13   | 7.3.27 | 2.0.12 | 0.14.5 | 3.0.4  | ![](https://img.shields.io/docker/image-size/adlacruzes/php-ci/7.3?style=square)
| 7.4 | 3.13   | 7.4.16 | 2.0.12 | 0.14.5 | 3.0.4  | ![](https://img.shields.io/docker/image-size/adlacruzes/php-ci/7.4?style=square)
| 8.0 | 3.13   | 8.0.3  | 2.0.12 | 0.14.5 | 3.0.4  | ![](https://img.shields.io/docker/image-size/adlacruzes/php-ci/8.0?style=square)

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

* **mysql-client** (https://mariadb.org based)
    
    CLI connection to mysql/mariadb

## Tags

Available tags:

* 7.0
* 7.1
* 7.2
* 7.3
* 7.4
* 8.0

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
