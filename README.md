# Docker (For running Laravel/PHP applications)

Global docker container to run your Laravel apps: MySQL/Nginx/PHP

### Includes

+ Mysql 5.7
+ Nginx
+ PHP 7.0 FPM
+ PHP 5.6 FPM

### How to use

#### Install docker-sync

To install docker-sync, run `gem install docker-sync`, or visit [docker-sync.io](http://docker-sync.io/).

#### Nginx

Copy nginx/sites/default.conf.example file to website.conf (or another name with .conf), modify domain, document root and php versions.

#### MySQL

Change root password in `docker-compose.yml` file, in mysql section. See environments block.

#### Shared folders

Change folder (`/Users/gwsmaster/Sites`) with your path of projects in `docker-compose.yml` and `docker-sync.yml`

To build, run and daemonize, you can simply run this command in this folder `docker-compose up -d --build`
