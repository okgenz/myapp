# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version
2.5.7

* System dependencies

* Configuration

* 作業ディレクトリ作成
cd ~/Users
mkdir /myapp
cd /Users/myapp

* Dockerfile 作成
touch Dockerfile

* Gemfile 作成
touch Gemfile && touch Gemfile.lock

* Donker
# イメージをビルド
docker-compose build

# コンテナ作成
docker-compose up

# psコマンドで起動確認
docker-compose ps

* Database creation
# DB作成
docker-compose run web rake db:create

* Database initialization
# migrate実行
docker-compose run web rails db:migrate

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions
# herokuのコンテナレジストリにログイン
heroku container:login

# 新しいappを作成
heroku create

# イメージを作成してコンテナレジストリにpush
heroku container:push web

# postgresqlアドオンの無料プランを追加
heroku addons:create heroku-postgresql:hobby-dev

# DBセットアップ
heroku run rails db:migrate

# イメージをherokuへデプロイ
heroku container:release web

# 実際にアクセスして/usersを確認してみる
heroku open

* ...
