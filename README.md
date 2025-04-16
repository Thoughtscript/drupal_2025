# drupal_2025

[![](https://img.shields.io/badge/Alpine-Linux-yellow.svg)](https://hub.docker.com/_/drupal) 
[![](https://img.shields.io/badge/Apache-red.svg)](https://www.apache.org/) 
[![](https://img.shields.io/badge/Bitnami-MySQL-red.svg)](https://hub.docker.com/r/bitnami/mysql)
[![](https://img.shields.io/badge/PHP-8.4-purple.svg)](https://www.php.net/releases/8.4/en.php) 
[![](https://img.shields.io/badge/Docker-blue.svg)](https://www.docker.com/) 

Drupal on **LAMP** Stack. Just the very basics (**LAMP** Stack scaffold akin to [WAMP](https://sourceforge.net/projects/wampserver/)).

> Uses **Apache** (over [FPM](https://www.php.net/manual/en/install.fpm.php) distributions which **FPM** with **Nginx** to serve HTTP Request/Responses).

## Setup and Use

Docker Compose:
```bash
docker compose up
```

> Since we're using **Apache** the **Drupal** site is exposed directly at: http://localhost:8080

During the initial setup you'll be asked to configure the database. 
1. Pass in the values configured [here](docker-compose.yml) and make sure to use the Docker Network alias `mysql` instead of `localhost`.
2. The setup process will take up to a couple minutes to restart and launch the default site.

### Commands

Composer:
```bash
composer create-project drupal/recommended-project:10 drupal
```
> This is already done in the Docker Image.

## Resources and Links

1. https://hub.docker.com/_/drupal
1. https://savaslabs.com/blog/how-locally-install-new-drupal-10-site
1. https://forums.docker.com/t/how-do-i-run-the-official-drupal-image/117365
1. https://github.com/docker-library/drupal/blob/master/10.4/php8.4/apache-bullseye/Dockerfile