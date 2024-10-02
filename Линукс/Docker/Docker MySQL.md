Чтобы установить на Docker MySQL и пользоваться им надо:
1. Создать папку
2. Создать файл `docker-compose.yml`
3. В файл поместить следующий код:
```yaml
services:
  php:
    build: ./docker/php
    volumes:
      - './src:/var/www/html'
    environment:
      PHP_IDE_CONFIG: "serverName=docker-cli"

  nginx:
    image: nginx:latest
    ports:
      - 80:80
    volumes:
      - './src:/var/www/html'
      - './docker/nginx/conf.d:/etc/nginx/conf.d'

  mysql:
    image: mysql:8
    environment:
      - MYSQL_ROOT_PASSWORD=root
    volumes:
      - './docker/volume/mysql:/var/lib/mysql'
  phpmyadmin:
    image: phpmyadmin/phpmyadmin
    links:
      - mysql:mysql
    ports:
      - 8080:80
    environment:
      PMA_HOST: mysql
      PMA_PORT: 3306
      PMA_ARBITRARY: 1
```
4. Скачать с [GitHub](https://github.com/gmaslov-dev/docker-php-xdebug/tree/main) папку docker, и переместить ее в папку с файлом `docker-compose.yml`
5. В этой же папке открыть консоль и выполнить команду `docker compose up -d`
