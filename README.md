# Laravel環境構築
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
* Nginx ver. 1.14.0
* PHP ver. 7.1.17
* MySQL ver. 8

## 使用方法
```
1. git clone https://github.com/Kazuo123/docker-laravel.git
2. cd docker-laravel
3. docker-compose up -d
4. docker exec -it php7-fpm bash
5. composer create-project --prefer-dist laravel/laravel laravel "5.5.*"
     ※使いたいバージョンをインストール
6. .envを以下の様に編集
7. Docker For Windows or Mac の 場合           : `http://localhost`
   Docker Toolbox  の場合IPを変更していなければ  : `http://192.168.99.100`
   Laravel Welcomeページが確認できます。
```

## .env 編集
```
DB_HOST=laravel-db
DB_DATABASE=laravel-db
DB_USERNAME=laravel
DB_PASSWORD=laravel
```
