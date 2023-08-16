# Board App

## サービス概要
Board Appは、ユーザー同士が情報を共有・交換するためのオンラインプラットフォームです。ユーザーは掲示板に投稿を行い、他のユーザーとのコミュニケーションを楽しむことができます。

## 想定されるユーザー層
SNSやフォーラムを利用する20代から50代の男女。特定のトピックや興味に関して情報を共有したり、意見を交換したいと考えるユーザー。

## 使用技術
- Ruby 3.2.2
- Rails 7.0.7
- MySQL (gem: mysql2 0.5)
- Puma Web Server 5.0
- Sprockets-Rails
- Importmap-Rails
- Turbo-Rails
- Stimulus-Rails
- Jbuilder
- tzinfo-data
- Bootsnap
- Web-console (Development)
- Debug (Development & Test)
- Capybara, Selenium-webdriver, Webdrivers (Test)

## サービスコンセプト
* インターネット上で気軽に情報を共有・交換できる場所が求められている。
* ユーザー間のコミュニケーションを促進し、情報の価値を最大化する。
* シンプルで使いやすいデザイン。
* 効率的な情報検索機能やブックマーク機能を実装。

## 実装を予定している機能
### MVP
* 会員登録・ログイン機能
* 掲示板への投稿・閲覧
* コメント機能
* 画像アップロード機能
* ブックマーク機能

### その後の機能
* いいね機能
* ユーザーのプロフィール編集機能
* 掲示板の検索機能
* 管理者画面
* Ajaxを用いた動的なUIの実装

## Dockerを使ってのローカル環境構築手順

### 前提条件
- Dockerがインストールされている
- Docker Composeがインストールされている

### 手順

1. リポジトリをクローンする
```bash
git clone git@github.com:ASONE0923/board_app.git
cd board_app
```

2. Dockerイメージをビルドする
```bash
docker-compose build
```

3. データベースを作成・マイグレーションを実行する
```bash
docker-compose run web rails db:create db:migrate
```

4. アプリケーションを立ち上げる
```bash
docker-compose up
```

5. ブラウザでアプリケーションにアクセスする
通常、[http://localhost:3000](http://localhost:3000) にアクセスすることでアプリケーションが表示されます。

### その他のコマンド

- 依存ライブラリ（gemなど）を追加した場合:
```bash
docker-compose build
```

- データベースのマイグレーションを実行する場合:
```bash
docker-compose run web rails db:migrate
```

- アプリケーションを終了する場合:
```bash
docker-compose down
```
