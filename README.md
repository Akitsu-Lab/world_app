# world_app

## 概要
world_app アプリの環境構築
## 利用手順
1. dbのdocker imageを作成
   [dbのリポジトリ](https://github.com/Akitsu-Lab/world_db)のREADMEのうち、`dockerfile から image を作成(ビルド)`までを行う。
2. リポジトリをクローン
    ```shell
    git clone git@github.com:Akitsu-Lab/world_app.git
    ```
   すでにリポジトリが存在する場合は、pullする
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

### MySQLにログイン
- mysqlにログイン
   - DBコンテナに入る
    ```shell
    docker exec -it world_db /bin/bash
    ```
   - パスワードはdocker-compose.ymlのMYSQL_ROOT_PASSWORDを使用
    ```shell
    mysql -u root -p
    ```
   - mysqlからログアウト
    ```shell
    exit
    ```
