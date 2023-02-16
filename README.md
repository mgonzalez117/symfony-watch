# symfony-watch
Technological watch base for projects with symfony

## Fork the project

This project is intended to be forked for each new watch need.

## What is inside

- Docker development stack
  
  * `symfony` container, php-fpm and app sources
  * `nginx` container, the webserver, listen on port `8000` by default    

- Symfony **6.2** skeleton (--webapp)
- Composer
- GrumpPHP : PHPStan, PHPCsFixer, Tests checker
- PHPUnit

## How to use

* Copy file `.php-cs-fixer.dist.php` to `.php-cs-fixer.php`
* Change `GIT_USER_EMAIL` and `GIT_USER_NAME` values in `docker-compose.yml`
* Configure `./docker/.env`, it is the env file for the `symfony` container
* Configure `./docker/.env.nginx`, it is the env file for the `nginx` container
* Start docker containers : `docker-compose up` (or `docker-compose build` && `docker-compose start`)
* use `docker exec -it symfony bash` to have a shell into the `symfony` container :
    * `sf` alias or `php bin/console` to use the Symfony console
    * `composer` to use composer