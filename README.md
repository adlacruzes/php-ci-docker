# PHP CI Docker images

[![Minimum PHP Version](https://img.shields.io/badge/php-%3E%3D%207.0-8892BF.svg?style=square)](https://php.net/)
[![Docker pulls](https://img.shields.io/docker/pulls/adlacruzes/php-ci?style=square)](https://hub.docker.com/r/adlacruzes/php-ci)

Docker images for PHP based on the [official PHP Alpine images](https://hub.docker.com/r/_/php/).

These images contain the basic requirements for use with continuous integration in most projects.

## Images

|     | alpine | php    | composer | phive  | xdebug | build | size
| --- | :---:  | :---:  | :---:    | :---:  | :---:  | :---: | :---:
| 7.0 | 3.7    | 7.0.33 | 2.1.6 | 0.12.1 | 2.7.2  | ![Github actions](https://github.com/adlacruzes/php-ci-docker/actions/workflows/php-7.0--docker-build-push.yml/badge.svg?branch=master) | ![](https://img.shields.io/docker/image-size/adlacruzes/php-ci/7.0?style=square)
| 7.1 | 3.10   | 7.1.33 | 2.1.6 | 0.13.5 | 2.9.8  | ![Github actions](https://github.com/adlacruzes/php-ci-docker/actions/workflows/php-7.1--docker-build-push.yml/badge.svg?branch=master) | ![](https://img.shields.io/docker/image-size/adlacruzes/php-ci/7.1?style=square)
| 7.2 | 3.12   | 7.2.34 | 2.1.6 | 0.14.5 | 3.0.4  | ![Github actions](https://github.com/adlacruzes/php-ci-docker/actions/workflows/php-7.2--docker-build-push.yml/badge.svg?branch=master) | ![](https://img.shields.io/docker/image-size/adlacruzes/php-ci/7.2?style=square)
| 7.3 | 3.14   | 7.3.33 | 2.1.6 | 0.15.0 | 3.0.4  | ![Github actions](https://github.com/adlacruzes/php-ci-docker/actions/workflows/php-7.3-docker-build-push.yml/badge.svg?branch=master) | ![](https://img.shields.io/docker/image-size/adlacruzes/php-ci/7.3?style=square)
| 7.4 | 3.13   | 7.4.26 | 2.1.6 | 0.15.0 | 3.0.4  | ![Github actions](https://github.com/adlacruzes/php-ci-docker/actions/workflows/php-7.4-docker-build-push.yml/badge.svg?branch=master) | ![](https://img.shields.io/docker/image-size/adlacruzes/php-ci/7.4?style=square)
| 8.0 | 3.13   | 8.0.12 | 2.1.6 | 0.15.0 | 3.0.4  | ![Github actions](https://github.com/adlacruzes/php-ci-docker/actions/workflows/php-8.0-docker-build-push.yml/badge.svg?branch=master) | ![](https://img.shields.io/docker/image-size/adlacruzes/php-ci/8.0?style=square)
| 8.1 | 3.14   | 8.1.0RC5 | 2.1.6 | 0.15.0 | 3.1.1  | ![Github actions](https://github.com/adlacruzes/php-ci-docker/actions/workflows/php-8.1-docker-build-push.yml/badge.svg?branch=master) | ![](https://img.shields.io/docker/image-size/adlacruzes/php-ci/8.1?style=square)

## Tags

Available tags:

* 7.0
* 7.1
* 7.2
* 7.3
* 7.4
* 8.0
* 8.1

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
