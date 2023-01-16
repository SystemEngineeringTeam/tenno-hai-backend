# tenno-hai-front

https://hackmd.io/@hihumikan/r1aRDgpqs/edit

## Introduction

ユーザ登録と問題やランキング表示、インストール方法などの天皇杯をサポートするWebサービスを提供します。 Laravel All in Oneで作成されたアプリですが、WebAPIも利用可能とします。

## Enbironment

| Tool     | Version |
| -------- | ------- |
| Composer |         |
| Node.js  |         |
| PHP      |         |

## Usage

### Laravel

#### Dockerで行う場合

```bash
composer install
cp .env.sample .env
./vendor/bin/sail up
sail php artisan key:generate
sail php artisan migrate
sail npm install
sail npm run dev
```

#### PHP(Composer)で行う場合

```bash
composer install
cp .env.sample .env
php artisan key:generate
php artisan migrate
php artsan serve
npm install
npm run dev
```

### CDK

https://aws.amazon.com/jp/cdk/

## 機能

- 問題文表示機能
    - MarkDown
- 環境構築機能 
- チェックサービスの導入
    - Webでユーザごとの採点(LaravelAPI)
    - OTPを使って判定コードを持ってくる
    - ランキング形式で表示
- 会員登録機能(GitHubAuth?)
    - グループ機能

## DB

- User
    - id
    - name
    - email
    - verified_at
    - password
    - remembertoken
    - group_id
    - timestamps
- Issue
    - id
    - title
    - content
    - category
    - timestamps
- Category
    - id
    - category_name
    - timestamps
- Result
    - id
    - issue_id
    - user_id
    - point
    - timestamps
- Group
    - id
    - name
    - timestamps
