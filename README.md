# fasion EC

## ・environment

### ・app_server_fasion_ec

- Ruby 2.5.1
- Rails 5.1.6
- Docker (Ruby:2.5.1)
- MySQL 5.6
- API mode

### ・front_server_fasion_ec

- Node.js 12.8.0
- Nuxt.js
- Docker（node:12.8.0）

### AWS Architecture

![fasion-ec-infra-architect](https://user-images.githubusercontent.com/45042275/65850902-b77ea380-e38b-11e9-8c6f-a01193d80952.png)

### DB Architecture

![fasion-ec](https://user-images.githubusercontent.com/45042275/65926282-7b048380-e42f-11e9-9d1e-a1ba014d3225.png)

### API Specification

#### API一覧

|HTTPメソッド|リクエストURL|機能概要|
|------|----|-------|
|GET|/api/v1/items|items一覧を取得|
|GET|/api/v1/items/:id|1つのitemsを取得|
|POST|/api/v1/items/:id|itemsを新しく作成|
|PUT|/api/v1/items/:id|itemsを更新|
|DELETE|/api/v1/items/:id|itemsを削除|
|GET|/api/v1/news|news一覧を取得|
|GET|/api/v1/news/:id|1つのnewsを取得|
|POST|/api/v1/news/:id|newsを新しく作成|
|PUT|/api/v1/news/:id|newsを更新|
|DELETE|/api/v1/news/:id|newsを削除|
|GET|/api/v1/contacts|お問い合わせを一覧|
|GET|/api/v1/contacts|1つのお問い合わせを取得|
|POST|/api/v1/contacts|お問い合わせを登録|

## ・Set Up

git clone
```
$ git clone https://github.com/THitokuse/fasion_ec_docker-compose.git fasion-ec
$ cd fasion-ec
$ git clone https://github.com/THitokuse/app_server_fasion_ec.git
$ git clone https://github.com/THitokuse/front_server_fasion_ec.git
```

create .env file in app_server_fasion_ec dir
```.env
DATABASE_USER = root
DATABASE_PASSWORD = fasion-ec
DATABASE_HOST = db
RAILS_MAX_THREADS = 5

AWS_ACCESS_KEY_ID = #####
AWS_SECRET_ACCESS_KEY = #####
AWS_REGION = ######
AWS_S3_BUCKET = #####
```

build docker-compose
```
$ docker-compose build
$ docker-compose up -d
```
