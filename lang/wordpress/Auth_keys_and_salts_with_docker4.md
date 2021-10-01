---
title: Auth keys and salts with docker4
keywords: [wordpress]
---
You can change the authentication keys and salts that wordpress uses inside
Docker using the docker enviroment variables:

AUTH_KEY',         getenv_docker('WORDPRESS_AUTH_KEY'
SECURE_AUTH_KEY',  getenv_docker('WORDPRESS_SECURE_AUTH_KEY'
LOGGED_IN_KEY',    getenv_docker('WORDPRESS_LOGGED_IN_KEY'
NONCE_KEY',        getenv_docker('WORDPRESS_NONCE_KEY'
AUTH_SALT',        getenv_docker('WORDPRESS_AUTH_SALT'
SECURE_AUTH_SALT', getenv_docker('WORDPRESS_SECURE_AUTH_SALT'
LOGGED_IN_SALT',   getenv_docker('WORDPRESS_LOGGED_IN_SALT'
NONCE_SALT',       getenv_docker('WORDPRESS_NONCE_SALT'

You can always generate these keys from:
(https://api.wordpress.org/secret-key/1.1/salt/)

Also see Docker Enviroment Variables
