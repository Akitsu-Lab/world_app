# world_app

## 概要

world_app アプリの環境構築

## 利用手順

1. db の docker image を作成
   [db のリポジトリ](https://github.com/Akitsu-Lab/world_db)の README のうち、`dockerfile から image を作成(ビルド)`までを行う。
2. リポジトリをクローン
   ```shell
   git clone git@github.com:Akitsu-Lab/world_app.git
   ```
   すでにリポジトリが存在する場合は、pull する
   ```shell
   git pull origin main
   ```
3. コンテナの立ち上げ
   ```shell
   docker-compose up -d
   ```
4. コンテナの停止
   ```shell
   docker-compose down
   ```

### MySQL にログイン

- mysql にログイン
  - DB コンテナに入る
  ```shell
  docker exec -it world_db /bin/bash
  ```
  - パスワードは docker-compose.yml の MYSQL_ROOT_PASSWORD を使用
  ```shell
  mysql -u root -p
  ```
  - mysql からログアウト
  ```shell
  exit
  ```
