# Laravel開発環境構築
Laradockではなくofficialイメージを使用して構築します。

## ツール
* Docker for Windows (or Max)
* Docker ToolBox

## イメージ
* nginx:1.14.0-alpine [(OFFICIAL)](https://hub.docker.com/_/nginx/)
* php:7.1.17-fpm [(OFFICIAL)](https://hub.docker.com/_/php/)
* mysql:latest [(OFFICIAL)](https://hub.docker.com/_/mysql/)
* busybox:latest [(OFFICIAL)](https://hub.docker.com/_/busybox/)

## 環境
* Laravel ver. 5.5.40
* Nginx ver. 1.14.0
* PHP ver. 7.1.17
* MySQL ver. 5.7.22

## 使用方法
```
1. https://github.com/KazuhisaFukuda/docker-laravel.git
2. cd docker-laravel
3. docker-compose up -d
4. docker-compose exec app composer install
5. docker-compose exec app cp .env.example .env
6. docker-compose exec app php artisan key:generate
```

## Laravel Ver 変更
```
使用方法 3. docker-compose up -d 後に以下を行ってください
1. docker exec -it php_fpm bash
2. cd .. && rm -fr laravel
3. composer create-project --prefer-dist laravel/laravel laravel "5.5.*"
     ※使用したいバージョンをインストール
4. .envを以下の様に編集
```

## .env 編集
```
DB_HOST=dbserver
DB_DATABASE=laravel-db
DB_USERNAME=laravel
DB_PASSWORD=laravel
```

## Welcome Page
| ツール | URL |
| ---- | ---- |
| docker for windows (or mac) | http://localhost |
| docker toolbox | http://192.168.99.100 |
