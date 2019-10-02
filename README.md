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
|POST|/api/v1/items/:id|itemsを新しく作成|
|PUT|/api/v1/items/:id|itemsを更新|
|DELETE|/api/v1/items/:id|itemsを削除|
|POST|/api/v1/contacts|お問い合わせを登録|
|GET|/api/v1/contacts|お問い合わせを一覧|

#### ・items一覧を取得する
HTTPメソッド： GET

リクエストURL： /api/v1/items

パラメータのデフォルト値：
```
{
  "status": "SUCCESS",
  "data": [
    {
      "id": int(8),
      "name": string(255),
      "price": int(8),
      "price": int,
      "content": text,
      "images": [
        {
          "id": int(8),
          "src": string(255)
        },
        {
          "id": int(8),
          "src": string(255)
        }
      ]
    },
    {
      "id": int(8),
      "name": string(255),
      "price": int(8),
      "price": int,
      "content": text
    }
  ]
}
```
※ 入力パラメータによってレスポンス情報は変化する。

#### ・itemsを新しく作成する
HTTPメソッド： POST

リクエストURL： /api/v1/items

パラメータのデフォルト値：
```
{
  "status": "SUCCESS",
  "data": {
    "id": int(8),
    "name": string(255),
    "price": int(8),
    "price": int,
    "content": text,
    "images": [
      {
        "id": int(8),
        "src": string(255)
      },
      {
        "id": int(8),
        "src": string(255)
      }
    ]
  }
}
```
※ 入力パラメータによってレスポンス情報は変化する。

#### ・itemsを更新する
HTTPメソッド： PUT

リクエストURL： /api/v1/items/:id

パラメータのデフォルト値：
```
{
  "status": "SUCCESS",
  "data": {
    "id": int(8),
    "name": string(255),
    "price": int(8),
    "price": int,
    "content": text,
    "images": [
      {
        "id": int(8),
        "src": string(255)
      },
      {
        "id": int(8),
        "src": string(255)
      }
    ]
  }
}
```
※ 更新する入力パラメータのみを送る

#### ・itemsを削除する
HTTPメソッド： DELETE

リクエストURL： /api/v1/items/:id

パラメータのデフォルト値：
```
{
  "status": "SUCCESS",
  "data": {
    "id": int(8),
    "name": string(255),
    "price": int(8),
    "price": int,
    "content": text,
    "images": [
      {
        "id": int(8),
        "src": string(255)
      },
      {
        "id": int(8),
        "src": string(255)
      }
    ]
  }
}
```
※ 更新する入力パラメータのみを送る

#### ・contact（お問い合わせ）内容を送る
HTTPメソッド： POST

リクエストURL： /api/v1/contacts

パラメータのデフォルト値：
```
{
  "status": "SUCCESS",
  "data": {
    "name": string(255),
    "email": string(255),
    "content": string(255)
  }
}
```

#### ・contact（お問い合わせ）内容を送る
HTTPメソッド： GET

リクエストURL： /api/v1/contacts

パラメータのデフォルト値：
```
{
  "status": "SUCCESS",
  "data": {
    "name": string(255),
    "email": string(255),
    "content": string(255)
  }
}
```
※ 入力パラメータによってレスポンス情報は変化する。

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
USER=root
PASSWORD=
HOST=db
```

build docker-compose
```
$ docker-compose build
$ docker-compose up -d
```
