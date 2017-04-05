# Docker (For running Laravel/PHP applications)

Global docker container to run your Laravel apps: MySQL/Nginx/PHP

![Laravel & Docker](https://cloud.githubusercontent.com/assets/6238393/24731434/06790214-1a7b-11e7-87d7-f7c0aa71be17.png)

### Includes

+ Mysql 5.7
+ Nginx
+ PHP 7.0 FPM
+ PHP 5.6 FPM

### How to use

#### Clone

Clone this repo somewhere in safe place. This will be your global configuration. For example: `cd ~/ && git clone https://github.com/Lotuashvili/Docker.git`

#### Install docker-sync

To install docker-sync, run `gem install docker-sync`, or visit [docker-sync.io](http://docker-sync.io/).

#### Nginx

Copy nginx/sites/default.conf.example file to website.conf (or another name with .conf), modify domain, document root and php versions.

#### MySQL

Change root password in `docker-compose.yml` file, in mysql section. See environments block.

#### Shared folders

Change folder (`/Users/gwsmaster/Sites`) with your path of projects in `docker-compose.yml` and `docker-sync.yml`

#### Running docker

To build, run and daemonize, you can simply run this command in this folder `docker-compose up -d --build`

Restart machine: `docker-compose down && docker-compose up -d` (run with --build argument if you changed php's Dockerfile)
