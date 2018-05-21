# Nginx + PHP-FPM
Dockerを使用したLaravel環境を構築

## ツール
* Docker for Windows (or Max)
* Docker ToolBox

## イメージ
* nginx:1.14.0-alpine [(OFFICIAL)](https://hub.docker.com/_/nginx/)
* php:7.1.17-fpm [(OFFICIAL)](https://hub.docker.com/_/php/)
* mysql:latest [(OFFICIAL)](https://hub.docker.com/_/mysql/)
* busybox:latest [(OFFICIAL)](https://hub.docker.com/_/busybox/)

## 環境
* Nginx ver. 1.14.0
* PHP ver. 7.1.17
* MySQL ver. 8
* Larave ver. 5.5.40

## 使用方法
```
1. git clone https://github.com/Kazuo123/docker-laravel.git
2. cd docker-laravel
3. docker-compose up -d
4. docker exec -it php7-fpm bash
5. composer create-project --prefer-dist laravel/laravel laravel "5.5.*"
     ※使いたいバージョンをインストール
6. .envを以下の様に編集
```

```

```
