# Symfony LAMP

Dockerfile and docker-compose.yml optimized for Symfony projects.

This docker includes:

### Images

- php:7.0-apache
- mysql:5.6.34
- tianon/true

### Checks

Check virtual host config for Apache.

### How to

Copy all files inside root project directory.

Execute: `docker-compose build`

And when the process ends

Execute **one**: 

- `docker-compose up` to see apache access.log
- `docker-compose up -d` for background exec

### Symfony parameters

This is **really important**. Database parameters inside *parameters.yml*

```
    database_host: mysql
    database_port: 3306
    database_name: symfony
    database_user: root
    database_password: root
```
