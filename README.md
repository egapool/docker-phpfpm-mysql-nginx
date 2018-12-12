さくっとphp-fpm,nginx,mysql環境をたてるやつ。redis付き

```
git clone https://github.com/egapool/docker-phpfpm-mysql-nginx.git
cd docker-phpfpm-mysql-nginx
cp .env.sample .env
```

.env

* DOMAIN:なくても良い。
* SRC_DIR=プロジェクトルート
* PUBLIC_DIR=プロジェクトルートからdocument rootまでの相対パス。先頭に「/」はつけない



ビルド
```
$ docker-compose up --build
```

バックグランド起動
```
$ docker-compose up -d
```

終了
```
$ docker-compose stop
```

PHP CLIの実行
```
$ docker-compose run php-cli php {command}

// 例
$ docker-compose run php-cli php -v
```



see http://localhost:8000 or http://your.domain:8000
