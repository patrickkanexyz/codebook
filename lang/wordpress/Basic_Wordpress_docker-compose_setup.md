---
title: Basic Wordpress docker-compose setup
keywords: [wordpress]
---
Make a new `docker-compose.yaml` file and add:

`version: '3'
services:
  mysql:
    image: mysql:latest
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: my_password
      MYSQL_DATABASE: wordpress
      MYSQL_USER: wordpress_user
      MYSQL_PASSWORD: wordpress_password
    volumes:
      - mysql_data:/var/lib/mysql

  wordpress:
    image: wordpress:latest
    depends_on:
      - mysql
    ports:
      - 9000:80
    restart: always
    environment:
      WORDPRESS_DB_HOST: mysql:3306
      WORDPRESS_DB_USER: wordpress_user
      WORDPRESS_DB_PASSWORD: wordpress_password
    volumes:
      - ./wp-content:/var/www/html/wp-content

volumes:
  mysql_data:`

Note: this is not a secure way to deploy wordpress.  You will need to secure
the enviroment variables you are using to handle usernames and passwords.
