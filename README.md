# dockerfileを作るリポジトリ

## mysql5.7.38のイメージとコンテナを作る
```bash
# イメージの作成
$ docker build -t docker-mysql-5-7:1 ./mysql5_7

# イメージからコンテナの作成
# docker run --name コンテナ名 --rm -d -p ホスト側のポート:コンテナ側のポート イメージ名
$ docker run --name mysql_container --rm -d -p 23306:3306 docker-mysql-5-7:1

# コンテナに入る
$ docker exec -it mysql_container bash

# コンテナのmysqlコンソール
$ docker exec -it mysql_containerl mysql -uroot -p
```
