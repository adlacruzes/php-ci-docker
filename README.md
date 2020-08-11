# PHP CI Docker images

[![Minimum PHP Version](https://img.shields.io/badge/php-%3E%3D%207.0-8892BF.svg?style=square)](https://php.net/)
[![Build Status](https://travis-ci.org/adlacruzes/php-ci-docker.svg?branch=master)](https://travis-ci.org/adlacruzes/php-ci-docker)
[![Docker pulls](https://img.shields.io/docker/pulls/adlacruzes/php-ci?style=square)](https://hub.docker.com/r/adlacruzes/php-ci)
[![Docker build status](https://img.shields.io/docker/cloud/build/adlacruzes/php-ci?style=square)](https://hub.docker.com/r/adlacruzes/php-ci/builds)

Docker images for PHP based on the [official PHP Alpine images](https://hub.docker.com/r/_/php/).

These images contain the basic requirements for use with continuous integration in most projects.

## Images

|     | alpine | php    | composer | phive  | xdebug | size                                                                | layers
| --- | :---:  | :---:  | :---:    | :---:  | :---:  | :---:                                                               | :---:
| 7.0 | 3.7    | 7.0.33 | 1.10.10  | 0.12.1 | 2.7.2  | ![](https://img.shields.io/docker/image-size/adlacruzes/php-ci/7.0?style=square) | ![](https://img.shields.io/microbadger/layers/adlacruzes/php-ci/7.0?style=square)
| 7.1 | 3.10   | 7.1.33 | 1.10.10  | 0.13.2 | 2.9.6  | ![](https://img.shields.io/docker/image-size/adlacruzes/php-ci/7.1?style=square) | ![](https://img.shields.io/microbadger/layers/adlacruzes/php-ci/7.1?style=square)
| 7.2 | 3.12   | 7.2.33 | 1.10.10  | 0.13.2 | 2.9.6  | ![](https://img.shields.io/docker/image-size/adlacruzes/php-ci/7.2?style=square) | ![](https://img.shields.io/microbadger/layers/adlacruzes/php-ci/7.2?style=square)
| 7.3 | 3.12   | 7.3.20 | 1.10.10  | 0.13.2 | 2.9.6  | ![](https://img.shields.io/docker/image-size/adlacruzes/php-ci/7.3?style=square) | ![](https://img.shields.io/microbadger/layers/adlacruzes/php-ci/7.3?style=square)
| 7.4 | 3.12   | 7.4.8  | 1.10.10  | 0.13.2 | 2.9.6  | ![](https://img.shields.io/docker/image-size/adlacruzes/php-ci/7.4?style=square) | ![](https://img.shields.io/microbadger/layers/adlacruzes/php-ci/7.4?style=square)

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
