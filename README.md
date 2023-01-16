# tenno-hai-front

https://hackmd.io/@hihumikan/r1aRDgpqs/edit

## Introduction

ユーザ登録と問題やランキング表示、インストール方法などの天皇杯をサポートするWebサービスを提供します。 Laravel All in Oneで作成されたアプリですが、WebAPIも利用可能とします。

## Usage

tennohai.qqey.net から利用出来ます。

<!-- TODO -->

## Purpose

大学サークルであるシス研では、オンプレミス環境のサーバがあり、現場と変わらない本格的なネットワーク環境を構築しています。

しかしながら、サークルという環境は企業とは違い、人の流動性があり、人が手入れするのが難しくなっています。

属人化や人手不足が課題になっていることから立案されたのがプロジェクト天皇杯です。

## Requirement definition
<!-- 要件定義,実装した機能 -->

- 問題文表示機能
    - MarkDown
- 環境構築機能 
- チェックサービスの導入
    - Webでユーザごとの採点(LaravelAPI)
    - OTPを使って判定コードを持ってくる
    - ランキング形式で表示
- 会員登録機能(GitHubAuth?)
    - グループ機能

## Feature
<!-- 実装予定 -->

## Enbironment

| Tool     | Version |
| -------- | ------- |
| Composer |         |
| Node.js  |         |
| PHP      |         |

## Development

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

Laravel on ECS(Fargate)を実装する(予定)
https://aws.amazon.com/jp/cdk/


## Database

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
    - category_id
    - timestamps
- Category
    - id
    - name
    - timestamps
- Result
    - id
    - issue_id
    - user_id
    - answer
      - bool
    - timestamps
- Group
    - id
    - name
    - timestamps

## Web


## WebAPI


