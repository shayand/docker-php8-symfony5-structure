# DOCKER PHP 8 Symfony Structure with ability to debug and profile

This is a docker compose project for developing code with PHP 8 and mariadb
10.4

## Summary
This package is built for development of PHP Symfony framework project. We also try to gather things and containers that
used to  implement **CQRS** architectures

* Main Goal: **`A flexible tool for building and profiling Symfony framework with hands on CQRS `**
* Includes:
    * `PHP 8.4` PHP FPM
    * `NGINX` latest veriosn of alpine nginx
    * `MySQL 8.0.23` The most common version of mariaDB
    * `Redis Driver` the Redis driver of PHP
    * `XDebug` ability to debug project with XDebug
    * `Blackfire Agent` ability to profile code and request with profiller
    * `Cron` an alpine container to run your cron jobs
    * `ElasticSearch` latest stable version of elasticsearch 
    * `RabbitMQ` broker and queue management service
    * `TimeZone` We set Asia\Tehran Timezone for PHP

## Getting Started
For starting simply use this command
~~~ 
docker-compose up -d
~~~ 
For using Blackfire start containers with bellow command. you need also blackfire client e.g. google chrome extention
~~~ 
docker-compose -f docker-compose.yml -f docker-compose.dev.yml up -d 
~~~ 
For stopping the containers use this command
~~~ 
docker-compose down
~~~  